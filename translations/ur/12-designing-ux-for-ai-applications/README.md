<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "ec385b41ee50579025d50cc03bfb3a25",
  "translation_date": "2025-07-09T14:50:22+00:00",
  "source_file": "12-designing-ux-for-ai-applications/README.md",
  "language_code": "ur"
}
-->
# AI ایپلیکیشنز کے لیے UX ڈیزائن کرنا

[![Designing UX for AI Applications](../../../translated_images/12-lesson-banner.c53c3c7c802e8f563953ce388f6a987ca493472c724d924b060be470951c53c8.ur.png)](https://aka.ms/gen-ai-lesson12-gh?WT.mc_id=academic-105485-koreyst)

> _(اس سبق کی ویڈیو دیکھنے کے لیے اوپر تصویر پر کلک کریں)_

یوزر ایکسپیرینس ایپ بنانے کا ایک بہت اہم پہلو ہے۔ صارفین کو آپ کی ایپ کو مؤثر طریقے سے استعمال کرنا چاہیے تاکہ وہ اپنے کام انجام دے سکیں۔ مؤثر ہونا ایک بات ہے، لیکن آپ کو ایسی ایپس بھی ڈیزائن کرنی ہوتی ہیں جو ہر کسی کے لیے قابلِ رسائی ہوں۔ یہ باب اسی موضوع پر توجہ دے گا تاکہ آپ ایسی ایپ ڈیزائن کریں جو لوگ استعمال کرنا چاہیں اور کر سکیں۔

## تعارف

یوزر ایکسپیرینس اس بات کو کہتے ہیں کہ صارف کسی مخصوص پروڈکٹ یا سروس کے ساتھ کیسے تعامل کرتا ہے، چاہے وہ کوئی سسٹم، ٹول یا ڈیزائن ہو۔ AI ایپلیکیشنز تیار کرتے وقت، ڈویلپرز نہ صرف اس بات پر توجہ دیتے ہیں کہ یوزر ایکسپیرینس مؤثر ہو بلکہ یہ بھی یقینی بناتے ہیں کہ یہ اخلاقی ہو۔ اس سبق میں ہم یہ سیکھیں گے کہ کیسے ایسی AI ایپلیکیشنز بنائی جائیں جو صارفین کی ضروریات کو پورا کریں۔

سبق میں درج ذیل موضوعات شامل ہوں گے:

- یوزر ایکسپیرینس کا تعارف اور صارف کی ضروریات کو سمجھنا  
- AI ایپلیکیشنز کو اعتماد اور شفافیت کے لیے ڈیزائن کرنا  
- AI ایپلیکیشنز کو تعاون اور فیڈبیک کے لیے ڈیزائن کرنا  

## سیکھنے کے مقاصد

اس سبق کے بعد آپ قابل ہوں گے کہ:

- AI ایپلیکیشنز بنائیں جو صارف کی ضروریات کو پورا کریں۔  
- AI ایپلیکیشنز ڈیزائن کریں جو اعتماد اور تعاون کو فروغ دیں۔  

### پیشگی معلومات

کچھ وقت نکال کر [یوزر ایکسپیرینس اور ڈیزائن تھنکنگ](https://learn.microsoft.com/training/modules/ux-design?WT.mc_id=academic-105485-koreyst) کے بارے میں مزید پڑھیں۔

## یوزر ایکسپیرینس کا تعارف اور صارف کی ضروریات کو سمجھنا

ہماری فرضی تعلیمی اسٹارٹ اپ میں دو بنیادی صارفین ہیں: اساتذہ اور طلباء۔ ہر صارف کی منفرد ضروریات ہوتی ہیں۔ یوزر سینٹرڈ ڈیزائن صارف کو ترجیح دیتا ہے تاکہ پروڈکٹس ان کے لیے متعلقہ اور فائدہ مند ہوں جن کے لیے وہ بنائی گئی ہیں۔

ایپلیکیشن کو **مفید، قابلِ اعتماد، قابلِ رسائی اور خوشگوار** ہونا چاہیے تاکہ اچھا یوزر ایکسپیرینس فراہم کیا جا سکے۔

### استعمال کی آسانی

مفید ہونے کا مطلب ہے کہ ایپلیکیشن میں وہ فیچرز ہوں جو اس کے مقصد کے مطابق ہوں، جیسے گریڈنگ کے عمل کو خودکار بنانا یا ریویژن کے لیے فلیش کارڈز تیار کرنا۔ ایک ایسی ایپ جو گریڈنگ خودکار کرتی ہے، اسے طلباء کے کام کو درست اور مؤثر طریقے سے اسکور کرنا چاہیے۔ اسی طرح، ریویژن فلیش کارڈز بنانے والی ایپ کو متعلقہ اور متنوع سوالات تیار کرنے چاہئیں۔

### قابلِ اعتماد ہونا

قابلِ اعتماد ہونے کا مطلب ہے کہ ایپلیکیشن اپنا کام مستقل اور بغیر غلطی کے انجام دے۔ تاہم، AI بھی انسانوں کی طرح کامل نہیں ہوتا اور غلطیوں کا امکان ہوتا ہے۔ ایپلیکیشنز کو ایسی صورتحال کا سامنا ہو سکتا ہے جہاں انسانی مداخلت یا اصلاح کی ضرورت ہو۔ آپ غلطیوں کو کیسے سنبھالتے ہیں؟ اس سبق کے آخری حصے میں ہم دیکھیں گے کہ AI سسٹمز اور ایپلیکیشنز کو تعاون اور فیڈبیک کے لیے کیسے ڈیزائن کیا جاتا ہے۔

### قابلِ رسائی ہونا

قابلِ رسائی ہونے کا مطلب ہے کہ یوزر ایکسپیرینس کو مختلف صلاحیتوں کے حامل صارفین تک پہنچایا جائے، بشمول معذور افراد، تاکہ کوئی بھی باہر نہ رہے۔ قابلِ رسائی رہنما اصولوں اور اصولوں کی پیروی سے AI حل زیادہ جامع، قابلِ استعمال اور تمام صارفین کے لیے فائدہ مند بن جاتے ہیں۔

### خوشگوار ہونا

خوشگوار ہونے کا مطلب ہے کہ ایپلیکیشن استعمال کرنے میں خوشگوار ہو۔ ایک پرکشش یوزر ایکسپیرینس صارف پر مثبت اثر ڈال سکتی ہے، انہیں ایپ پر واپس آنے کی ترغیب دیتی ہے اور کاروباری آمدنی میں اضافہ کرتی ہے۔

![AI میں UX کے پہلوؤں کی وضاحت کرتی ہوئی تصویر](../../../translated_images/uxinai.d5b4ed690f5cefff0c53ffcc01b480cdc1828402e1fdbc980490013a3c50935a.ur.png)

ہر مسئلہ AI سے حل نہیں کیا جا سکتا۔ AI آپ کے یوزر ایکسپیرینس کو بہتر بنانے کے لیے آتا ہے، چاہے وہ دستی کاموں کو خودکار بنانا ہو یا یوزر ایکسپیرینس کو ذاتی نوعیت دینا ہو۔

## AI ایپلیکیشنز کو اعتماد اور شفافیت کے لیے ڈیزائن کرنا

اعتماد قائم کرنا AI ایپلیکیشنز کے ڈیزائن میں بہت اہم ہے۔ اعتماد اس بات کو یقینی بناتا ہے کہ صارف کو یقین ہو کہ ایپ کام مکمل کرے گی، نتائج مستقل طور پر فراہم کرے گی اور نتائج وہی ہوں گے جو صارف چاہتا ہے۔ اس شعبے میں خطرہ mistrust اور overtrust کا ہوتا ہے۔ mistrust اس وقت ہوتا ہے جب صارف AI سسٹم پر کم یا کوئی اعتماد نہیں کرتا، جس کی وجہ سے وہ آپ کی ایپ کو مسترد کر دیتا ہے۔ overtrust اس وقت ہوتا ہے جب صارف AI سسٹم کی صلاحیت کو زیادہ سمجھتا ہے، جس سے صارف AI پر حد سے زیادہ اعتماد کر لیتا ہے۔ مثال کے طور پر، ایک خودکار گریڈنگ سسٹم میں overtrust کی صورت میں استاد کچھ پیپرز کو چیک نہیں کرتا کہ گریڈنگ سسٹم صحیح کام کر رہا ہے یا نہیں۔ اس سے طلباء کو غیر منصفانہ یا غلط گریڈز مل سکتے ہیں، یا فیڈبیک اور بہتری کے مواقع ضائع ہو سکتے ہیں۔

اعتماد کو ڈیزائن کے مرکز میں رکھنے کے دو طریقے explainability اور control ہیں۔

### Explainability

جب AI فیصلے کرنے میں مدد دیتا ہے، جیسے کہ آنے والی نسلوں کو علم منتقل کرنا، تو اساتذہ اور والدین کے لیے یہ سمجھنا ضروری ہوتا ہے کہ AI فیصلے کیسے کیے جاتے ہیں۔ یہی explainability ہے — یہ سمجھنا کہ AI ایپلیکیشنز فیصلے کیسے کرتی ہیں۔ explainability کے لیے ڈیزائن میں AI ایپلیکیشن کی صلاحیتوں کی مثالیں شامل کرنا ضروری ہے۔ مثال کے طور پر، "Get started with AI teacher" کی بجائے نظام کہہ سکتا ہے: "اپنے نوٹس کو آسان ریویژن کے لیے AI کی مدد سے خلاصہ کریں۔"

![AI ایپلیکیشنز میں explainability کی واضح مثال کے ساتھ ایپ کا لینڈنگ پیج](../../../translated_images/explanability-in-ai.134426a96b498fbfdc80c75ae0090aedc0fc97424ae0734fccf7fb00a59a20d9.ur.png)

ایک اور مثال یہ ہے کہ AI صارف اور ذاتی ڈیٹا کو کیسے استعمال کرتا ہے۔ مثال کے طور پر، ایک صارف جس کا persona student ہے، اس کی کچھ حدود ہو سکتی ہیں۔ AI ممکنہ طور پر سوالات کے جوابات ظاہر نہیں کر سکتا لیکن صارف کو مسئلہ حل کرنے کے طریقے سوچنے میں مدد دے سکتا ہے۔

![persona کی بنیاد پر سوالات کے جواب دیتا ہوا AI](../../../translated_images/solving-questions.b7dea1604de0cbd2e9c5fa00b1a68a0ed77178a035b94b9213196b9d125d0be8.ur.png)

explainability کا آخری اہم حصہ وضاحتوں کو آسان بنانا ہے۔ طلباء اور اساتذہ AI ماہر نہیں ہوتے، اس لیے ایپ کی صلاحیتوں کی وضاحت آسان اور سمجھنے میں آسان ہونی چاہیے۔

![AI کی صلاحیتوں پر آسان وضاحتیں](../../../translated_images/simplified-explanations.4679508a406c3621fa22bad4673e717fbff02f8b8d58afcab8cb6f1aa893a82f.ur.png)

### Control

Generative AI صارف اور AI کے درمیان تعاون پیدا کرتا ہے، جہاں صارف مختلف نتائج کے لیے prompts کو تبدیل کر سکتا ہے۔ مزید برآں، جب کوئی آؤٹ پٹ تیار ہو جائے، تو صارفین کو نتائج میں ترمیم کرنے کی سہولت ہونی چاہیے تاکہ انہیں کنٹرول کا احساس ہو۔ مثال کے طور پر، Bing استعمال کرتے وقت آپ اپنے prompt کو فارمیٹ، انداز اور لمبائی کے لحاظ سے ترتیب دے سکتے ہیں۔ اس کے علاوہ، آپ اپنے آؤٹ پٹ میں تبدیلیاں بھی کر سکتے ہیں جیسا کہ نیچے دکھایا گیا ہے:

![Bing سرچ کے نتائج جن میں prompt اور آؤٹ پٹ کو تبدیل کرنے کے آپشنز ہیں](../../../translated_images/bing1.293ae8527dbe2789b675c8591c9fb3cb1aa2ada75c2877f9aa9edc059f7a8b1c.ur.png)

Bing کی ایک اور خصوصیت جو صارف کو ایپلیکیشن پر کنٹرول دیتی ہے وہ یہ ہے کہ صارف ڈیٹا کے استعمال میں opt-in اور opt-out کر سکتا ہے۔ اسکول کی ایپلیکیشن میں، ایک طالب علم چاہے گا کہ وہ اپنے نوٹس کے ساتھ ساتھ اساتذہ کے وسائل کو بھی ریویژن کے مواد کے طور پر استعمال کرے۔

![Bing سرچ کے نتائج جن میں prompt اور آؤٹ پٹ کو تبدیل کرنے کے آپشنز ہیں](../../../translated_images/bing2.309f4845528a88c28c1c9739fb61d91fd993dc35ebe6fc92c66791fb04fceb4d.ur.png)

> AI ایپلیکیشنز ڈیزائن کرتے وقت، ارادے کا ہونا بہت ضروری ہے تاکہ صارفین AI کی صلاحیتوں کے بارے میں غیر حقیقی توقعات نہ رکھیں۔ اس کا ایک طریقہ یہ ہے کہ prompts اور نتائج کے درمیان کچھ رکاوٹ رکھی جائے، صارف کو یاد دلایا جائے کہ یہ AI ہے، کوئی انسان نہیں۔

## AI ایپلیکیشنز کو تعاون اور فیڈبیک کے لیے ڈیزائن کرنا

جیسا کہ پہلے ذکر کیا گیا، generative AI صارف اور AI کے درمیان تعاون پیدا کرتا ہے۔ زیادہ تر تعاملات میں صارف prompt دیتا ہے اور AI آؤٹ پٹ تیار کرتا ہے۔ اگر آؤٹ پٹ غلط ہو تو کیا ہوتا ہے؟ اگر غلطی ہو جائے تو ایپلیکیشن اسے کیسے سنبھالتی ہے؟ کیا AI صارف کو مورد الزام ٹھہراتا ہے یا غلطی کی وضاحت کرتا ہے؟

AI ایپلیکیشنز کو فیڈبیک لینے اور دینے کے قابل بنایا جانا چاہیے۔ یہ نہ صرف AI سسٹم کو بہتر بناتا ہے بلکہ صارفین کے ساتھ اعتماد بھی قائم کرتا ہے۔ ڈیزائن میں فیڈبیک لوپ شامل ہونا چاہیے، مثال کے طور پر آؤٹ پٹ پر سادہ thumbs up یا down۔

ایک اور طریقہ یہ ہے کہ سسٹم کی صلاحیتوں اور حدود کو واضح طور پر بیان کیا جائے۔ جب صارف AI کی صلاحیتوں سے باہر کچھ مانگتا ہے، تو اس کا بھی کوئی طریقہ ہونا چاہیے جیسا کہ نیچے دکھایا گیا ہے۔

![فیڈبیک دینا اور غلطیوں کو سنبھالنا](../../../translated_images/feedback-loops.7955c134429a94663443ad74d59044f8dc4ce354577f5b79b4bd2533f2cafc6f.ur.png)

سسٹم کی غلطیاں عام ہیں، خاص طور پر ایسی ایپلیکیشنز میں جہاں صارف کو AI کے دائرہ کار سے باہر معلومات کی ضرورت ہو یا ایپلیکیشن پر سوالات/موضوعات کی تعداد محدود ہو۔ مثال کے طور پر، اگر AI ایپلیکیشن صرف تاریخ اور ریاضی کے موضوعات پر تربیت یافتہ ہے، تو وہ جغرافیہ کے سوالات کا جواب نہیں دے سکے گی۔ اس کا حل یہ ہو سکتا ہے کہ AI سسٹم جواب دے: "معذرت، ہمارا پروڈکٹ صرف درج ذیل موضوعات پر تربیت یافتہ ہے.....، میں آپ کے سوال کا جواب نہیں دے سکتا۔"

AI ایپلیکیشنز کامل نہیں ہوتیں، اس لیے وہ غلطیاں کریں گی۔ اپنی ایپلیکیشنز ڈیزائن کرتے وقت، آپ کو صارفین سے فیڈبیک لینے اور غلطیوں کو سنبھالنے کے لیے آسان اور قابلِ فہم طریقے بنانے چاہئیں۔

## اسائنمنٹ

اب تک جو بھی AI ایپس آپ نے بنائی ہیں، ان میں درج ذیل اقدامات پر غور کریں اور انہیں نافذ کرنے کی کوشش کریں:

- **خوشگوار:** سوچیں کہ آپ اپنی ایپ کو کیسے مزید خوشگوار بنا سکتے ہیں۔ کیا آپ ہر جگہ وضاحتیں شامل کر رہے ہیں؟ کیا آپ صارف کو دریافت کرنے کی ترغیب دے رہے ہیں؟ آپ اپنی غلطی کے پیغامات کیسے لکھ رہے ہیں؟  
- **استعمال کی آسانی:** ویب ایپ بنا رہے ہیں۔ یقینی بنائیں کہ آپ کی ایپ ماؤس اور کی بورڈ دونوں سے نیویگیٹ کی جا سکے۔  
- **اعتماد اور شفافیت:** AI اور اس کے نتائج پر مکمل اعتماد نہ کریں، سوچیں کہ آپ کس طرح انسانی تصدیق کو شامل کر سکتے ہیں۔ مزید برآں، اعتماد اور شفافیت حاصل کرنے کے دیگر طریقے بھی نافذ کریں۔  
- **کنٹرول:** صارف کو اس ڈیٹا پر کنٹرول دیں جو وہ ایپلیکیشن کو فراہم کرتا ہے۔ AI ایپلیکیشن میں ڈیٹا کلیکشن کے لیے opt-in اور opt-out کا طریقہ شامل کریں۔  

## اپنی تعلیم جاری رکھیں!

اس سبق کو مکمل کرنے کے بعد، ہمارے [Generative AI Learning collection](https://aka.ms/genai-collection?WT.mc_id=academic-105485-koreyst) کو دیکھیں تاکہ اپنی Generative AI کی معلومات کو مزید بڑھا سکیں!

سبق 13 پر جائیں، جہاں ہم دیکھیں گے کہ [AI ایپلیکیشنز کو کیسے محفوظ بنایا جائے](../13-securing-ai-applications/README.md?WT.mc_id=academic-105485-koreyst)!

**دستخطی دستبرداری**:  
یہ دستاویز AI ترجمہ سروس [Co-op Translator](https://github.com/Azure/co-op-translator) کے ذریعے ترجمہ کی گئی ہے۔ اگرچہ ہم درستگی کے لیے کوشاں ہیں، براہ کرم آگاہ رہیں کہ خودکار ترجمے میں غلطیاں یا عدم درستیاں ہو سکتی ہیں۔ اصل دستاویز اپنی مادری زبان میں ہی معتبر ماخذ سمجھی جانی چاہیے۔ اہم معلومات کے لیے پیشہ ور انسانی ترجمہ کی سفارش کی جاتی ہے۔ اس ترجمے کے استعمال سے پیدا ہونے والی کسی بھی غلط فہمی یا غلط تشریح کی ذمہ داری ہم پر عائد نہیں ہوتی۔