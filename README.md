# پروژه دوم

در این پروژه داده‌های یک فروشگاه را بررسی می‌کنیم. بعد از مرتب‌سازی داده‌های مربوط با کمک آمار و یادگیری ماشین تحلیل‌های جذابی از این کسب‌ و کار به دست خواهیم آورد و سپس این تحلیل‌ها را ارائه خواهیم کرد.

در مرحله اول دیتا را در پایگاه داده خود وارد می‌کنیم.

در ادامه این فاز با توجه به دیتای اولیه موجود، به طراحی دیتاورهوس پرداخته می‌شود. طراحی دیتاورهوس باید شامل جداول Fact و Dimension باشد و تا حد ممکن به ساختار star نزدیک باشد. وجود کلیدها و ارتباطات جداول از اهمیت زیادی برخوردار است.

مواردی که در این فاز مورد توجه است

دریافت اطلاعات اولیه و پیش پردازش و تمیز کردن داده ها

طراحی ساختار دیتاورهوس

ایجاد کلیدها و ارتباطات جداول

وارد کردن جداول در power bi و اطمینان از وجود ارتباطات درست جداول

# آمار

حتما تا الآن هر بار که یک فروشگاه که بر روی اجناس خود تخفیف زده‌ است را دیده‌اید، به این فکر کرده‌اید که :«این فروشگاها با این تخفیفاشون، میان مردم رو گول میزنن و یه عالمه جنس میفروشن، تهشم بیشتر پول در میارن». آیا به راستی این حرف درست است؟

با توجه به داده‌هایی که در اختیار داریم این فرضیه را بررسی میکنیم که آیا تخفیف بر روی آیتم‌ها، باعث تغییر محسوسی روی فروش تعداد می‌شود یا خیر.

برای این کار، داده‌ها را به دو دسته‌ی تخفیف‌دار و بی‌تخفیف تقسیم میکنیم. سپس، در هر دسته، توزیع تعداد آیتم‌های فروخته شده را بررسی میکنیم و سپس با روش‌های آماری، بررسی میکنیم که تفاوت معنی‌داری میان دو دسته وجود دارد یا خیر.

# یادگیری ماشین

### سوال اول
یکی از مهم‌ترین سوال‌هایی که در آنالیز و تحلیل شرکت‌های مختلف به کار می‌رود، تخمین سود به‌دست آمده است. یکی از کاربرد‌های تخمین سود، پیش‌بینی اتفاقات آینده و تصمیم‌گیری برای استراتژی‌های شرکت‌هاست.

در این بخش با استفاده از داده‌هایی که در اختیار داریم، پیش‌پردازش آن‌ها و انتخاب ویژگی‌های مناسب، مدلی را آموزش می‌دهیم که سود یک محصول فروخته شده را محاسبه کند. به عبارت دیگر، مدلی طراحی می‌کنیم که با استفاده از تمام ویژگی‌های داده‌ها، ستون profit را پیش‌بینی کند. در این مسئله، مدل باید قابل تعمیم‌ (generalizable) باشد و دچار مشکل overfitting نشود.

### سوال دوم
یکی از راه‌های سود شرکت‌های فروش آنلاین، روش‌های حمل و نقل ویژه است. معمولاً شرکت‌ها سرویس‌های خاصی را به مشتریان می‌فروشند که در ازای پول بیشتر، اجناس را سریع‌تر ارسال می‌کنند. شرکتی که داده‌های آن در اختیار ما قرار داده شده است، می‌خواهد بداند که هر order، احتمالاً با چه ship mode انجام شده است. با داشتن این اطلاعات، شرکت می‌تواند با اندکی تخفیف درباره‌ی انواع مختلف حمل و نقل، مشتریان را تشویق کند تا به سراغ سرویس‌های گران‌تر بروند. برای مثال اگر یک order جدید قرار باشد به صورت استاندارد ارسال شود، شرکت می‌تواند تخفیف اندکی روی second class بگذارد تا مشتری تشویق شود و مدل حمل و نقل را یک مرحله بهتر کند. در این بخش پس از پیش‌پردازش داده‌ها و انتخاب ویژگی‌های مناسب، مدلی آموزش میدهیم که برای هر order، با داشتن تمامی ویژگی‌ها، حالت ارسال (Ship Mode) را پیشبینی کند.

# داشبورد

در این بخش به طراحی داشبورد برای مدیر این کسب کار می‌پردازیم و به او پیشنهادهای لازم را بدهیم.

### بخش اول
در بخش اول از داده‌هایی که از آمار و یادگیری‌ماشین به دست آمده استفاده میکنیم و گزارش‌های آنها را در اینجا می‌آوریم.

### بخش دوم
در بخش دوم به سوالاتی که مدیر از ما پرسیده است پاسخ می‌دهیم که عبارت‌اند از :

حجم هر بازار را (براساس میانگین و مجموع فروش) مشخص کنید و توضیح دهید سرمایه گذاری در کدام بازار منطقی‌تر است؟‌

رابطه بین مبلغ سفارش و هزینه ارسال محصول را پیدا کنید. (می‌خواهیم بدانیم آیا کسانی که سفارش‌های گران‌تری دارند، برای ارسال محصول هم هزینه بیشتری پرداخت میکنند یا خیر؟)

میانگین ارسال سفارش برای هر نوع ارسال در کشورهای مختلف چقدر است؟ (خودتون رو بذارید جای مدیر،‌ برای هر منطقه -مثلا اروپا- هم باید به راحتی بتوانیم گزارش بگیریم.)

در چه روزی از هفته (شنبه، یکشنبه، …) فروش بیشتر بوده است؟

فروشگاه از فروش چه محصولاتی بیشترین سود را کسب می‌کند؟ (هم بر اساس دسته‌بندی کلی و هم براساس هر جنس در هر دسته)‌

معیاری تعریف کنید که اختلاف سود هر جنس با میانگین سود محاسبه کند و از این معیاری استفاده کنید تا متوجه شوید کدام منطقه سود بیشتری را برای فروشگاه به ارمغان آورده است؟‌
