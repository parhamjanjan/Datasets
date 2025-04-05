## درباره دیتاست

دیتاستی که در این پروژه مورد استفاده قرار گرفته، حاصل ترکیب چند منبع مختلف و همچنین تولید داده‌های مصنوعی است. جزئیات آن به شرح زیر است:

- دیتاست نهایی شامل حدود **60,000 نمونه** است.
- از دیتاست [Miras Opinion](https://huggingface.co/datasets/Khedesh/MirasOpinion) تعداد **30,000 نمونه متمایز** با استفاده از الگوریتم **K-Center** انتخاب شد تا متنوع‌ترین داده‌ها برای آموزش مدل فراهم شود.
- حدود **9,000 داده مصنوعی** نیز توسط ما با استفاده از **ChatGPT API** و طراحی پرامپت مناسب تولید شده‌اند:
  - **6,000 نمونه** مربوط به کامنت‌های عادی
  - **3,000 نمونه** به صورت **کنایه‌آمیز (sarcastic)** طراحی شده‌اند

- سایر داده‌ها از منابع زیر تهیه شده‌اند:
  - ترجمه‌ی فارسی از دیتاست‌های خارجی مرتبط با کامنت‌های دوره‌های آموزشی:
    - [Course Reviews on Coursera (Kaggle)](https://www.kaggle.com/datasets/imuhammad/course-reviews-on-coursera?select=Coursera_reviews.csv)
    - [100K Coursera Course Reviews (Kaggle)](https://www.kaggle.com/datasets/septa97/100k-courseras-course-reviews-dataset)
    - [Course Reviews Dataset (Huggingface)](https://huggingface.co/datasets/kkotkar1/course-reviews)
  - بخشی دیگر از داده‌ها از دیتاست توییت‌های فارسی مربوط به تحلیل احساسات استخراج شده است:
    - [Persian Sentiment Analysis (GitHub)](https://github.com/baktash81/Persian_Sentiment_Analysis/blob/main/Data/train.tsv)
-باید توجه داشت که ساخت داده ی بیش از حد با api chatgpt نیز مشکلاتی به همراه داشت فارغ از مدت زمان و هزینه صرف شده مدل با دیدن داده های نزدیک به هم که از یک ساختار کلی یکسان پیروی می کند خوب یاد نمیگرفت و عملکرد مدل در داده های تست اصلا خوب نبود میتوانید دیتاست های تولید شده با chatgpt را مشاهده کنید:
    - [ChatGpt Dataset (GitHub)](https://github.com/parhamjanjan/Datasets/Main_Gpt)

- با اینکه دیتاست را در موضوعات مختلف آموزشی خودرو غذا اثرات هنری و ... ساختیم باز هم مدل عملکرد خوبی به همراه نداشت
## ساختار کلاس‌بندی

- برخی از این دیتاست‌ها دارای **۵ کلاس احساسی (Emotion Classes)** هستند.
- در پردازش نهایی، ترکیب این کلاس‌ها به صورت **مثبت، منفی، یا خنثی** در نظر گرفته شده است.
- اکثر دیتاست‌های مورد استفاده تنها شامل **دو کلاس (مثبت و منفی)** هستند.
- کلاس‌های **خنثی** عمدتاً از دیتاست [Miras Opinion](https://huggingface.co/datasets/Khedesh/MirasOpinion) استخراج شده‌اند.
