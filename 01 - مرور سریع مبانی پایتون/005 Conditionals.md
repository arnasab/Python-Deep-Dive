<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
</head>
<body style="font-family: Arial, sans-serif; direction: rtl; text-align: right; line-height: 1.8;">

<h1>دستورات شرطی در پایتون</h1>

<hr>

<h2>دستورات شرطی</h2>
<p>دستور شرطی به شما این امکان را می‌دهد که بر اساس برآورده شدن یا نشدن یک شرط، کد خود را تقسیم کنید. این کار از طریق دستورات <strong>if</strong>، <strong>elif</strong>، <strong>else</strong> یا عملگر شرطی (ترنری) انجام می‌شود.</p>

<h2>استفاده از دستور if</h2>
<p>در این مثال، متغیر <code style="direction: ltr;">a</code> بررسی می‌شود و بر اساس مقدار آن، پیام مناسبی چاپ می‌شود:</p>

<pre style="direction: ltr;">
a = 2
if a < 3:
    print('a < 3')
else:
    print('a >= 3')
</pre>

<p>در این حالت، چون مقدار <code style="direction: ltr;">a</code> کمتر از 3 است، پیام <code style="direction: ltr;">a < 3</code> چاپ می‌شود.</p>

<hr>

<h2>دستورات شرطی تو در تو (Nested If Statements)</h2>
<p>دستورات شرطی می‌توانند در داخل یکدیگر قرار گیرند. در این مثال، ابتدا بررسی می‌شود که آیا مقدار <code style="direction: ltr;">a</code> کمتر از 5 است، سپس بررسی‌های بعدی انجام می‌شود:</p>

<pre style="direction: ltr;">
a = 15
if a < 5:
    print('a < 5')
else:
    if a < 10:
        print('5 <= a < 10')
    else:
        print('a >= 10')
</pre>

<p>در اینجا، چون مقدار <code style="direction: ltr;">a</code> برابر با 15 است، پیام <code style="direction: ltr;">a >= 10</code> چاپ می‌شود.</p>

<hr>

<h2>استفاده از دستور elif</h2>
<p>دستور <code style="direction: ltr;">elif</code> برای بهتر کردن خوانایی کد استفاده می‌شود و می‌تواند جایگزین دستورات شرطی تو در تو باشد:</p>

<pre style="direction: ltr;">
a = 15
if a < 5:
    print('a < 5')
elif a < 10:
    print('5 <= a < 10')
else:
    print('a >= 10')
</pre>

<p>در اینجا نیز چون مقدار <code style="direction: ltr;">a</code> برابر با 15 است، پیام <code style="direction: ltr;">a >= 10</code> چاپ می‌شود.</p>

<hr>

<h2>عملگر شرطی (Ternary Operator)</h2>
<p>پایتون از عملگر شرطی (ترنری) نیز پشتیبانی می‌کند که به شما این امکان را می‌دهد که به‌صورت یک خطی شرط را ارزیابی کنید:</p>

<pre style="direction: ltr;">
a = 5
res = 'a < 10' if a < 10 else 'a >= 10'
print(res)
</pre>

<p>در اینجا، چون مقدار <code style="direction: ltr;">a</code> کمتر از 10 است، پیام <code style="direction: ltr;">a < 10</code> چاپ خواهد شد.</p>

<hr>

<h2>استفاده از عملگر شرطی برای فراخوانی توابع</h2>
<p>عملگر شرطی می‌تواند برای فراخوانی توابع نیز استفاده شود. در این مثال، توابع <code style="direction: ltr;">say_hello</code> و <code style="direction: ltr;">say_goodbye</code> بسته به مقدار متغیر <code style="direction: ltr;">a</code> فراخوانی می‌شوند:</p>

<pre style="direction: ltr;">
def say_hello():
    print('Hello!')

def say_goodbye():
    print('Goodbye!')

a = 5
say_hello() if a < 10 else say_goodbye()

a = 15
say_hello() if a < 10 else say_goodbye()
</pre>

<p>در اینجا، وقتی مقدار <code style="direction: ltr;">a</code> برابر با 5 است، پیام "Hello!" و وقتی برابر با 15 است، پیام "Goodbye!" چاپ می‌شود.</p>

<hr>

<h2>نتیجه‌گیری</h2>
<p>در این ویدیو، استفاده از دستورات شرطی در پایتون را بررسی کردیم. دستورات <code style="direction: ltr;">if</code>، <code style="direction: ltr;">elif</code>، <code style="direction: ltr;">else</code> و عملگر شرطی (ترنری) به شما این امکان را می‌دهند که اجرای کد خود را بر اساس شرایط خاص کنترل کنید.</p>

</body>
</html>
