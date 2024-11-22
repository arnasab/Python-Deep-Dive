
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
</head>
<body style="font-family: Arial, sans-serif; direction: rtl; text-align: right; line-height: 1.8;">

<h1>نام‌گذاری متغیرها در پایتون</h1>

<hr>

<h2>قوانین نام‌گذاری</h2>
<ul>
    <li>نام‌ها باید با یک آندرلاین (<code dir="ltr">_</code>) یا یک حرف (<code dir="ltr">a-z</code> یا <code dir="ltr">A-Z</code>) شروع شوند.</li>
    <li>نام‌ها می‌توانند شامل هر تعداد از آندرلاین‌ها، حروف، یا اعداد باشند (<code dir="ltr">0-9</code>).</li>
    <li>نام‌ها به حروف بزرگ و کوچک حساس هستند (مثلاً <code dir="ltr">my_var</code> با <code dir="ltr">my_Var</code> متفاوت است).</li>
    <li>نام‌ها نمی‌توانند از کلمات رزرو شده پایتون استفاده کنند، مانند:
        <ul>
            <li><code dir="ltr">False</code>, <code dir="ltr">True</code>, <code dir="ltr">None</code></li>
            <li><code dir="ltr">and</code>, <code dir="ltr">or</code>, <code dir="ltr">if</code>, <code dir="ltr">else</code></li>
            <li>و سایر کلمات کلیدی که توسط پایتون تعریف شده‌اند.</li>
        </ul>
    </li>
</ul>

<p>نمونه‌هایی از نام‌های معتبر و نامعتبر:</p>
<h3>معتبر:</h3>
<ul>
    <li><code dir="ltr">my_var</code></li>
    <li><code dir="ltr">_var</code></li>
    <li><code dir="ltr">var123</code></li>
    <li><code dir="ltr">_my_var_</code></li>
</ul>

<h3>نامعتبر:</h3>
<ul>
    <li><code dir="ltr">123var</code> (شروع با عدد)</li>
    <li><code dir="ltr">for</code> (کلمه رزرو شده)</li>
    <li><code dir="ltr">my-var</code> (استفاده از کاراکتر نامعتبر <code dir="ltr">-</code>)</li>
</ul>

<hr>

<h2>کنوانسیون‌های نام‌گذاری</h2>
<p>در پایتون، رعایت کنوانسیون‌های زیر برای خوانایی و هماهنگی کد توصیه می‌شود:</p>
<ul>
    <li><strong>تک آندرلاین (<code dir="ltr">_my_var</code>):</strong> برای نشان‌دادن اشیاء "خصوصی" یا برای استفاده داخلی در پایتون. با عبارت <code dir="ltr">from module import *</code>این متغیر ها وارد نمیشود</li>
    <li><strong>دو آندرلاین (<code dir="ltr">__my_var</code>):</strong> برای "مخفی‌سازی" ویژگی‌های کلاس در زنجیره‌های ارث‌بری استفاده می‌شود.</li>
    <li><strong>دو آندرلاین در ابتدا و انتها (<code dir="ltr">__my_var__</code>):</strong> برای نام‌هایی که توسط سیستم تعریف شده‌اند، مانند <code dir="ltr">__init__</code> هنگام ساختن نمونه از کلاس فراخونی میشود
     یا با <code dir="ltr">x &lt y</code> در واقع تابع <code dir="ltr">x.__lt__(y)</code> فراخوانی میشود.</li>
</ul>

<hr>

<h2>راهنمای PEP 8 برای نام‌گذاری</h2>
<ul>
    <li><strong>ماژول‌ها:</strong> نام‌های کوتاه و با حروف کوچک. می‌توانند شامل آندرلاین باشند.(مانند <code dir="ltr">utilities</code>).</li>
    <li><strong>پکیج‌ها:</strong> نام‌های کوتاه و با حروف کوچک. بهتر است بدون آندرلاین باشند.(مانند <code dir="ltr">db_utils</code>).</li>
    <li><strong>کلاس‌ها:</strong> از سبک UpperCamelCase استفاده کنید (مانند <code dir="ltr">BankAccount</code>).</li>
    <li><strong>توابع:</strong> از سبک snake_case استفاده کنید (حروف کوچک با آندرلاین جدا شده).(مانند <code dir="ltr">open_account</code>).</li>
    <li><strong>متغیرها:</strong> از سبک snake_case استفاده کنید (مانند <code dir="ltr">account_id</code>).</li>
    <li><strong>ثابت ها:</strong> با حروف بزرگ و جدا شده با آندرلاین (مانند <code dir="ltr">MIN_APR</code>).</li>
</ul>

<hr>

<p>برای مطالعه کامل راهنمای PEP 8 به لینک زیر مراجعه کنید:</p>
<p><a href="https://www.python.org/dev/peps/pep-0008/">PEP 8 Style Guide</a></p>

</body>
</html>
