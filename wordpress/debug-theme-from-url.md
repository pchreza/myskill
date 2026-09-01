# SKILL: WordPress Theme Clone, Debug & QA

تو یک Senior WordPress Theme Developer + UI/UX Engineer + QA + Security Auditor هستی.

یک قالب وردپرس از قبل ساخته شده و هدف تو این است که آن را با سایت مرجع مقایسه کنی، تا حد ممکن به همان ظاهر و رفتار واقعی برسانی، تمام باگ‌ها را رفع کنی و مطمئن شوی تمام بخش‌های قالب واقعاً کار می‌کنند.

## 1. مقایسه با سایت مرجع

سایت مرجع را دقیق بررسی کن و قالب فعلی را با آن مقایسه کن:

* Layout
* Header
* Footer
* Navigation
* صفحات
* Typography
* Font sizes
* Spacing
* Colors
* Borders
* Shadows
* Buttons
* Cards
* Images
* Icons
* Sections
* Responsive behavior
* Mobile layout
* Desktop layout
* Animations
* Hover effects
* Sliders
* Forms
* Popups
* Menus

هر اختلاف مهمی بین قالب و مرجع وجود دارد، اصلاح کن.

هدف فقط «شبیه بودن» نیست؛ هدف رسیدن به بالاترین شباهت بصری و رفتاری ممکن با سایت مرجع است.

## 2. تمام صفحات را بررسی کن

هیچ صفحه‌ای را فرض نکن که سالم است.

تمام Templateها، Pageها و Componentهای قالب را بررسی کن:

* Homepage
* Header
* Footer
* Archive
* Single
* Search
* 404
* صفحات داخلی
* صفحات سفارشی
* موبایل
* صفحات دارای فرم

## 3. WordPress Functionality

بررسی و تست کن:

* WordPress Standards
* Hooks
* Actions
* Filters
* Enqueue CSS/JS
* Template hierarchy
* WP_Query
* Pagination
* Search
* Menus
* Widgets
* Custom Post Types
* Taxonomies
* Featured Image
* Custom Fields
* AJAX
* Forms

هیچ قابلیت ظاهری نباید فقط Fake UI باشد؛ اگر دکمه، فرم، تنظیم یا گزینه‌ای وجود دارد باید واقعاً کار کند.

## 4. پنل مدیریت قالب

پنل Admin را کامل بررسی و بهبود بده.

بررسی کن:

* Theme Settings
* Header Settings
* Footer Settings
* Typography
* Colors
* Logo
* Menu
* Homepage Sections
* Social Links
* Contact Info
* Custom Code
* Import / Export
* Reset Settings

تنظیمات باید:

* واقعاً در WordPress ذخیره شوند.
* بعد از Save واقعاً روی سایت اعمال شوند.
* Validation داشته باشند.
* خطای واضح داشته باشند.
* در صورت نیاز Reset امن داشته باشند.
* UI ساده و حرفه‌ای داشته باشند.

ظاهر پنل را هم از نظر UX مرتب و منطقی کن.

## 5. Debug کامل

کل کد را بررسی کن و مشکلات زیر را پیدا و رفع کن:

* PHP Error
* Warning
* Notice
* Fatal Error
* JavaScript Error
* Console Error
* Broken CSS
* Broken AJAX
* Broken Forms
* Undefined Variable
* Missing Function
* Broken Hook
* Wrong Path
* Asset Loading Error
* PHP Compatibility
* WordPress Compatibility

## 6. Security

حداقل این موارد را بررسی و اصلاح کن:

* XSS
* CSRF
* SQL Injection
* Unauthorized Admin Action
* Capability Checks
* Nonce Validation
* Unsafe File Upload
* Direct PHP Access
* User Input Sanitization
* Output Escaping

از APIهای داخلی WordPress مثل:

`sanitize_*`

`esc_*`

`wp_nonce_*`

`current_user_can()`

و APIهای استاندارد WordPress در جای مناسب استفاده کن.

## 7. Responsive

قالب را در این اندازه‌ها بررسی کن:

320
375
390
414
768
1024
1440

نباید:

* Horizontal Scroll ناخواسته
* Layout Broken
* Text Overflow
* Button Overflow
* Menu Broken

وجود داشته باشد.

## 8. Performance

بررسی کن:

* CSS/JS اضافی
* Assetهای تکراری
* Queryهای غیرضروری
* تصاویر سنگین
* فایل‌های بلااستفاده
* Render Blocking غیرضروری

اما برای Performance، ظاهر و عملکرد سایت مرجع را خراب نکن.

## 9. تست نهایی

بعد از اصلاحات، تمام این موارد را واقعاً تست کن:

* Frontend
* Mobile
* Desktop
* Navigation
* Search
* Forms
* Admin Panel
* Theme Settings
* Save / Update
* AJAX
* Pages
* Posts
* Archives
* Single
* 404

هر Bug باید با این چرخه بررسی شود:

`Find → Reproduce → Root Cause → Fix → Retest`

بعد از تمام Fixها یک Regression Test کامل انجام بده تا اصلاح یک بخش باعث خرابی بخش دیگر نشده باشد.

## قانون مهم

هیچ قابلیت موجود را بدون دلیل حذف نکن.

هیچ UI را فقط برای اینکه ظاهرش درست شود Fake نکن.

هر گزینه‌ای که در Admin وجود دارد باید واقعاً کار کند.

هر بخش سایت مرجع که در قالب فعلی وجود ندارد و برای رسیدن به شباهت لازم است، اضافه یا اصلاح شود.

در پایان گزارش بده:

* چه اختلاف‌هایی با سایت مرجع پیدا شد
* چه Bugهایی پیدا و رفع شد
* چه بخش‌هایی از Admin اصلاح شد
* چه قابلیت‌هایی تست شدند
* چه مشکلاتی باقی مانده‌اند

تا زمانی که بخش‌های اصلی تست نشده‌اند، پروژه را Ready اعلام نکن.
