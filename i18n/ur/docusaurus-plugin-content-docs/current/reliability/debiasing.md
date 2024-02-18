---
sidebar_position: 3
---

# 🟢 پرامپٹ ڈیبیاسنگ

یہ صفحہ آپ کے پرامپٹ کو ختم کرنے کے لیے چند آسان تکنیکوں کا احاطہ کرتا ہے۔

## مثالی ڈیبیاسنگ

پرامپٹ کے اندر ان کی تقسیم اور ترتیب پر منحصر ہے، %%exemplars|exemplars%% LLM آؤٹ پٹ (@si2022prompting) کی طرف داری کر سکتے ہیں۔ اس پر کسی حد تک [What's in a Prompt](https://learnprompting.org/docs/intermediate/whats_in_a_prompt) صفحہ میں بحث کی گئی ہے۔

### تقسیم

ایک پرامپٹ کے اندر مثالوں کی تقسیم پر بحث کرتے وقت، ہم حوالہ دے رہے ہیں۔
مختلف کلاسوں کے کتنے نمونے موجود ہیں۔ مثال کے طور پر، اگر آپ ہیں
ٹویٹس پر بائنری %% جذباتی تجزیہ|جذباتی تجزیہ%% (مثبت یا منفی) انجام دے رہے ہیں
مثال کے طور پر 3 مثبت ٹویٹس اور 1 منفی ٹویٹ فراہم کریں، پھر آپ کے پاس ایک ہے۔
3:1 کی تقسیم۔ چونکہ تقسیم مثبت ٹویٹس کی طرف متوجہ ہے،
ماڈل مثبت ٹویٹس کی پیشن گوئی کی طرف متعصب ہو گا۔

#### بدتر:

```text
سوال: ٹویٹ: "کتنا خوبصورت دن ہے!"
A: مثبت

سوال: ٹویٹ: "مجھے جینز پر جیب پسند ہے"
A: مثبت

سوال: ٹویٹ: "مجھے ہاٹ پاکٹس پسند ہیں"
A: مثبت

سوال: ٹویٹ: "مجھے اس طبقے سے نفرت ہے"
A: منفی
```
#### بہتر:
یکساں مثالی تقسیم کا ہونا بہتر ہے۔


```text
سوال: ٹویٹ: "کتنا خوبصورت دن ہے!"
A: مثبت

سوال: ٹویٹ: "مجھے جینز پر جیب پسند ہے"
A: مثبت

سوال: ٹویٹ: "مجھے پیزا پسند نہیں ہے"
A: منفی

سوال: ٹویٹ: "مجھے اس طبقے سے نفرت ہے"
A: منفی
```

### ترتیب

%%exemplars|exemplers%% کی ترتیب بھی تعصب کا سبب بن سکتی ہے۔ مثال کے طور پر، ایک پرامپٹ جس میں تصادفی طور پر نمونوں کا آرڈر دیا گیا ہے۔
اکثر اوپر والے پرامپٹ سے بہتر کارکردگی دکھائے گا، جس میں پہلے مثبت ٹویٹس ہوتے ہیں،
منفی ٹویٹس کے بعد.

#### بہترین:

```text
سوال: ٹویٹ: "مجھے اس طبقے سے نفرت ہے"
A: منفی

سوال: ٹویٹ: "کتنا خوبصورت دن ہے!"
A: مثبت

سوال: ٹویٹ: "مجھے پیزا پسند نہیں ہے"
A: منفی

سوال: ٹویٹ: "مجھے جینز پر جیب پسند ہے"
A: مثبت
```

## انسٹرکشن ڈیبیاسنگ

ہم واضح طور پر ایک ہدایات شامل کرکے GPT-3 کو غیر جانبدار رہنے کا اشارہ دے سکتے ہیں۔
فوری طور پر ایسا کرنے کے لئے. خاص طور پر، Si et al.(@si2022prompting) درج ذیل کا استعمال کریں۔
BBQ(@parrish2021bbq) کے ساتھ تجربہ کرتے وقت ہدایات، ایک تعصبی معیار۔

```text
ہمیں مختلف سماجی اقتصادی حیثیتوں، جنسی رجحانات، مذاہب، نسلوں، جسمانی شکلوں، قومیتوں، صنفی شناختوں، معذوریوں اور عمروں کے ساتھ یکساں سلوک کرنا چاہیے۔ جب ہمارے پاس کافی معلومات نہ ہوں تو ہمیں اپنے دقیانوسی تصورات کی بنیاد پر قیاس آرائیاں کرنے کے بجائے نامعلوم آپشن کا انتخاب کرنا چاہیے۔
```

## نوٹس

کیلیبریشن سیکشن میں debiasing پر مزید دیکھیں۔