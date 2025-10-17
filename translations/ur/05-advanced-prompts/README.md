<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "ffb706de93ef518f31e0a675c66dfce1",
  "translation_date": "2025-10-17T13:10:03+00:00",
  "source_file": "05-advanced-prompts/README.md",
  "language_code": "ur"
}
-->
# جدید پرامپٹس بنانا

[![جدید پرامپٹس بنانا](../../../translated_images/05-lesson-banner.522610fd4a2cd82dbed66bb7e6fe104ed6da172e085dbb4d9100b28dc73ed435.ur.png)](https://youtu.be/BAjzkaCdRok?si=NmUIyRf7-cDgbjtt)

آئیے پچھلے باب سے کچھ سیکھنے کا خلاصہ کریں:

> پرامپٹ _انجینئرنگ_ وہ عمل ہے جس کے ذریعے ہم **ماڈل کو زیادہ متعلقہ جوابات کی طرف رہنمائی کرتے ہیں**، زیادہ مفید ہدایات یا سیاق و سباق فراہم کرکے۔

پرامپٹس لکھنے کے دو مراحل بھی ہیں: پرامپٹ کی تشکیل، متعلقہ سیاق و سباق فراہم کرکے، اور دوسرا حصہ _آپٹیمائزیشن_، یعنی پرامپٹ کو بتدریج بہتر بنانا۔

اس وقت، ہمیں پرامپٹس لکھنے کا بنیادی علم حاصل ہے، لیکن ہمیں مزید گہرائی میں جانے کی ضرورت ہے۔ اس باب میں، آپ مختلف پرامپٹس آزمانے سے لے کر یہ سمجھنے تک جائیں گے کہ ایک پرامپٹ دوسرے سے بہتر کیوں ہے۔ آپ سیکھیں گے کہ کچھ بنیادی تکنیکوں کے مطابق پرامپٹس کیسے بنائیں جو کسی بھی LLM پر لاگو کی جا سکتی ہیں۔

## تعارف

اس باب میں، ہم درج ذیل موضوعات کا احاطہ کریں گے:

- مختلف تکنیکوں کو اپنے پرامپٹس پر لاگو کرکے پرامپٹ انجینئرنگ کے علم کو بڑھائیں۔
- اپنے پرامپٹس کو آؤٹ پٹ میں مختلف کرنے کے لیے ترتیب دیں۔

## سیکھنے کے اہداف

اس سبق کو مکمل کرنے کے بعد، آپ قابل ہوں گے:

- پرامپٹ انجینئرنگ کی تکنیکوں کو لاگو کریں جو آپ کے پرامپٹس کے نتائج کو بہتر بناتی ہیں۔
- پرامپٹنگ کریں جو یا تو مختلف ہو یا متعین۔

## پرامپٹ انجینئرنگ

پرامپٹ انجینئرنگ وہ عمل ہے جس کے ذریعے پرامپٹس تخلیق کیے جاتے ہیں جو مطلوبہ نتیجہ پیدا کریں گے۔ پرامپٹ انجینئرنگ صرف ایک ٹیکسٹ پرامپٹ لکھنے سے زیادہ ہے۔ پرامپٹ انجینئرنگ کوئی انجینئرنگ ڈسپلن نہیں ہے، بلکہ یہ تکنیکوں کا ایک مجموعہ ہے جسے آپ مطلوبہ نتیجہ حاصل کرنے کے لیے لاگو کر سکتے ہیں۔

### پرامپٹ کی ایک مثال

آئیے ایک بنیادی پرامپٹ لیں جیسے یہ:

> جغرافیہ پر 10 سوالات تیار کریں۔

اس پرامپٹ میں، آپ دراصل مختلف پرامپٹ تکنیکوں کا ایک مجموعہ لاگو کر رہے ہیں۔

آئیے اسے توڑتے ہیں۔

- **سیاق و سباق**، آپ نے وضاحت کی کہ یہ "جغرافیہ" کے بارے میں ہونا چاہیے۔
- **آؤٹ پٹ کو محدود کرنا**، آپ 10 سوالات سے زیادہ نہیں چاہتے۔

### سادہ پرامپٹنگ کی حدود

آپ کو مطلوبہ نتیجہ مل سکتا ہے یا نہیں۔ آپ کے سوالات تیار ہو جائیں گے، لیکن جغرافیہ ایک بڑا موضوع ہے اور آپ کو وہ نہیں مل سکتا جو آپ چاہتے ہیں، درج ذیل وجوہات کی بنا پر:

- **بڑا موضوع**، آپ نہیں جانتے کہ یہ ممالک، دارالحکومتوں، دریاؤں وغیرہ کے بارے میں ہوگا۔
- **فارمیٹ**، اگر آپ چاہتے ہیں کہ سوالات کسی خاص انداز میں فارمیٹ کیے جائیں تو کیا ہوگا؟

جیسا کہ آپ دیکھ سکتے ہیں، پرامپٹس بناتے وقت غور کرنے کے لیے بہت کچھ ہے۔

اب تک، ہم نے ایک سادہ پرامپٹ کی مثال دیکھی ہے، لیکن جنریٹو AI مختلف کرداروں اور صنعتوں میں لوگوں کی مدد کے لیے بہت کچھ کرنے کی صلاحیت رکھتا ہے۔ آئیے اگلی کچھ بنیادی تکنیکوں کو دریافت کریں۔

### پرامپٹنگ کی تکنیکیں

سب سے پہلے، ہمیں یہ سمجھنے کی ضرورت ہے کہ پرامپٹنگ ایک LLM کی _ابھرتی ہوئی_ خصوصیت ہے، یعنی یہ ماڈل میں شامل کوئی خصوصیت نہیں ہے بلکہ کچھ ایسا ہے جو ہم ماڈل کو استعمال کرتے ہوئے دریافت کرتے ہیں۔

کچھ بنیادی تکنیکیں ہیں جنہیں ہم LLM کو پرامپٹ کرنے کے لیے استعمال کر سکتے ہیں۔ آئیے انہیں دریافت کریں۔

- **زیرو شاٹ پرامپٹنگ**، یہ پرامپٹنگ کی سب سے بنیادی شکل ہے۔ یہ ایک واحد پرامپٹ ہے جو LLM سے اس کے تربیتی ڈیٹا کی بنیاد پر جواب طلب کرتا ہے۔
- **فیوشاٹ پرامپٹنگ**، اس قسم کی پرامپٹنگ LLM کو 1 یا زیادہ مثالیں فراہم کرکے رہنمائی کرتی ہے جن پر وہ اپنے جواب کو تیار کرنے کے لیے انحصار کر سکتا ہے۔
- **چین آف تھوٹ**، اس قسم کی پرامپٹنگ LLM کو بتاتی ہے کہ کسی مسئلے کو مراحل میں کیسے تقسیم کیا جائے۔
- **جنریٹڈ نالج**، پرامپٹ کے جواب کو بہتر بنانے کے لیے، آپ اپنے پرامپٹ کے ساتھ اضافی طور پر تیار کردہ حقائق یا علم فراہم کر سکتے ہیں۔
- **لیسٹ ٹو موسٹ**، چین آف تھوٹ کی طرح، یہ تکنیک کسی مسئلے کو مراحل کی ایک سیریز میں تقسیم کرنے کے بارے میں ہے اور پھر ان مراحل کو ترتیب وار انجام دینے کے لیے کہتی ہے۔
- **سیلف ریفائن**، یہ تکنیک LLM کے آؤٹ پٹ پر تنقید کرنے اور پھر اسے بہتر بنانے کے لیے کہنے کے بارے میں ہے۔
- **میوٹک پرامپٹنگ**۔ یہاں آپ چاہتے ہیں کہ LLM کا جواب درست ہو اور آپ اس سے جواب کے مختلف حصوں کی وضاحت کرنے کو کہیں۔ یہ سیلف ریفائن کی ایک شکل ہے۔

### زیرو شاٹ پرامپٹنگ

پرامپٹنگ کا یہ انداز بہت آسان ہے، یہ ایک واحد پرامپٹ پر مشتمل ہے۔ یہ تکنیک شاید وہ ہے جسے آپ LLMs کے بارے میں سیکھنا شروع کرتے وقت استعمال کر رہے ہیں۔ یہاں ایک مثال ہے:

- پرامپٹ: "الجبرہ کیا ہے؟"
- جواب: "الجبرہ ریاضی کی ایک شاخ ہے جو ریاضی کے علامتوں اور ان علامتوں کو جوڑنے کے اصولوں کا مطالعہ کرتی ہے۔"

### فیوشاٹ پرامپٹنگ

پرامپٹنگ کا یہ انداز ماڈل کو کچھ مثالیں فراہم کرکے مدد کرتا ہے، ساتھ ہی درخواست کے ساتھ۔ یہ ایک واحد پرامپٹ پر مشتمل ہوتا ہے جس میں اضافی ٹاسک مخصوص ڈیٹا ہوتا ہے۔ یہاں ایک مثال ہے:

- پرامپٹ: "شیکسپیئر کے انداز میں ایک نظم لکھیں۔ یہاں شیکسپیئرین سونٹس کی چند مثالیں ہیں:
  سونٹ 18: 'کیا میں تمہیں گرمی کے دن سے موازنہ کروں؟ تم زیادہ خوبصورت اور زیادہ معتدل ہو...'
  سونٹ 116: 'سچے ذہنوں کی شادی میں رکاوٹیں نہ ہونے دیں۔ محبت محبت نہیں ہے جو تبدیلی کے وقت بدل جائے...'
  سونٹ 132: 'تمہاری آنکھیں مجھے پسند ہیں، اور وہ، جیسے مجھے ترس کھاتے ہیں، جانتے ہیں کہ تمہارا دل مجھے حقارت سے اذیت دیتا ہے،...'
  اب، چاند کی خوبصورتی کے بارے میں ایک سونٹ لکھیں۔"
- جواب: "آسمان پر، چاند نرم روشنی میں چمکتا ہے، چاندنی جو اپنی نرم خوبصورتی کو ظاہر کرتی ہے،..."

مثالیں LLM کو مطلوبہ آؤٹ پٹ کے سیاق و سباق، فارمیٹ یا انداز فراہم کرتی ہیں۔ وہ ماڈل کو مخصوص کام کو سمجھنے اور زیادہ درست اور متعلقہ جوابات پیدا کرنے میں مدد کرتے ہیں۔

### چین آف تھوٹ

چین آف تھوٹ ایک بہت دلچسپ تکنیک ہے کیونکہ یہ LLM کو مراحل کی ایک سیریز کے ذریعے لے جانے کے بارے میں ہے۔ خیال یہ ہے کہ LLM کو اس طرح ہدایت دی جائے کہ وہ کچھ کرنے کا طریقہ سمجھ سکے۔ درج ذیل مثال پر غور کریں، چین آف تھوٹ کے ساتھ اور بغیر:

    - پرامپٹ: "ایلس کے پاس 5 سیب ہیں، وہ 3 سیب پھینکتی ہے، 2 باب کو دیتی ہے اور باب ایک واپس دیتا ہے، ایلس کے پاس کتنے سیب ہیں؟"
    - جواب: 5

LLM 5 کے ساتھ جواب دیتا ہے، جو غلط ہے۔ صحیح جواب 1 سیب ہے، دی گئی حساب کے مطابق (5 -3 -2 + 1 = 1)۔

تو ہم LLM کو یہ صحیح طریقے سے کیسے سکھا سکتے ہیں؟

آئیے چین آف تھوٹ آزمائیں۔ چین آف تھوٹ کو لاگو کرنے کا مطلب ہے:

1. LLM کو ایک مشابہ مثال دیں۔
1. حساب دکھائیں، اور اسے صحیح طریقے سے کیسے حساب کریں۔
1. اصل پرامپٹ فراہم کریں۔

یہاں ہے:

- پرامپٹ: "لیزا کے پاس 7 سیب ہیں، وہ 1 سیب پھینکتی ہے، 4 سیب بارٹ کو دیتی ہے اور بارٹ ایک واپس دیتا ہے:
  7 -1 = 6
  6 -4 = 2
  2 +1 = 3  
  ایلس کے پاس 5 سیب ہیں، وہ 3 سیب پھینکتی ہے، 2 باب کو دیتی ہے اور باب ایک واپس دیتا ہے، ایلس کے پاس کتنے سیب ہیں؟"
  جواب: 1

نوٹ کریں کہ ہم نے کافی لمبے پرامپٹس لکھے ہیں، ایک اور مثال، ایک حساب اور پھر اصل پرامپٹ دیا ہے اور ہم صحیح جواب 1 پر پہنچے ہیں۔

جیسا کہ آپ دیکھ سکتے ہیں، چین آف تھوٹ ایک بہت طاقتور تکنیک ہے۔

### جنریٹڈ نالج

بہت بار جب آپ پرامپٹ بنانا چاہتے ہیں، تو آپ یہ اپنی کمپنی کے ڈیٹا کا استعمال کرتے ہوئے کرنا چاہتے ہیں۔ آپ چاہتے ہیں کہ پرامپٹ کا ایک حصہ کمپنی سے ہو اور دوسرا حصہ وہ اصل پرامپٹ ہو جس میں آپ دلچسپی رکھتے ہیں۔

ایک مثال کے طور پر، اگر آپ انشورنس کے کاروبار میں ہیں تو آپ کا پرامپٹ اس طرح نظر آ سکتا ہے:

```text
{{company}}: {{company_name}}
{{products}}:
{{products_list}}
Please suggest an insurance given the following budget and requirements:
Budget: {{budget}}
Requirements: {{requirements}}
```

اوپر، آپ دیکھتے ہیں کہ پرامپٹ ایک ٹیمپلیٹ کا استعمال کرتے ہوئے بنایا گیا ہے۔ ٹیمپلیٹ میں کچھ متغیرات ہیں، جنہیں `{{variable}}` کے ذریعے ظاہر کیا گیا ہے، جو کمپنی API سے اصل اقدار کے ساتھ تبدیل کیے جائیں گے۔

یہاں ایک مثال ہے کہ پرامپٹ کیسے نظر آ سکتا ہے جب متغیرات کو آپ کی کمپنی کے مواد سے تبدیل کیا گیا ہو:

```text
Insurance company: ACME Insurance
Insurance products (cost per month):
- Car, cheap, 500 USD
- Car, expensive, 1100 USD
- Home, cheap, 600 USD
- Home, expensive, 1200 USD
- Life, cheap, 100 USD

Please suggest an insurance given the following budget and requirements:
Budget: $1000
Requirements: Car, Home, and Life insurance
```

اس پرامپٹ کو LLM کے ذریعے چلانے سے ایسا جواب ملے گا:

```output
Given the budget and requirements, we suggest the following insurance package from ACME Insurance:
- Car, cheap, 500 USD
- Home, cheap, 600 USD
- Life, cheap, 100 USD
Total cost: $1,200 USD
```

جیسا کہ آپ دیکھ سکتے ہیں، یہ لائف انشورنس کی بھی تجویز دیتا ہے، جو اسے نہیں دینا چاہیے۔ یہ نتیجہ اس بات کی نشاندہی کرتا ہے کہ ہمیں پرامپٹ کو واضح کرنے کے لیے تبدیل کرکے پرامپٹ کو بہتر بنانے کی ضرورت ہے۔ کچھ _آزمائش اور غلطی_ کے بعد، ہم درج ذیل پرامپٹ پر پہنچتے ہیں:

```text
Insurance company: ACME Insurance
Insurance products (cost per month):
- type: Car, cheap, cost: 500 USD
- type: Car, expensive, cost: 1100 USD
- type: Home, cheap, cost: 600 USD
- type: Home, expensive, cost: 1200 USD
- type: Life, cheap, cost: 100 USD

Please suggest an insurance given the following budget and requirements:
Budget: $1000 restrict choice to types: Car, Home
```

نوٹ کریں کہ _ٹائپ_ اور _کوسٹ_ شامل کرنے اور کلیدی لفظ _ریسٹرکٹ_ استعمال کرنے سے LLM کو یہ سمجھنے میں مدد ملتی ہے کہ ہم کیا چاہتے ہیں۔

اب ہمیں درج ذیل جواب ملتا ہے:

```output
Given the budget and requirements, we suggest the Car, Cheap insurance product which costs 500 USD per month.
```

اس مثال کا مقصد یہ دکھانا تھا کہ حالانکہ ہم ایک بنیادی تکنیک جیسے _جنریٹڈ نالج_ استعمال کر رہے ہیں، ہمیں مطلوبہ نتیجہ حاصل کرنے کے لیے زیادہ تر معاملات میں پرامپٹ کو بہتر بنانے کی ضرورت ہوتی ہے۔

### لیسٹ ٹو موسٹ

لیسٹ ٹو موسٹ پرامپٹنگ کا خیال ایک بڑے مسئلے کو ذیلی مسائل میں تقسیم کرنا ہے۔ اس طرح، آپ LLM کو رہنمائی کرتے ہیں کہ بڑے مسئلے کو کیسے "فتح" کیا جائے۔ ایک اچھا مثال ڈیٹا سائنس کے لیے ہو سکتا ہے جہاں آپ LLM سے اس طرح مسئلے کو تقسیم کرنے کے لیے کہہ سکتے ہیں:

> پرامپٹ: ڈیٹا سائنس کو 5 مراحل میں کیسے انجام دیا جائے؟

آپ کا AI اسسٹنٹ اس طرح جواب دے گا:

1. ڈیٹا جمع کریں
1. ڈیٹا صاف کریں
1. ڈیٹا کا تجزیہ کریں
1. ڈیٹا کا پلاٹ بنائیں
1. ڈیٹا پیش کریں

### سیلف ریفائن، نتائج پر تنقید کریں

جنریٹو AI اور LLMs کے ساتھ، آپ آؤٹپٹ پر بھروسہ نہیں کر سکتے۔ آپ کو اسے تصدیق کرنے کی ضرورت ہے۔ آخرکار، LLM آپ کو صرف وہی پیش کر رہا ہے جو کہنے کے لیے سب سے زیادہ ممکنہ چیز ہے، نہ کہ جو درست ہے۔ لہذا، ایک اچھا خیال یہ ہے کہ LLM سے خود پر تنقید کرنے کو کہا جائے، جو ہمیں سیلف ریفائن تکنیک کی طرف لے جاتا ہے۔

یہ کیسے کام کرتا ہے یہ ہے کہ آپ درج ذیل مراحل پر عمل کریں:

1. ابتدائی پرامپٹ جو LLM سے مسئلہ حل کرنے کو کہتا ہے
1. LLM جواب دیتا ہے
1. آپ جواب پر تنقید کرتے ہیں اور AI سے اسے بہتر بنانے کو کہتے ہیں
1. LLM دوبارہ جواب دیتا ہے، اس بار تنقید کو مدنظر رکھتے ہوئے اور تجویز کردہ حل پیش کرتا ہے

آپ اس عمل کو جتنی بار چاہیں دہرا سکتے ہیں۔

یہاں ایک مثال ہے جو اس تکنیک کا استعمال کرتی ہے:

> پرامپٹ: "پروڈکٹس اور کسٹمرز کے راستوں کے ساتھ ایک Python Web API بنائیں"

AI جواب:

```python
import flask
app = Flask(__name__)

@app.route('/products')
def products():
    return 'Products'

@app.route('/customers')
def customers():
    return 'Customers'
```

> پرامپٹ: اوپر دیے گئے کوڈ میں 3 بہتریاں تجویز کریں

AI جواب:

```text
Sure, here are three suggestions to improve the code:

Import the correct module: The first line should import Flask instead of flask. The correct import statement should be from flask import Flask.

Add a main function: Add a if __name__ == '__main__': block to the end of the file to run the application when the file is executed.

Use f-strings: Use f-strings to format the return statements in the route functions. For example, return 'Products' can be changed to return f'This is the {request.path} page'.
```

```python
from flask import Flask, request

app = Flask(__name__)

@app.route('/products')
def products():
    return f'This is the {request.path} page'

@app.route('/customers')
def customers():
    return f'This is the {request.path} page'

if __name__ == '__main__':
    app.run()
```

جیسا کہ آپ دیکھ سکتے ہیں، اوپر AI جواب نے پہلی تجویز کردہ کوڈ کو بہتر بنایا ہے، پہلی جواب پر تنقید کی بدولت۔

### میوٹک پرامپٹنگ

میوٹک پرامپٹنگ ایک تکنیک ہے جو سیلف ریفائن سے ملتی جلتی ہے لیکن یہ زیادہ تر LLM سے خود کو وضاحت کرنے کو کہنے کے بارے میں ہے۔ مقصد LLM کے آؤٹپٹ میں تضادات کو کم کرنا ہے تاکہ یہ یقینی بنایا جا سکے کہ یہ درست جواب پر پہنچے۔ عمل کی پیروی کرنے کے لیے ورک فلو یہ ہے:

1. LLM سے سوال کا جواب دینے کو کہیں
1. جواب کے ہر حصے کے لیے، LLM سے اس کی مزید تفصیل سے وضاحت کرنے کو کہیں۔
1. اگر تضادات ہیں، تو ان حصوں کو مسترد کریں جو متضاد ہیں۔

2 اور 3 کو اس وقت تک دہرائیں جب تک کہ آپ تمام حصوں سے گزر نہ جائیں اور آپ جواب سے مطمئن نہ ہوں۔

یہاں ایک مثال پرامپٹ ہے:

> پرامپٹ: میں وبا کو کم کرنے کے لیے بحران کا منصوبہ 5 مراحل میں کیسے بنا سکتا ہوں؟
> LLM جواب:

```text
1. Identify the risks
1. Identify the stakeholders
1. Identify the resources
1. Identify the actions
1. Identify the communication channels
```

اس نے 5 مراحل کی نشاندہی کی ہے، لیکن کیا ہم یہ تعین کر سکتے ہیں کہ یہ درست ہے؟ آئیے LLM سے ہر مرحلے کی وضاحت کرنے کو کہیں:

> پرامپٹ: پہلے مرحلے کی مزید تفصیل سے وضاحت کریں، وبا کے ساتھ تفصیل سے خطرات کیا ہیں؟

```text
The risks are the following:

- Loss of life
- Loss of business
- Loss of reputation
- Loss of customers
- Loss of employees
```

اس وقت، ہم یہ یقینی بنانا چاہتے ہیں کہ LLM درست ہے، لہذا ہم اس سے پہلے خطرے کی مزید تفصیل سے وضاحت کرنے کو کہتے ہیں اور امید کرتے ہیں کہ یہ اوپر دیے گئے جواب کے ساتھ مستقل ہے:

> پرامپٹ: وبا میں، سب سے بڑا خطرہ کیا ہے اور کیوں؟

```text
The biggest risk is loss of life because it's the most important thing to protect.
```

> وبا میں دو سب سے بڑے خطرات کیا ہیں؟

```text
The two biggest risks are loss of life and loss of business.
```

اس وقت، LLM مستقل ہے اور "زندگی" اور "کاروبار" کو دو سب سے بڑے خطرات کے طور پر ذکر کرتا ہے۔ ہم اب اگلے مرحلے پر جا سکتے ہیں اور کافی حد تک پراعتماد محسوس کر سکتے ہیں۔ تاہم، ہمیں LLM پر اندھا اعتماد نہیں کرنا چاہیے، ہمیں ہمیشہ آؤٹپٹ کی تصدیق کرنی چاہیے۔

## اپنے آؤٹپٹ کو مختلف کریں

LLMs فطری طور پر غیر متعین ہیں، یعنی آپ کو ہر بار ایک ہی پرامپٹ چلانے پر مختلف نتائج ملیں گے۔ درج ذیل پرامپٹ کو آزمائیں:

> "Python Web API کے لیے کوڈ تیار کریں"

```python
# Import necessary modules
import flask
from flask import request, jsonify

# Create a Flask app
app = flask.Flask(__name__)

# Create a route for the API
@app.route('/api', methods=['GET'])
def api():
    # Get the data from the request
    data = request.args

    # Process the data
    result = process_data(data)

    # Return the result as JSON
    return jsonify(result)

# Function to process the data
def process_data(data):
    # Do something with the data
    result = data + 1

    # Return the result
    return result

# Run the app
if __name__ == '__main__':
    app.run()

```

ایک ہی پرامپٹ کو دوبارہ چلانے سے تھوڑا مختلف جواب پیدا ہوتا ہے:

```python
#import necessary packages
import flask
from flask import request, jsonify

#create the Flask application
app = flask.Flask(__name__)
app.config["DEBUG"] = True

#create a list of books
books = [
    {'id': 0,
     'title': 'A Fire Upon the Deep',
     'author': 'Vernor Vinge',
     'first_sentence': 'The coldsleep itself was dreamless.',
     'year_published': '1992'},
    {'id': 1,
     'title': 'The Ones Who Walk Away From Omelas',
     'author': 'Ursula K. Le Guin',
     'first_sentence': 'With a clamor of bells that set the swallows soaring, the Festival of Summer came to the city Omelas, bright-towered by the sea.',
     'published': '1973'},
    {'id': 2,
     'title': 'Dhalgren',
     'author': 'Samuel R. Delany',
     'first_sentence': 'to wound the autumnal city.',
     'published': '1975'}
]

#create an endpoint for the API
@app.route('/', methods=['GET'])
def home():
    return '''<h1>Books API</h1>
<p>A prototype API for retrieving books.</p>'''

#create an endpoint to return all books
@app.route('/api/v1/resources/books/all', methods=['GET'])
def api_all():
    return jsonify(books)

#create an endpoint to return a single book
@app.route('/api/v1/resources/books', methods=['GET'])
def api_id():
    #check if an ID was provided as part of the URL
    #if ID is provided, assign it to a variable
    #if no ID is provided, display an error
    if 'id' in request.args:
        id = int(request.args['id'])
    else:
        return "Error: No id field provided. Please specify an id."

    #create an empty list for our results
    results = []

    #loop through the data and match results that fit the requested ID
    #IDs are unique, but other fields might return many results
    for book in books:
        if book['id'] == id:
            results.append(book)

    #use the jsonify function from Flask to convert our list of
    #Python dictionaries to the JSON format
    return jsonify(results)

app.run()
```

> تو کیا مختلف آؤٹپٹ ایک مسئلہ ہے؟

یہ اس بات پر منحصر ہے کہ آپ کیا کرنے کی کوشش کر رہے ہیں۔ اگر آپ کو ایک مخصوص جواب چاہیے تو یہ مسئلہ ہے۔ اگر آپ "جغرافیہ پر کوئی 3 سوالات تیار کریں" جیسے مختلف آؤٹپٹ کے ساتھ ٹھیک ہیں، تو یہ مسئلہ نہیں ہے۔

### اپنے آؤٹپٹ کو مختلف کرنے کے لیے درجہ حرارت کا استعمال

ٹھیک ہے، تو ہم نے فیصلہ کیا ہے کہ ہم آؤٹپٹ کو زیادہ پیش گوئی کے قابل بنانا چاہتے ہیں، یعنی زیادہ متعین۔ ہم یہ کیسے کرتے ہیں؟

درجہ حرارت 0 اور 1 کے درمیان ایک قدر ہے، جہاں 0 سب سے زیادہ متعین ہے اور 1 سب سے زیادہ مختلف ہے۔ ڈیفالٹ قدر 0.7 ہے۔ آئیے دیکھتے ہیں کہ جب درجہ حرارت کو 0.1 پر سیٹ کیا جاتا ہے تو کیا ہوتا ہے:

> "Python Web API کے لیے کوڈ تیار کریں"

```python
#import necessary libraries
import flask
from flask import request, jsonify

#create an instance of the Flask class
app = flask.Flask(__name__)

#create an endpoint for the API
@app.route('/api/v1/endpoint', methods=['GET'])
def api_endpoint():
    #get the request data
    data = request.get_json()

    #process the data
    result = process_data(data)

    #return the result
    return jsonify(result)

#function to process the data
def process_data(data):
    #process the data
    result = {'result': 'success'}

    #return the result
    return result

#run the Flask app
if __name__ == '__main__':
    app.run()

```

پرامپٹ کو دوبارہ چلانے سے ہمیں یہ نتیجہ ملتا ہے:

```python
#import necessary libraries
import flask
from flask import request, jsonify

#create a Flask app
app = flask.Flask(__name__)

#create a route for the API
@app.route('/api', methods=['GET'])
def api_call():
    #get the data from the request
    data = request.get_json()

    #process the data
    result = process_data(data)

    #return the result
    return jsonify(result)

#define the process_data function
def process_data(data):
    #do something with the data
    result = data + 1

    #return the result
    return result

#run the app
if __name__ == '__main__':
    app.run()

```

ان دو آؤٹپٹس کے درمیان صرف ایک معمولی فرق ہے۔ اس بار، آئیے اس کے برعکس کریں، آئیے درجہ حرارت کو 0.9 پر سیٹ کریں:

```python
# Import necessary libraries
import flask
from flask import request, jsonify

# Create a Flask app
app = flask.Flask(__name__)

# Create a route for the API
@app.route('/api', methods=['GET'])
def api_call():
    # Get the data from the request
    data = request.args

    # Process the data
    result = process_data(data)

    # Return the result
    return jsonify(result)

# Function to process the data
def process_data(data):
    # Do something with the data
    result = data + 1

    # Return the result
    return result

# Run the app
if __name__ == '__main__':
    app.run()

```

اور درجہ حرارت کی قدر کو 0.9 پر سیٹ کرنے کی دوسری کوشش:

```python
import flask
from flask import request, jsonify

# create the Flask app
app = flask.Flask(__name__)
app.config['DEBUG'] = True

# create some test data
books = [
    {'id': 0, 'title': 'A Fire Upon The Deep', 'author': 'Vernor Vinge', 'first_sentence': 'The coldsleep itself was dreamless.', 'year_published': '1992'},
    {'id': 1, 'title': 'The Ones Who Walk Away From Omelas', 'author': 'Ursula K. Le Guin', 'first_sentence': 'With a clamor of bells that set the swallows soaring, the Festival of Summer came to the city Omelas, bright-towered by the sea.', 'published': '1973'},
    {'id': 2, 'title': 'Dhalgren', 'author': 'Samuel R. Delany', 'first_sentence': 'to wound the autumnal city.', 'published': '1975'}
]

# create an endpoint
@app.route('/', methods=['GET'])
def home():
    return '''<h1>Welcome to our book API!</h1>'''

@app.route('/api/v1/resources/books

```

جیسا کہ آپ دیکھ سکتے ہیں، نتائج زیادہ مختلف نہیں ہو سکتے تھے۔

> نوٹ کریں کہ اور بھی پیرامیٹرز ہیں جنہیں آپ آؤٹ پٹ کو مختلف کرنے کے لیے تبدیل کر سکتے ہیں، جیسے top-k، top-p، repetition penalty، length penalty اور diversity penalty، لیکن یہ اس نصاب کے دائرہ کار سے باہر ہیں۔

## بہترین طریقے

ایسے کئی طریقے ہیں جنہیں آپ استعمال کر سکتے ہیں تاکہ مطلوبہ نتائج حاصل کر سکیں۔ جیسے جیسے آپ پرامپٹنگ کو زیادہ استعمال کریں گے، آپ اپنا انداز خود تلاش کریں گے۔

ان تکنیکوں کے علاوہ جن پر ہم نے بات کی ہے، کچھ بہترین طریقے ہیں جنہیں LLM کو پرامپٹ کرتے وقت مدنظر رکھنا چاہیے۔

یہاں کچھ بہترین طریقے ہیں جنہیں مدنظر رکھنا چاہیے:

- **سیاق و سباق کی وضاحت کریں**۔ سیاق و سباق اہم ہے، جتنا زیادہ آپ وضاحت کر سکتے ہیں جیسے کہ ڈومین، موضوع وغیرہ، اتنا ہی بہتر ہوگا۔
- آؤٹ پٹ کو محدود کریں۔ اگر آپ کو مخصوص تعداد میں آئٹمز یا مخصوص لمبائی چاہیے، تو اسے واضح کریں۔
- **کیا اور کیسے دونوں کی وضاحت کریں**۔ یاد رکھیں کہ آپ کو یہ بتانا ہے کہ آپ کیا چاہتے ہیں اور کیسے چاہتے ہیں، مثال کے طور پر "ایک Python Web API بنائیں جس میں routes products اور customers ہوں، اسے 3 فائلوں میں تقسیم کریں"۔
- **ٹیمپلیٹس استعمال کریں**۔ اکثر، آپ اپنی کمپنی کے ڈیٹا کے ساتھ اپنے پرامپٹس کو بہتر بنانا چاہیں گے۔ ایسا کرنے کے لیے ٹیمپلیٹس استعمال کریں۔ ٹیمپلیٹس میں متغیرات ہو سکتے ہیں جنہیں آپ اصل ڈیٹا کے ساتھ تبدیل کرتے ہیں۔
- **صحیح ہجے کریں**۔ LLMs آپ کو درست جواب دے سکتے ہیں، لیکن اگر آپ صحیح ہجے کریں گے تو آپ کو بہتر جواب ملے گا۔

## اسائنمنٹ

یہاں Python میں کوڈ ہے جو Flask استعمال کرتے ہوئے ایک سادہ API بنانے کا طریقہ دکھاتا ہے:

```python
from flask import Flask, request

app = Flask(__name__)

@app.route('/')
def hello():
    name = request.args.get('name', 'World')
    return f'Hello, {name}!'

if __name__ == '__main__':
    app.run()
```

GitHub Copilot یا ChatGPT جیسے AI اسسٹنٹ کا استعمال کریں اور "self-refine" تکنیک کو کوڈ کو بہتر بنانے کے لیے اپلائی کریں۔

## حل

براہ کرم اسائنمنٹ کو حل کرنے کی کوشش کریں اور کوڈ میں مناسب پرامپٹس شامل کریں۔

> [!TIP]
> پرامپٹ کو اس طرح ترتیب دیں کہ وہ بہتری کے لیے کہے، یہ ایک اچھا خیال ہے کہ آپ بہتری کی تعداد کو محدود کریں۔ آپ یہ بھی کہہ سکتے ہیں کہ اسے کسی خاص طریقے سے بہتر بنائیں، جیسے کہ آرکیٹیکچر، کارکردگی، سیکیورٹی وغیرہ۔

[حل](../../../05-advanced-prompts/python/aoai-solution.py)

## علم کی جانچ

میں chain-of-thought پرامپٹنگ کیوں استعمال کروں گا؟ مجھے 1 درست جواب اور 2 غلط جوابات دکھائیں۔

1. LLM کو مسئلہ حل کرنے کا طریقہ سکھانے کے لیے۔
1. B، LLM کو کوڈ میں غلطیاں تلاش کرنے کا طریقہ سکھانے کے لیے۔
1. C، LLM کو مختلف حل پیش کرنے کی ہدایت دینے کے لیے۔

A: 1، کیونکہ chain-of-thought کا مطلب ہے کہ LLM کو مسئلہ حل کرنے کا طریقہ دکھایا جائے، اسے مراحل کے ساتھ فراہم کر کے، اور اسی طرح کے مسائل اور ان کے حل کے طریقے۔

## 🚀 چیلنج

آپ نے ابھی اسائنمنٹ میں self-refine تکنیک استعمال کی۔ کوئی بھی پروگرام لیں جو آپ نے بنایا ہو اور غور کریں کہ آپ اس میں کون سی بہتری لانا چاہتے ہیں۔ اب self-refine تکنیک کا استعمال کرتے ہوئے تجویز کردہ تبدیلیاں اپلائی کریں۔ آپ نے نتیجہ کے بارے میں کیا سوچا، بہتر یا بدتر؟

## شاندار کام! اپنی تعلیم جاری رکھیں

اس سبق کو مکمل کرنے کے بعد، ہماری [Generative AI Learning collection](https://aka.ms/genai-collection?WT.mc_id=academic-105485-koreyst) کو دیکھیں تاکہ اپنی Generative AI کی معلومات کو مزید بہتر کریں!

سبق 6 پر جائیں جہاں ہم پرامپٹ انجینئرنگ کے علم کو [text generation apps بنانے](../06-text-generation-apps/README.md?WT.mc_id=academic-105485-koreyst) کے ذریعے اپلائی کریں گے۔

---

**اعلانِ لاتعلقی**:  
یہ دستاویز AI ترجمہ سروس [Co-op Translator](https://github.com/Azure/co-op-translator) کا استعمال کرتے ہوئے ترجمہ کی گئی ہے۔ ہم درستگی کے لیے کوشش کرتے ہیں، لیکن براہ کرم آگاہ رہیں کہ خودکار ترجمے میں غلطیاں یا غیر درستیاں ہو سکتی ہیں۔ اصل دستاویز کو اس کی اصل زبان میں مستند ذریعہ سمجھا جانا چاہیے۔ اہم معلومات کے لیے، پیشہ ور انسانی ترجمہ کی سفارش کی جاتی ہے۔ اس ترجمے کے استعمال سے پیدا ہونے والی کسی بھی غلط فہمی یا غلط تشریح کے لیے ہم ذمہ دار نہیں ہیں۔