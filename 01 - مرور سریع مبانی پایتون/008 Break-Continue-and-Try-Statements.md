<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
</head>
<body style="font-family: Arial, sans-serif; direction: rtl; text-align: right; line-height: 1.8;">

<h1>استفاده از دستور Break و Continue در داخل Try...Except...Finally</h1>

<hr>

<h2>مقدمه</h2>
<p>در این بخش، به بررسی رفتار دستورات <code style="direction: ltr;">break</code> و <code style="direction: ltr;">continue</code> در داخل یک <code style="direction: ltr;">try...except...finally</code> خواهیم پرداخت.</p>

<h2>یادآوری: دستور <code style="direction: ltr;">finally</code> همیشه اجرا می‌شود</h2>
<p>یادآوری: در یک دستور <code style="direction: ltr;">try</code>، بخش <code style="direction: ltr;">finally</code> همیشه اجرا می‌شود:</p>

<pre style="direction: ltr;">
a = 10
b = 1
try:
    a / b
except ZeroDivisionError:
    print('division by 0')
finally:
    print('this always executes')
</pre>

<p>در این مثال، به‌دلیل اینکه تقسیم بر صفر انجام نشده، کد خطای صفر نمایش داده نمی‌شود، اما دستور <code style="direction: ltr;">finally</code> همچنان اجرا می‌شود.</p>

<pre style="direction: ltr;">
a = 10
b = 0
try:
    a / b
except ZeroDivisionError:
    print('division by 0')
finally:
    print('this always executes')
</pre>

<p>در این حالت، با وجود خطای تقسیم بر صفر، بخش <code style="direction: ltr;">finally</code> همچنان اجرا خواهد شد.</p>

<h2>استفاده از دستور <code style="direction: ltr;">continue</code> در داخل حلقه <code style="direction: ltr;">while</code> و <code style="direction: ltr;">try</code></h2>
<p>حال بیایید نگاهی بیندازیم به این که وقتی دستور <code style="direction: ltr;">continue</code> یا <code style="direction: ltr;">break</code> در داخل یک حلقه <code style="direction: ltr;">while</code> و دستور <code style="direction: ltr;">try</code> قرار می‌گیرد، چه اتفاقی می‌افتد:</p>

<pre style="direction: ltr;">
a = 0
b = 2

while a < 3:
    print('-------------')
    a += 1
    b -= 1
    try:
        res = a / b
    except ZeroDivisionError:
        print('{0}, {1} - division by 0'.format(a, b))
        res = 0
        continue
    finally:
        print('{0}, {1} - always executes'.format(a, b))
    
    print('{0}, {1} - main loop'.format(a, b))
</pre>

<p>در این مثال، با اینکه در صورت تقسیم بر صفر از دستور <code style="direction: ltr;">continue</code> استفاده می‌کنیم، بخش <code style="direction: ltr;">finally</code> همچنان اجرا می‌شود.</p>

<h2>استفاده از دستور <code style="direction: ltr;">break</code> در داخل حلقه <code style="direction: ltr;">while</code> و <code style="direction: ltr;">try</code></h2>
<p>همین رفتار با دستور <code style="direction: ltr;">break</code> نیز مشابه است:</p>

<pre style="direction: ltr;">
a = 0
b = 2

while a < 3:
    print('-------------')
    a += 1
    b -= 1
    try:
        res = a / b
    except ZeroDivisionError:
        print('{0}, {1} - division by 0'.format(a, b))
        res = 0
        break
    finally:
        print('{0}, {1} - always executes'.format(a, b))
    
    print('{0}, {1} - main loop'.format(a, b))
</pre>

<p>در این کد، با استفاده از دستور <code style="direction: ltr;">break</code>، حلقه به محض رسیدن به شرط قطع می‌شود، اما دستور <code style="direction: ltr;">finally</code> باز هم اجرا خواهد شد.</p>

<h2>ترکیب <code style="direction: ltr;">continue</code> و <code style="direction: ltr;">break</code> با دستور <code style="direction: ltr;">else</code></h2>
<p>حال بیایید ترکیب دستورات <code style="direction: ltr;">continue</code> و <code style="direction: ltr;">break</code> را با بخش <code style="direction: ltr;">else</code> بررسی کنیم:</p>

<pre style="direction: ltr;">
a = 0
b = 2

while a < 3:
    print('-------------')
    a += 1
    b -= 1
    try:
        res = a / b
    except ZeroDivisionError:
        print('{0}, {1} - division by 0'.format(a, b))
        res = 0
        break
    finally:
        print('{0}, {1} - always executes'.format(a, b))
    
    print('{0}, {1} - main loop'.format(a, b))
else:
    print('\n\nno errors were encountered!')
</pre>

<p>در این کد، اگر هیچ خطایی پیش نیاید، بخش <code style="direction: ltr;">else</code> اجرا خواهد شد و پیامی مبنی بر عدم وجود خطاها نمایش داده می‌شود.</p>

<p>در صورتی که خطاهایی در حین اجرای حلقه اتفاق بیفتد، مثل تقسیم بر صفر، حلقه به‌طور معمول ادامه می‌یابد و بخش <code style="direction: ltr;">else</code> اجرا نمی‌شود.</p>

</body>
</html>
