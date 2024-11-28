<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
</head>
<body style="font-family: Arial, sans-serif; direction: rtl; text-align: right; line-height: 1.8;">

<h1>حلقه For در پایتون</h1>

<hr>

<h2>مقدمه</h2>
<p>یک **iterable** به چیزی گفته می‌شود که می‌تواند تکرار شود. :)</p>

<h2>تعریف بهتر از iterable</h2>
<p>شاید یک روش غیر دایره‌ای بهتر برای تعریف iterable این باشد که آن را به‌عنوان مجموعه‌ای از چیزهایی در نظر بگیریم که می‌توان به‌صورت یکی یکی به آن‌ها دسترسی پیدا کرد.</p>
<p>در پایتون، یک **iterable** معنای خاصی دارد: یک **شیء** که قادر به بازگرداندن اعضای خود یکی یکی است.</p>
<p>چندین شیء در پایتون iterable هستند: لیست‌ها، رشته‌ها، اشیاء فایل و بسیاری دیگر.</p>

<h2>استفاده از دستور **for** برای تکرار در پایتون</h2>
<p>دستور **for** می‌تواند برای تکرار یک iterable استفاده شود.</p>

<h2>حلقه for در دیگر زبان‌های برنامه‌نویسی</h2>
<p>اگر شما تجربه‌ای در زبان‌های برنامه‌نویسی دیگر دارید، احتمالاً دستور **for** را به این صورت دیده‌اید:</p>
<pre style="direction: ltr;">
for (int i=0; i < 5; i++) {
    //کد درون بلوک
}
</pre>

<p>این شکل از حلقه **for** تنها یک تکرار است، شبیه به حلقه **while**. در واقع این معادل چیزی است که در پایتون می‌توانیم به صورت زیر بنویسیم:</p>

<pre style="direction: ltr;">
i = 0
while i < 5:
    #کد درون بلوک
    print(i)
    i += 1
i = None
</pre>

<h2>حلقه **for** در پایتون</h2>
<p>اما این چیزی که در پایتون می‌بینید، دقیقاً همانطور که در زبان‌های دیگر تعریف می‌شود، نیست. در پایتون، دستور **for** برای **تکرار** روی iterables است و هیچ ارتباطی با حلقه‌های **for** استاندارد ندارند. معادل نزدیک‌تر آن در پایتون همان حلقه **while** است.</p>

<h2>برای استفاده از حلقه **for** در پایتون به یک iterable نیاز داریم</h2>
<p>یک شیء ساده iterable توسط تابع <code style="direction: ltr;">range()</code> تولید می‌شود:</p>

<pre style="direction: ltr;">
for i in range(5):
    print(i)
</pre>

<h2>حلقه **for** در پایتون در واقع تکرار روی یک شیء iterable است</h2>
<p>گرچه این به نظر نزدیک‌ترین معادل به حلقه **for** استاندارد C است، اما همچنان یک تفاوت عمده وجود دارد که در آن ما داریم روی یک شیء iterable تکرار می‌کنیم، که این بسیار متفاوت است.</p>

<h2>چندین شیء iterable در پایتون</h2>
<p>در پایتون بسیاری از اشیاء iterable هستند:</p>

<pre style="direction: ltr;">
for x in [1, 2, 3]:
    print(x)
</pre>

<pre style="direction: ltr;">
for x in 'hello':
    print(x)
</pre>

<pre style="direction: ltr;">
for x in ('a', 'b', 'c'):
    print(x)
</pre>

<h2>هر بار که روی یک iterable تکرار می‌کنیم، مقدار "بعدی" را باز می‌گرداند</h2>
<p>ما حتی می‌توانیم مقادیر هر زوج از tuple را به متغیرهای خاص اختصاص دهیم:</p>

<pre style="direction: ltr;">
for i, j in [(1, 2), (3, 4), (5, 6)]:
    print(i, j)
</pre>

<h2>دستور **break** و **continue** در حلقه **for**</h2>
<p>دستورات **break** و **continue** در حلقه‌های **for** دقیقاً مشابه حلقه‌های **while** کار می‌کنند:</p>

<pre style="direction: ltr;">
for i in range(5):
    if i == 3:
        continue
    print(i)
</pre>

<pre style="direction: ltr;">
for i in range(5):
    if i == 3:
        break
    print(i)
</pre>

<h2>حلقه **for** و دستور **else**</h2>
<p>حلقه **for** همانند حلقه **while** از دستور **else** پشتیبانی می‌کند که تنها در صورتی اجرا می‌شود که حلقه به‌طور معمول خاتمه یابد (یعنی به دلیل دستور **break** از حلقه خارج نشده باشد):</p>

<pre style="direction: ltr;">
for i in range(1, 5):
    print(i)
    if i % 7 == 0:
        print('multiple of 7 found')
        break
else:
    print('No multiples of 7 encountered')
</pre>

<pre style="direction: ltr;">
for i in range(1, 8):
    print(i)
    if i % 7 == 0:
        print('multiple of 7 found')
        break
else:
    print('No multiples of 7 encountered')
</pre>

<h2>ترکیب دستورات **break** و **continue** با بخش **finally** در دستور **try**</h2>
<p>دستورات **break** و **continue** همچنین در ترکیب با بخش **finally** در دستور **try** به همان صورت که در حلقه‌ها استفاده می‌شوند، عمل می‌کنند:</p>

<pre style="direction: ltr;">
for i in range(5):
    print('--------------------')
    try:
        10 / (i - 3)
    except ZeroDivisionError:
        print('divided by 0')
        continue
    finally:
        print('always runs')
    print(i)
</pre>

<h2>روش‌های استاندارد برای تکرار روی iterables</h2>
<p>روش‌های استاندارد زیادی برای تکرار روی iterables وجود دارد:</p>

<pre style="direction: ltr;">
s = 'hello'
for c in s:
    print(c)
</pre>

<h2>چگونه برای انواع iterable قابل شاخص‌گذاری، شاخص آیتم‌ها را در حلقه پیدا کنیم</h2>
<p>گاهی اوقات برای انواع iterable که می‌توانند شاخص‌گذاری شوند (مانند دنباله‌ها)، می‌خواهیم شاخص هر آیتم را در حلقه نیز بدانیم:</p>

<pre style="direction: ltr;">
s = 'hello'
i = 0
for c in s:
    print(i, c)
    i += 1
</pre>

<p>روش بهتری برای این کار استفاده از <code style="direction: ltr;">range(len(s))</code> است:</p>

<pre style="direction: ltr;">
s = 'hello'

for i in range(len(s)):
    print(i, s[i])
</pre>

<p>و یا حتی بهتر، استفاده از <code style="direction: ltr;">enumerate()</code>:</p>

<pre style="direction: ltr;">
s = 'hello'

for i, c in enumerate(s):
    print(i, c)
</pre>

<h2>نتیجه‌گیری</h2>
<p>ما به تفصیل در طول دوره در مورد تمامی این تکنیک‌های تکرار در iterables صحبت خواهیم کرد.</p>

</body>
</html>
