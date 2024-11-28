<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
</head>
<body style="font-family: Arial, sans-serif; direction: rtl; text-align: right; line-height: 1.8;">

<h1>حلقه while در پایتون</h1>

<hr>

<h2>مقدمه</h2>
<p>در این ویدیو، به بررسی حلقه <code style="direction: ltr;">while</code> در پایتون خواهیم پرداخت. حلقه <code style="direction: ltr;">while</code> به‌طور ساده‌ای است که کد داخل آن تا زمانی که یک شرط درست باشد، اجرا می‌شود.</p>

<h2>ساختار حلقه while</h2>
<p>مثال ساده‌ای از حلقه <code style="direction: ltr;">while</code> را در نظر بگیرید:</p>

<pre style="direction: ltr;">
i = 0
while i < 5:
    print(i)
    i += 1
</pre>

<p>این کد صفر تا چهار را چاپ می‌کند. چرا که حلقه تا زمانی که <code style="direction: ltr;">i</code> کمتر از پنج باشد، اجرا می‌شود. سپس پس از هر تکرار، مقدار <code style="direction: ltr;">i</code> یک واحد افزایش می‌یابد.</p>

<h2>شرط پایان حلقه</h2>
<p>وقتی که <code style="direction: ltr;">i</code> به پنج برسد، حلقه متوقف می‌شود، زیرا شرط <code style="direction: ltr;">i < 5</code> دیگر برقرار نیست.</p>

<h2>حلقه while و اجرای کد در ابتدای آن</h2>
<p>توجه داشته باشید که ممکن است کد داخل حلقه <code style="direction: ltr;">while</code> اصلاً اجرا نشود. به عنوان مثال:</p>

<pre style="direction: ltr;">
i = 5
while i < 5:
    print(i)
    i += 1
</pre>

<p>در این حالت هیچ چیزی چاپ نمی‌شود، چون شرط <code style="direction: ltr;">i < 5</code> در ابتدای حلقه برقرار نیست.</p>

<h2>حلقه do-while در پایتون</h2>
<p>در برخی زبان‌ها مانند C یا JavaScript، حلقه <code style="direction: ltr;">do-while</code> وجود دارد که کد داخل حلقه حداقل یکبار اجرا می‌شود، حتی اگر شرط درست نباشد. پایتون چنین ساختاری ندارد، اما می‌توان آن را به‌صورت دستی با استفاده از حلقه <code style="direction: ltr;">while</code> و دستور <code style="direction: ltr;">break</code> شبیه‌سازی کرد:</p>

<pre style="direction: ltr;">
i = 5
while True:
    print(i)
    if i >= 5:
        break
    i += 1
</pre>

<p>این کد ابتدا <code style="direction: ltr;">i</code> را چاپ می‌کند و سپس بررسی می‌کند که آیا مقدار آن بزرگتر یا برابر پنج است یا خیر. در صورت درست بودن شرط، حلقه شکسته می‌شود.</p>

<h2>استفاده از دستور break</h2>
<p>دستور <code style="direction: ltr;">break</code> برای شکستن حلقه به‌کار می‌رود. اگر بخواهیم از حلقه خارج شویم، می‌توانیم از این دستور استفاده کنیم. به‌عنوان مثال:</p>

<pre style="direction: ltr;">
i = 5
while True:
    print(i)
    if i >= 5:
        break
    i += 1
</pre>

<p>در این کد، حلقه فقط یکبار اجرا می‌شود و پس از چاپ <code style="direction: ltr;">i</code> از حلقه خارج می‌شود.</p>

<h2>استفاده از دستور continue</h2>
<p>دستور <code style="direction: ltr;">continue</code> باعث می‌شود که حلقه به ابتدای آن برگردد و تکرار بعدی اجرا شود. به‌عنوان مثال:</p>

<pre style="direction: ltr;">
a = 0
while a < 10:
    a += 1
    if a % 2 == 0:
        continue
    print(a)
</pre>

<p>این کد فقط اعداد فرد از ۱ تا ۹ را چاپ می‌کند زیرا با دستور <code style="direction: ltr;">continue</code> اعداد زوج نادیده گرفته می‌شوند.</p>

<h2>حلقه while با else</h2>
<p>یکی از ویژگی‌های جالب حلقه <code style="direction: ltr;">while</code> این است که می‌تواند یک بخش <code style="direction: ltr;">else</code> داشته باشد. بخش <code style="direction: ltr;">else</code> تنها زمانی اجرا می‌شود که حلقه به‌طور عادی تمام شده باشد و دستور <code style="direction: ltr;">break</code> در داخل آن اجرا نشده باشد:</p>

<pre style="direction: ltr;">
L = [1, 2, 3]
val = 10
index = 0
while index < len(L):
    if L[index] == val:
        break
    index += 1
else:
    L.append(val)
    print(L)
</pre>

<p>در این مثال، اگر مقدار <code style="direction: ltr;">val</code> در لیست <code style="direction: ltr;">L</code> نباشد، به لیست اضافه می‌شود و سپس چاپ می‌شود. اگر مقدار موجود باشد، حلقه با دستور <code style="direction: ltr;">break</code> خاتمه می‌یابد و بخش <code style="direction: ltr;">else</code> اجرا نمی‌شود.</p>

</body>
</html>
