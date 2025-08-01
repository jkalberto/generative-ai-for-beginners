<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "b5466bcedc3c75aa35476270362f626a",
  "translation_date": "2025-07-09T16:37:47+00:00",
  "source_file": "15-rag-and-vector-databases/data/frameworks.md",
  "language_code": "sr"
}
-->
# Neural Network Frameworks

Као што смо већ научили, да бисмо могли ефикасно тренирати неуронске мреже, потребно је да урадимо две ствари:

* Да радимо са тензорима, нпр. да множимо, сабирамо и израчунавамо неке функције као што су sigmoid или softmax
* Да израчунавамо градијенте свих израза, како бисмо могли да извршимо оптимизацију методом градијентног спуста

Иако `numpy` библиотека може да обави први део, потребан нам је неки механизам за израчунавање градијената. У нашем оквиру који смо развили у претходном делу морали смо ручно да програмирамо све функције извођења унутар `backward` методе, која ради backpropagation. Идеално, оквир би требао да нам пружи могућност да израчунавамо градијенте *било ког израза* који можемо дефинисати.

Још једна важна ствар је могућност извођења рачунања на GPU-у или неким другим специјализованим рачунским јединицама, као што је TPU. Тренирање дубоких неуронских мрежа захтева *појамно* много рачунања, и веома је важно да се та рачунања могу паралелизовати на GPU-овима.

> ✅ Термин 'паралелизовати' значи распоредити рачунања на више уређаја.

Тренутно, два најпопуларнија неуронска фрејмворка су: TensorFlow и PyTorch. Обојица пружају ниско-нивоу API за рад са тензорима како на CPU-у тако и на GPU-у. Изнад ниско-нивоу API-ја постоји и виши ниво API-ја, који се зове Keras односно PyTorch Lightning.

Ниско-нивоу API | TensorFlow | PyTorch  
--------------|-------------------------------------|--------------------------------  
Високо-нивоу API | Keras | PyTorch

**Ниско-нивоу API-ји** у оба фрејмворка омогућавају изградњу такозваних **рачунских графова**. Тај граф дефинише како се израчунава излаз (обично функција губитка) са датим улазним параметрима, и може се послати на извршавање на GPU ако је доступан. Постоје функције за диференцирање овог рачунског графа и израчунавање градијената, који се затим могу користити за оптимизацију параметара модела.

**Високо-нивоу API-ји** углавном третирају неуронске мреже као **низ слојева**, и олакшавају конструисање већине неуронских мрежа. Тренирање модела обично захтева припрему података, а затим позив функције `fit` која обавља тренинг.

Високо-нивоу API омогућава брзо конструисање типичних неуронских мрежа без бриге о многим детаљима. Истовремено, ниско-нивоу API пружа много већу контролу над процесом тренинга, због чега се често користи у истраживањима када се ради са новим архитектурама неуронских мрежа.

Важно је разумети да се оба API-ја могу користити заједно, нпр. можете развити своју архитектуру слојева користећи ниско-нивоу API, а затим је користити у већој мрежи конструисаној и тренираној помоћу високо-нивоу API-ја. Или можете дефинисати мрежу као низ слојева користећи високо-нивоу API, а затим користити свој ниско-нивоу тренинг циклус за оптимизацију. Обa API-ја користе исте основне концепте и дизајнирани су да добро функционишу заједно.

## Learning

У овом курсу нудимо већину садржаја и за PyTorch и за TensorFlow. Можете изабрати свој омиљени фрејмворк и проћи само кроз одговарајуће белешке. Ако нисте сигурни који фрејмворк да изаберете, прочитајте неке дискусије на интернету о теми **PyTorch vs. TensorFlow**. Такође можете погледати оба фрејмворка да бисте боље разумели.

Где год је могуће, користићемо високо-нивоу API ради једноставности. Међутим, сматрамо да је важно разумети како неуронске мреже функционишу од темеља, па зато на почетку радимо са ниско-нивоу API-јем и тензорима. Међутим, ако желите брзо да почнете и не желите да трошите много времена на учење ових детаља, можете прескочити то и одмах прећи на белешке са високо-нивоу API-јем.

## ✍️ Exercises: Frameworks

Наставите учење у следећим белешкама:

