<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "b5466bcedc3c75aa35476270362f626a",
  "translation_date": "2025-07-09T16:25:20+00:00",
  "source_file": "15-rag-and-vector-databases/data/frameworks.md",
  "language_code": "ru"
}
-->
# Фреймворки для нейронных сетей

Как мы уже узнали, чтобы эффективно обучать нейронные сети, нужно сделать две вещи:

* Операции с тензорами, например умножение, сложение и вычисление функций, таких как сигмоида или softmax
* Вычисление градиентов всех выражений для выполнения оптимизации методом градиентного спуска

Хотя библиотека `numpy` справляется с первой задачей, нам нужен механизм для вычисления градиентов. В нашем фреймворке, который мы разработали в предыдущем разделе, нам приходилось вручную программировать все функции производных внутри метода `backward`, который выполняет обратное распространение ошибки. В идеале фреймворк должен позволять вычислять градиенты *любого выражения*, которое мы можем определить.

Ещё одна важная вещь — возможность выполнять вычисления на GPU или других специализированных вычислительных устройствах, таких как TPU. Обучение глубоких нейронных сетей требует *огромного* количества вычислений, и возможность распараллеливания этих вычислений на GPU очень важна.

> ✅ Термин «распараллеливание» означает распределение вычислений между несколькими устройствами.

В настоящее время двумя самыми популярными фреймворками для нейросетей являются TensorFlow и PyTorch. Оба предоставляют низкоуровневый API для работы с тензорами как на CPU, так и на GPU. Поверх низкоуровневого API существуют высокоуровневые API — Keras и PyTorch Lightning соответственно.

Низкоуровневый API | TensorFlow | PyTorch
-------------------|------------|---------
Высокоуровневый API| Keras      | PyTorch

**Низкоуровневые API** в обоих фреймворках позволяют строить так называемые **вычислительные графы**. Этот граф определяет, как вычислить выход (обычно функцию потерь) при заданных входных параметрах, и может быть отправлен на вычисление на GPU, если он доступен. Существуют функции для дифференцирования этого вычислительного графа и вычисления градиентов, которые затем используются для оптимизации параметров модели.

**Высокоуровневые API** рассматривают нейронные сети как **последовательность слоёв** и значительно упрощают построение большинства нейросетей. Обучение модели обычно сводится к подготовке данных и вызову функции `fit`.

Высокоуровневый API позволяет быстро создавать типичные нейронные сети, не вдаваясь в множество деталей. В то же время низкоуровневый API даёт гораздо больше контроля над процессом обучения, поэтому он часто используется в исследованиях, когда работают с новыми архитектурами нейросетей.

Важно понимать, что можно использовать оба API вместе: например, разработать собственную архитектуру слоя с помощью низкоуровневого API, а затем использовать её внутри более крупной сети, построенной и обученной с помощью высокоуровневого API. Или определить сеть с помощью высокоуровневого API как последовательность слоёв, а затем использовать собственный низкоуровневый цикл обучения для оптимизации. Оба API основаны на одних и тех же базовых концепциях и хорошо сочетаются друг с другом.

## Обучение

В этом курсе мы предлагаем материалы как для PyTorch, так и для TensorFlow. Вы можете выбрать предпочитаемый фреймворк и проходить только соответствующие ноутбуки. Если вы не уверены, какой фреймворк выбрать, почитайте обсуждения в интернете на тему **PyTorch vs. TensorFlow**. Также полезно ознакомиться с обоими фреймворками для лучшего понимания.

Где возможно, мы будем использовать высокоуровневые API для простоты. Однако мы считаем важным понять, как работают нейронные сети изнутри, поэтому в начале мы начнём с работы с низкоуровневым API и тензорами. Если же вы хотите быстро начать и не тратить много времени на изучение деталей, можете пропустить этот этап и сразу перейти к ноутбукам с высокоуровневым API.

## ✍️ Упражнения: Фреймворки

Продолжайте обучение в следующих ноутбуках:

Низкоуровневый API | TensorFlow+Keras Notebook | PyTorch
-------------------|----------------------------|---------
Высокоуровневый API| Keras                      | *PyTorch Lightning*

