# داشبورد مدیریت باشگاه ورزشی

یک داشبورد کامل و زیبا برای مدیریت باشگاه‌های ورزشی با استفاده از HTML، CSS (Tailwind CSS)، و JavaScript.
<img width="1891" height="901" alt="image" src="https://github.com/user-attachments/assets/249d9100-ef6a-4d19-a274-1ce416f86121" />
<img width="1902" height="874" alt="image" src="https://github.com/user-attachments/assets/fadc9391-f124-437f-8b33-3087cbeef10c" />



## ویژگی‌ها

### 🎨 طراحی و ظاهر
- طراحی مدرن و زیبا با Tailwind CSS
- پشتیبانی کامل از راست‌به‌چپ (RTL)
- فونت فارسی «وزیرمتن» از Google Fonts
- حالت تاریک/روشن (Dark/Light Mode)
- ریسپانسیو و سازگار با موبایل

### 📊 نمودارها و آمار
- نمودار خطی رشد اعضا
- نمودار دایره‌ای (Donut) سهم درآمد
- نمودار میله‌ای ورودی ماهانه
- کارت‌های آماری با رنگ‌بندی متمایز

### 🧩 بخش‌های مختلف
- **داشبورد اصلی**: آمار کلی، نمودارها، و فعالیت‌های اخیر
- **اعضا**: مدیریت اعضا با جدول قابل فیلتر
- **کلاس‌ها**: مدیریت برنامه کلاس‌ها
- **اشتراک‌ها**: مدیریت اشتراک‌ها و تمدیدها
- **گزارش‌ها**: نمودارهای تحلیلی پیشرفته
- **پروفایل**: ویرایش اطلاعات کاربری
- **تنظیمات**: تنظیمات عمومی سیستم

### 🔧 قابلیت‌های فنی
- بدون وابستگی به فریم‌ورک‌های سنگین
- استفاده از Chart.js برای نمودارها
- localStorage برای ذخیره تنظیمات
- CSS Grid و Flexbox برای صفحه‌بندی
- انیمیشن‌های نرم و طبیعی

## ساختار فایل‌ها

```
باشگاه/
├── index.html          # صفحه اصلی داشبورد
├── members.html        # مدیریت اعضا
├── classes.html        # مدیریت کلاس‌ها
├── subscriptions.html  # مدیریت اشتراک‌ها
├── reports.html        # گزارش‌ها و نمودارها
├── profile.html        # پروفایل کاربری
├── settings.html       # تنظیمات
└── README.md          # این فایل
```

## نحوه استفاده

### راه‌اندازی سریع
1. فایل‌ها را دانلود کنید
2. فایل `index.html` را در مرورگر باز کنید
3. از منوی کناری بین صفحات مختلف جابه‌جا شوید

### تنظیمات
- **تغییر تم**: از دکمه ماه/خورشید در هدر استفاده کنید
- **منوی موبایل**: روی آیکون همبرگر در گوشه راست بالا کلیک کنید
- **جستجو**: از نوار جستجو در هدر صفحات استفاده کنید

## فناوری‌های استفاده شده

### Frontend
- **HTML5**: ساختار صفحات
- **CSS3**: استایل‌دهی پیشرفته
- **Tailwind CSS**: فریم‌ورک CSS utility-first
- **JavaScript (Vanilla)**: تعاملات و رفتار صفحه

### کتابخانه‌ها
- **Chart.js**: نمودارهای تعاملی
- **Google Fonts**: فونت فارسی وزیرمتن
- **Feather Icons**: آیکون‌های SVG

### ویژگی‌های CSS
- CSS Grid Layout
- Flexbox
- CSS Variables (Custom Properties)
- Media Queries ریسپانسیو
- Backdrop Filter
- CSS Transitions

## سفارشی‌سازی

### تغییر رنگ‌ها
در فایل‌های HTML، رنگ‌های brand را در بخش Tailwind config تغییر دهید:

```javascript
colors: {
  brand: {
    50: '#eff6ff',   // آبی روشن
    500: '#3b82f6',  // آبی اصلی  
    900: '#1e3a8a'   // آبی تیره
  }
}
```

### اضافه کردن صفحه جدید
1. فایل HTML جدید ایجاد کنید
2. ساختار مشابه صفحات موجود را کپی کنید
3. لینک صفحه را به منوی کناری اضافه کنید
4. آیکون مناسب از Feather Icons انتخاب کنید

### تغییر فونت
در head هر صفحه، لینک Google Fonts را تغییر دهید:

```html
<link href="https://fonts.googleapis.com/css2?family=YOUR_FONT&display=swap" rel="stylesheet">
```

## مرورگرهای پشتیبانی شده

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## مزایا

✅ **سرعت بالا**: بدون فریم‌ورک سنگین  
✅ **قابل نگهداری**: کد تمیز و ساده  
✅ **ریسپانسیو**: عملکرد عالی روی موبایل  
✅ **دسترسی‌پذیری**: ARIA labels و semantic HTML  
✅ **SEO دوست**: ساختار HTML استاندارد  
✅ **قابل توسعه**: معماری منعطف  

## نکات توسعه

### اضافه کردن نمودار جدید
```javascript
var newChart = new Chart(ctx, {
  type: 'line',
  data: { /* داده‌ها */ },
  options: {
    responsive: true,
    maintainAspectRatio: false,
    // سایر تنظیمات
  }
});
```

### مدیریت حالت تاریک
```javascript
// تشخیص تم فعلی
const isDark = document.documentElement.classList.contains('dark');

// تغییر تم
document.documentElement.classList.toggle('dark');
localStorage.setItem('theme', isDark ? 'light' : 'dark');
```

## مجوز

این پروژه تحت مجوز MIT منتشر شده است.



---

**نسخه**: 1.0.0  
**آخرین به‌روزرسانی**: 2024  
**زبان**: فارسی (Persian/Farsi)


