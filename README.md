## درباره دیتاست

دیتاست مورد استفاده در این پروژه ترکیبی از چند منبع مختلف است که شامل داده‌های واقعی، داده‌های ترجمه‌شده، و داده‌های مصنوعی تولیدشده توسط مدل‌های زبانی است. جزئیات ساخت این دیتاست به شرح زیر است:

### ۱. داده‌های استخراج‌شده از منابع موجود

- از دیتاست [Miras Opinion](https://huggingface.co/datasets/Khedesh/MirasOpinion) تعداد **30,000 نمونه متمایز** با استفاده از الگوریتم **K-Center** انتخاب شد تا متنوع‌ترین داده‌ها برای آموزش مدل فراهم شود.
- سایر داده‌ها از منابع زیر استخراج و به فارسی ترجمه شده‌اند:
  - [Course Reviews on Coursera (Kaggle)](https://www.kaggle.com/datasets/imuhammad/course-reviews-on-coursera?select=Coursera_reviews.csv)
  - [100K Coursera Course Reviews (Kaggle)](https://www.kaggle.com/datasets/septa97/100k-courseras-course-reviews-dataset)
  - [Course Reviews Dataset (Huggingface)](https://huggingface.co/datasets/kkotkar1/course-reviews)
- بخشی از داده‌ها نیز از دیتاست تحلیل احساسات توییت‌های فارسی استخراج شده است:
  - [Persian Sentiment Analysis (GitHub)](https://github.com/baktash81/Persian_Sentiment_Analysis/blob/main/Data/train.tsv)

### ۲. داده‌های مصنوعی تولیدشده با استفاده از ChatGPT

- با استفاده از **ChatGPT API** و طراحی پرامپت‌های هدفمند، تعداد **9,000 نمونه** داده مصنوعی تولید شد:
  - **6,000 نمونه** مربوط به کامنت‌های عادی
  - **3,000 نمونه** به‌صورت **کنایه‌آمیز (Sarcastic)** طراحی شده‌اند
- این داده‌ها موضوعات مختلفی مانند آموزش، خودرو، غذا، آثار هنری و... را پوشش می‌دهند.
- با این حال، ساخت بیش‌ازحد داده‌های مشابه با ساختارهای تکراری باعث کاهش عملکرد مدل در داده‌های تست شد؛ چرا که مدل قادر به تعمیم کافی روی داده‌های جدید نبود.

برای مشاهده این داده‌ها می‌توانید به لینک زیر مراجعه کنید:
- [ChatGPT Dataset (GitHub)](https://github.com/parhamjanjan/Datasets/Main_Gpt)

---

## ساختار کلاس‌بندی

- برخی از دیتاست‌های استفاده‌شده دارای **۵ کلاس احساسی (Emotion Classes)** هستند.
- در مرحله‌ی نهایی، کلاس‌ها به سه دسته‌ی کلی **مثبت، منفی و خنثی** نگاشت شده‌اند.
- اکثر منابع تنها شامل **دو کلاس مثبت و منفی** هستند.
- داده‌های مربوط به **کلاس خنثی** عمدتاً از دیتاست [Miras Opinion](https://huggingface.co/datasets/Khedesh/MirasOpinion) تأمین شده‌اند.