После освоения фреймворков давайте вспомним понятие переобучения.

# Переобучение

Переобучение — крайне важная концепция в машинном обучении, и её очень важно правильно понимать!

Рассмотрим задачу аппроксимации 5 точек (обозначенных `x` на графиках ниже):

!linear | overfit
-------------------------|--------------------------
**Линейная модель, 2 параметра** | **Нелинейная модель, 7 параметров**
Ошибка на обучении = 5.3 | Ошибка на обучении = 0
Ошибка на валидации = 5.1 | Ошибка на валидации = 20

* Слева мы видим хорошую аппроксимацию прямой линией. Поскольку количество параметров адекватно, модель правильно улавливает суть распределения точек.
* Справа модель слишком мощная. Поскольку у нас всего 5 точек, а параметров 7, модель может подстроиться так, чтобы пройти через все точки, сделав ошибку на обучении равной 0. Однако это мешает модели понять правильный паттерн данных, поэтому ошибка на валидации очень высокая.

Очень важно найти правильный баланс между сложностью модели (числом параметров) и количеством обучающих примеров.

## Почему возникает переобучение

  * Недостаточно обучающих данных
  * Слишком сложная модель
  * Слишком много шума во входных данных

## Как обнаружить переобучение

Как видно из графика выше, переобучение можно определить по очень низкой ошибке на обучении и высокой ошибке на валидации. Обычно во время обучения обе ошибки сначала уменьшаются, а затем в какой-то момент ошибка на валидации перестаёт снижаться и начинает расти. Это сигнал о переобучении и признак того, что, вероятно, стоит остановить обучение (или хотя бы сохранить снимок модели).

overfitting

## Как предотвратить переобучение

Если вы видите, что происходит переобучение, можно сделать следующее:

 * Увеличить объём обучающих данных
 * Уменьшить сложность модели
 * Использовать методы регуляризации, например Dropout, который мы рассмотрим позже.

## Переобучение и компромисс смещения и разброса

Переобучение — это частный случай более общей проблемы в статистике, называемой компромиссом смещения и разброса (Bias-Variance Tradeoff). Если рассмотреть возможные источники ошибок в модели, можно выделить два типа:

* **Ошибки смещения** возникают, когда алгоритм не может правильно уловить зависимость в обучающих данных. Это может быть связано с тем, что модель недостаточно мощная (**недообучение**).
* **Ошибки разброса** возникают, когда модель аппроксимирует шум во входных данных вместо значимых зависимостей (**переобучение**).

Во время обучения ошибка смещения уменьшается (модель учится аппроксимировать данные), а ошибка разброса растёт. Важно вовремя остановить обучение — либо вручную (при обнаружении переобучения), либо автоматически (с помощью регуляризации) — чтобы избежать переобучения.

## Итог

В этом уроке вы узнали о различиях между API двух самых популярных AI-фреймворков — TensorFlow и PyTorch. Кроме того, вы познакомились с очень важной темой — переобучением.

## 🚀 Задание

В сопроводительных ноутбуках внизу вы найдёте «задания»; пройдите ноутбуки и выполните их.

## Обзор и самостоятельное изучение

Изучите следующие темы:

- TensorFlow
- PyTorch
- Переобучение

Ответьте себе на вопросы:

- В чём разница между TensorFlow и PyTorch?
- В чём разница между переобучением и недообучением?

## Домашнее задание

В этой лабораторной работе вам предстоит решить две задачи классификации с помощью однослойных и многослойных полностью связанных сетей, используя PyTorch или TensorFlow.

**Отказ от ответственности**:  
Этот документ был переведен с помощью сервиса автоматического перевода [Co-op Translator](https://github.com/Azure/co-op-translator). Несмотря на наши усилия по обеспечению точности, просим учитывать, что автоматические переводы могут содержать ошибки или неточности. Оригинальный документ на его исходном языке следует считать авторитетным источником. Для получения критически важной информации рекомендуется обращаться к профессиональному человеческому переводу. Мы не несем ответственности за любые недоразумения или неправильные толкования, возникшие в результате использования данного перевода.