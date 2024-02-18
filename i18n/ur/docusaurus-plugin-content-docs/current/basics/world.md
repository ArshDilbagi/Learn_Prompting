---
sidebar_position: 105
---
# 🟢 اے آئی دماغوں کو سمجھنا


:::takeaways
- AIs کی بہت سی مختلف اقسام ہیں۔
- ایل ایل ایم کے کام کرنے کے طریقے کی بنیادی باتیں
:::


بقیہ کورس میں جانے سے پہلے، مختلف AIs اور ان کے کام کرنے کے بارے میں کچھ بنیادی تصورات کو سمجھنا ضروری ہے۔ یہ بنیادی علم مندرجہ ذیل مواد کی واضح تفہیم فراہم کرے گا۔


## مختلف AIs

مصنوعی ذہانت کا منظر نامہ وسیع اور ٹیکسٹوع ہے [^a]، جس میں ہزاروں، اگر لاکھوں نہیں، تو الگ الگ ماڈلز شامل ہیں۔ یہ ماڈل صلاحیتوں اور ایپلی کیشنز کے ایک وسیع میدان عمل پر فخر کرتے ہیں۔ کچھ تخلیقی ہیں، [images](https://openai.com/product/dall-e-2)، [music](https://google-research.github.io/seanet/musiclm جیسے آؤٹ پٹ بنانے کے لیے انجنیئر کردہ /examples/)، [text](https://platform.openai.com/playground)، اور یہاں تک کہ [ویڈیوز](https://makeavideo.studio/)۔ اس کے برعکس، دوسرے امتیازی ہیں، جو مختلف ان پٹ کے درمیان درجہ بندی یا فرق کرنے کے لیے ڈیزائن کیے گئے ہیں، جیسے کہ بلیوں اور کتوں کے درمیان امتیاز کرنے والا تصویری درجہ بندی۔ تاہم، یہ کورس مکمل طور پر تخلیقی AIs پر توجہ مرکوز کرے گا۔

جنریٹیو AIs میں سے، صرف چند ایک کے پاس جدید صلاحیتیں ہیں جو انہیں پرامپٹ انجینئرنگ کے لیے خاص طور پر مفید بناتی ہیں۔ اس کورس میں، ہم بنیادی طور پر ChatGPT اور دیگر بڑی زبان کے ماڈلز (LLMs) پر توجہ مرکوز کریں گے۔ ہم جن تکنیکوں کو دریافت کرتے ہیں وہ زیادہ تر LLMs پر لاگو ہوتے ہیں۔

جیسا کہ ہم تصویر بنانے کے دائرے میں قدم رکھتے ہیں، ہم [Stable Diffusion](https://beta.dreamstudio.ai/home) اور [DALLE](https://openai.com/product/dall) کے استعمال کو دریافت کریں گے۔ -e-2)۔

## زبان کے بڑے ماڈلز کیسے کام کرتے ہیں۔

جنریٹو ٹیکسٹ AIs، جیسے GPT-3 اور ChatGPT، ایک پیچیدہ قسم کے عصبی نیٹ ورک کی بنیاد پر کام کرتے ہیں جسے ٹرانسفارمر فن تعمیر کہا جاتا ہے۔ یہ فن تعمیر اربوں مصنوعی نیوران پر مشتمل ہے۔ یہ سمجھنے کے لیے کچھ اہم نکات یہ ہیں کہ یہ AIs کیسے کام کرتے ہیں:

1. اپنے مرکز میں، یہ AIs ریاضیاتی افعال ہیں۔ $f(x) = x^2$ جیسے سادہ فنکشن کے بجائے، ان کو ہزاروں متغیرات کے ساتھ فنکشن کے طور پر سوچیں جو ہزاروں ممکنہ آؤٹ پٹ کا باعث بنتے ہیں۔
2. یہ AIs جملوں کو ٹوکن کہلانے والی اکائیوں میں توڑ کر کارروائی کرتے ہیں، جو الفاظ یا ذیلی الفاظ ہو سکتے ہیں۔ مثال کے طور پر، AI پڑھ سکتا ہے `I don't like` کو `"I", "don", "'t", "like"` کے طور پر۔ اس کے بعد ہر ٹوکن کو AI کے عمل کے لیے نمبروں کی فہرست میں تبدیل کر دیا جاتا ہے۔
3. AIs پچھلے ٹوکن کی بنیاد پر اگلے ٹوکن کی پیشن گوئی کر کے ٹیکسٹ تیار کرتے ہیں۔ مثال کے طور پر، 'مجھے پسند نہیں' کے بعد، AI ممکن ہے کہ 'apples'[^b] کی پیشن گوئی کرے۔ ہر نیا ٹوکن جو وہ تیار کرتے ہیں وہ پچھلے ٹوکن سے متاثر ہوتا ہے۔
4. انسانوں کے برعکس جو بائیں سے دائیں یا دائیں سے بائیں پڑھتے ہیں، یہ AIs بیک وقت تمام ٹوکنز پر غور کرتے ہیں۔

یہ نوٹ کرنا ضروری ہے کہ "سوچنا"، "دماغ"، اور "نیورون" جیسی اصطلاحات ان AIs کے کام کو بیان کرنے کے لیے استعارے ہیں۔ حقیقت میں، یہ ماڈلز ریاضیاتی افعال ہیں، حیاتیاتی ہستی نہیں۔ وہ انسانوں کی طرح "سوچ" نہیں کرتے۔ وہ اس ڈیٹا کی بنیاد پر حساب لگاتے ہیں جس پر انہیں تربیت دی گئی ہے۔

## نتیجہ

AI کے بنیادی کاموں کو سمجھنا بہت ضروری ہے کیونکہ ہم اس کورس میں مزید گہرائی میں جاتے ہیں۔ اگرچہ یہ آسانی سے سمجھنے کے لیے AI کو اینتھروپومورفائز کرنے کے لیے پرکشش ہے، لیکن یہ یاد رکھنا ضروری ہے کہ یہ ماڈلز ریاضیاتی افعال ہیں، سوچنے والی مخلوق نہیں۔ وہ ڈیٹا اور الگورتھم کی بنیاد پر کام کرتے ہیں، انسانی ادراک کی نہیں۔ جیسا کہ ہم AI کی نوعیت اور صلاحیتوں کو دریافت اور بحث کرتے رہتے ہیں، یہ بنیادی علم ایک رہنما کے طور پر کام کرے گا، جو ہمیں مصنوعی ذہانت کی پیچیدہ اور دلچسپ دنیا میں تشریف لے جانے میں مدد کرے گا۔

[^a]: [d2l.ai](https://www.d2l.ai) AI کے کام کرنے کے طریقہ کے بارے میں جاننے کا ایک اچھا ذریعہ ہے۔

[^b]: براہ کرم نوٹ کریں کہ مصنفین، حقیقت میں، سیب سے لطف اندوز ہوتے ہیں۔ وہ مزیدار ہیں۔