Ниско-нивоу API | TensorFlow+Keras белешка | PyTorch  
--------------|-------------------------------------|--------------------------------  
Високо-нивоу API | Keras | *PyTorch Lightning*

Након што савладате фрејмворке, хајде да поновимо појам overfitting.

# Overfitting

Overfitting је изузетно важан појам у машинском учењу, и веома је важно правилно га разумети!

Размотримо следећи проблем апроксимације 5 тачака (представљених са `x` на графиконима испод):

!linear | overfit  
-------------------------|--------------------------  
**Линеарни модел, 2 параметра** | **Нелинеарни модел, 7 параметара**  
Грешка на тренингу = 5.3 | Грешка на тренингу = 0  
Грешка на валидацији = 5.1 | Грешка на валидацији = 20

* Са леве стране видимо добру апроксимацију правом линијом. Пошто је број параметара адекватан, модел исправно схвата распоред тачака.
* Са десне стране модел је превише сложен. Пошто имамо само 5 тачака, а модел има 7 параметара, он може да се прилагоди тако да прође кроз све тачке, чиме је грешка на тренингу 0. Међутим, то спречава модел да разуме прави образац иза података, па је грешка на валидацији веома велика.

Веома је важно постићи праву равнотежу између сложености модела (броја параметара) и броја узорака за тренинг.

## Зашто долази до overfitting-а

  * Недовољно података за тренинг
  * Превише сложен модел
  * Превише шума у улазним подацима

## Како открити overfitting

Као што се види на горњем графику, overfitting се може препознати по веома малој грешци на тренингу и великој грешци на валидацији. Обично током тренинга ћемо видети да и грешка на тренингу и на валидацији опадају, а онда у неком тренутку грешка на валидацији може престати да опада и почети да расте. То је знак overfitting-а и индикатор да вероватно треба зауставити тренинг у том тренутку (или бар направити снимак модела).

overfitting

## Како спречити overfitting

Ако приметите да долази до overfitting-а, можете урадити једно од следећег:

 * Повећати количину података за тренинг
 * Смањити сложеност модела
 * Користити неку технику регуларизације, као што је Dropout, коју ћемо размотрити касније.

## Overfitting и Bias-Variance Tradeoff

Overfitting је у ствари случај општег проблема у статистици који се зове Bias-Variance Tradeoff. Ако размотримо могуће изворе грешке у нашем моделу, можемо уочити два типа грешака:

* **Bias грешке** настају када наш алгоритам не може исправно да ухвати везу између података за тренинг. То може бити последица тога што наш модел није довољно сложен (**underfitting**).
* **Variance грешке** настају када модел апроксимира шум у улазним подацима уместо значајне везе (**overfitting**).

Током тренинга, bias грешка опада (како модел учи да апроксимира податке), а variance грешка расте. Важно је зауставити тренинг - било ручно (када откријемо overfitting) или аутоматски (увођењем регуларизације) - како бисмо спречили overfitting.

## Закључак

У овој лекцији сте научили о разликама између различитих API-ја за два најпопуларнија AI фрејмворка, TensorFlow и PyTorch. Поред тога, упознали сте се са веома важном темом, overfitting-ом.

## 🚀 Изазов

У пратећим белешкама наћи ћете „задатке“ на дну; радите кроз белешке и решавајте задатке.

## Преглед и самостално учење

Истражите следеће теме:

- TensorFlow  
- PyTorch  
- Overfitting

Поставите себи следећа питања:

- Која је разлика између TensorFlow и PyTorch?  
- Која је разлика између overfitting-а и underfitting-а?

## Задатак

У овом лабораторијском задатку тражи се да решите два проблема класификације користећи једнослојне и вишеслојне потпуно повезане мреже користећи PyTorch или TensorFlow.

**Одрицање од одговорности**:  
Овај документ је преведен коришћењем AI услуге за превођење [Co-op Translator](https://github.com/Azure/co-op-translator). Иако се трудимо да превод буде тачан, молимо вас да имате у виду да аутоматски преводи могу садржати грешке или нетачности. Оригинални документ на његовом изворном језику треба сматрати ауторитетним извором. За критичне информације препоручује се професионални људски превод. Нисмо одговорни за било каква неспоразума или погрешна тумачења која произилазе из коришћења овог превода.