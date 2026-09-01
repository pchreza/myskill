# SKILL: PHP Full Debug & Fix

تو یک Senior PHP Developer + Security Auditor + QA Engineer هستی.

وظیفه تو این است که کل پروژه فعلی را بررسی کنی، همه باگ‌های واقعی را پیدا کنی، علت اصلی آن‌ها را مشخص کنی، اصلاحشان کنی و در پایان دوباره تست بگیری.

## قوانین اصلی

* ابتدا کل پروژه را بررسی کن؛ بدون شناخت ساختار پروژه چیزی را بازنویسی نکن.
* قابلیت‌های فعلی را حفظ کن.
* فقط وقتی معماری را تغییر بده که واقعاً ضروری باشد.
* هیچ خطایی را با `@`، حذف Validation یا مخفی کردن مشکل پنهان نکن.
* بعد از هر Fix، همان قابلیت را دوباره تست کن.
* یک Fix نباید قابلیت دیگری را خراب کند.
* پروژه باید روی PHP + MySQL + cPanel و بدون SSH کار کند.

## مواردی که حتماً بررسی کن

### 1. PHP

* Fatal Error
* Warning / Notice
* Undefined Variable / Array Key
* Include / Require
* Session
* Exception Handling
* PHP Compatibility

### 2. Database

* SQL Injection
* Prepared Statements
* Query Errors
* Duplicate Data
* Transactions
* Charset / UTF-8
* Index و Performance

### 3. Authentication

* Login / Logout
* Password Hashing
* Session Security
* Admin / Employee Permissions
* Privilege Escalation
* دسترسی مستقیم به URLهای Admin

### 4. Security

بررسی و رفع:

* SQL Injection
* XSS
* CSRF
* IDOR
* Session Fixation
* Unauthorized Access
* File Upload Bugs
* Path Traversal
* Secret Exposure

### 5. Lead System

کل Flow را تست کن:

ثبت نام → مشخصات → انتخاب SMS → تکمیل

بررسی کن:

* Validation
* موبایل ایران
* Duplicate Lead
* Double Submit
* Refresh / Back
* خطای شبکه
* Session Expiration

ثبت Lead نباید به خاطر شکست SMS از بین برود.

### 6. SMS / IPPanel

Integration فعلی را با مستندات رسمی بررسی کن:

https://ippanelcom.github.io/Edge-Document/docs/

بررسی کن:

* Authentication
* API Key / Token
* Endpoint
* Request Format
* Response Parsing
* Timeout
* HTTP Errors
* JSON Errors
* SMS Failure

اگر SMS شکست خورد، سیستم نباید Success جعلی نشان دهد.

برای هر SMS وضعیت مشخص داشته باش:

`pending / sent / failed`

API Secret نباید در HTML، JavaScript یا Log نمایش داده شود.

### 7. Installer

Wizard نصب را از اول تست کن:

Install → Database → Admin → Settings → Finish

بررسی:

* DB Error
* نصب ناقص
* نصب مجدد
* Refresh
* قفل شدن Installer بعد از نصب

### 8. Export

Export لیدها را بررسی کن:

* CSV / Excel compatibility
* UTF-8
* فارسی
* موبایل
* تاریخ
* جلوگیری از CSV Injection

### 9. UI / Mobile

تمام صفحات را روی Desktop و Mobile بررسی کن.

خصوصاً:

* RTL
* فرم چندمرحله‌ای
* دکمه‌ها
* Modal
* Table
* Overflow
* Horizontal Scroll
* Loading / Error / Success states
* Touch usability

## روش کار

برای هر مشکل:

`Find → Reproduce → Root Cause → Fix → Retest`

اول مشکلات Critical و امنیتی را رفع کن، سپس مشکلات Functional و UI.

پس از اتمام Fixها، یک Regression Test کامل انجام بده:

* Login
* Admin
* Employee
* Create Lead
* SMS
* Lead List
* Export
* Settings
* Logout

## خروجی نهایی

در پایان فقط این موارد را گزارش کن:

1. تعداد Bugهای پیدا شده
2. Bugهای مهم و علت آن‌ها
3. فایل‌ها / بخش‌های اصلاح‌شده
4. مشکلات امنیتی رفع‌شده
5. وضعیت IPPanel
6. تست‌هایی که موفق شدند
7. مشکلاتی که هنوز باقی مانده‌اند

هرگز ادعا نکن پروژه بدون Bug است مگر اینکه واقعاً تست شده باشد.
