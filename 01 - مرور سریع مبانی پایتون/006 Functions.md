<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
</head>
<body style="font-family: Arial, sans-serif; direction: rtl; text-align: right; line-height: 1.8;">

<h1>توابع در پایتون</h1>

<hr>

<h2>مقدمه</h2>
<p>پایتون دارای بسیاری از توابع و متدهای داخلی است که می‌توانیم از آن‌ها استفاده کنیم. برخی از این توابع به طور پیش‌فرض در دسترس هستند، در حالی که برخی دیگر نیاز به وارد کردن دارند.</p>

<h2>توابع پیش‌فرض</h2>
<p>برخی توابع در پایتون به طور پیش‌فرض در دسترس هستند. به عنوان مثال، تابع <code style="direction: ltr;">len()</code> برای محاسبه طول یک لیست استفاده می‌شود:</p>

<pre style="direction: ltr;">
s = [1, 2, 3]
len(s)
</pre>

<p>نتیجه اجرای این کد <code style="direction: ltr;">3</code> خواهد بود.</p>

<hr>

<h2>وارد کردن توابع</h2>
<p>برخی توابع باید وارد شوند. به عنوان مثال، برای استفاده از تابع <code style="direction: ltr;">sqrt()</code> از ماژول <code style="direction: ltr;">math</code>، ابتدا باید آن را وارد کنیم:</p>

<pre style="direction: ltr;">
from math import sqrt
sqrt(4)
</pre>

<p>نتیجه اجرای این کد <code style="direction: ltr;">2.0</code> خواهد بود.</p>

<hr>

<h2>وارد کردن کل ماژول‌ها</h2>
<p>ما همچنین می‌توانیم یک ماژول کامل را وارد کنیم و از تمامی توابع آن استفاده کنیم:</p>

<pre style="direction: ltr;">
import math
math.exp(1)
</pre>

<p>نتیجه اجرای این کد مقدار <code style="direction: ltr;">2.718281828459045</code> خواهد بود.</p>

<hr>

<h2>تعریف توابع خودمان</h2>
<p>ما می‌توانیم توابع خود را نیز تعریف کنیم. در اینجا یک تابع ساده که عبارت "running func1" را چاپ می‌کند، تعریف کرده‌ایم:</p>

<pre style="direction: ltr;">
def func_1():
    print('running func1')

func_1()
</pre>

<p>نتیجه اجرای این کد، چاپ <code style="direction: ltr;">running func1</code> خواهد بود.</p>

<hr>

<h2>توابع با پارامتر</h2>
<p>ما همچنین می‌توانیم توابعی تعریف کنیم که پارامترهایی بگیرند. در اینجا یک تابع <code style="direction: ltr;">func_2</code> تعریف شده که دو پارامتر <code style="direction: ltr;">a</code> و <code style="direction: ltr;">b</code> را گرفته و نتیجه ضرب آن‌ها را برمی‌گرداند:</p>

<pre style="direction: ltr;">
def func_2(a, b):
    return a * b

func_2(3, 2)
</pre>

<p>نتیجه اجرای این کد <code style="direction: ltr;">6</code> خواهد بود.</p>

<hr>

<h2>پارامترهای ناهمگون</h2>
<p>توجه داشته باشید که توابع می‌توانند انواع مختلفی از داده‌ها را بپذیرند. برای مثال، اگر پارامترها رشته و عدد باشند، پایتون آن‌ها را بدون خطا پردازش می‌کند:</p>

<pre style="direction: ltr;">
func_2('a', 3)
</pre>

<p>نتیجه اجرای این کد <code style="direction: ltr;">'aaa'</code> خواهد بود.</p>

<hr>

<h2>استفاده از نوع‌گذاری (Type Annotations)</h2>
<p>ما می‌توانیم نوع پارامترها را برای توابع خود مشخص کنیم. این نوع‌گذاری‌ها فقط برای مستندسازی و کمک به IDE‌ها هستند و تأثیری در اجرای کد ندارند:</p>

<pre style="direction: ltr;">
def func_3(a: int, b: int):
    return a * b

func_3(2, 3)
</pre>

<p>نتیجه اجرای این کد <code style="direction: ltr;">6</code> خواهد بود.</p>

<hr>

<h2>توابع به‌عنوان اشیاء</h2>
<p>توابع در پایتون می‌توانند به‌عنوان اشیاء عمل کنند، به این معنی که می‌توان آن‌ها را به متغیرها نسبت داد:</p>

<pre style="direction: ltr;">
my_func = func_3
my_func(2, 3)
</pre>

<p>نتیجه اجرای این کد نیز <code style="direction: ltr;">6</code> خواهد بود.</p>

<hr>

<h2>بازگشت پیش‌فرض None</h2>
<p>اگر تابعی مقداری را برنگرداند، پایتون به‌طور پیش‌فرض <code style="direction: ltr;">None</code> را باز می‌گرداند:</p>

<pre style="direction: ltr;">
def func_4():
    a = 2

res = func_4()
print(res)
</pre>

<p>نتیجه اجرای این کد چاپ <code style="direction: ltr;">None</code> خواهد بود.</p>

<hr>

<h2>دستور def</h2>
<p>دستور <code style="direction: ltr;">def</code> یک قطعه کد اجرایی است که تابع را ایجاد می‌کند و آن را به نام متغیر اختصاص می‌دهد. توجه داشته باشید که کد داخل تابع تنها زمانی اجرا می‌شود که تابع فراخوانی شود.</p>

<hr>

<h2>مثال از توابع وابسته</h2>
<p>در اینجا یک مثال از توابعی است که به‌طور وابسته فراخوانی می‌شوند:</p>

<pre style="direction: ltr;">
def fn_1():
    fn_2()

def fn_2():
    print('Hello')

fn_1()
</pre>

<p>در اینجا، تابع <code style="direction: ltr;">fn_1</code> تابع <code style="direction: ltr;">fn_2</code> را فراخوانی می‌کند و پیام "Hello" چاپ می‌شود.</p>

<hr>

<h2>توابع lambda</h2>
<p>پایتون همچنین از توابع <code style="direction: ltr;">lambda</code> پشتیبانی می‌کند که توابعی بدون نام هستند و می‌توانند به‌طور موقت تعریف شوند:</p>

<pre style="direction: ltr;">
func_5 = lambda x: x**2
func_5(2)
</pre>

<p>نتیجه اجرای این کد <code style="direction: ltr;">4</code> خواهد بود.</p>

</body>
</html>
