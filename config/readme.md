# راهنمای پیکربندی V2Ray

این مستند به بررسی و توضیح اسم‌فیلدهای رایج در فایل پیکربندی V2Ray می‌پردازد.

## ساختار کلی

```json
{
  "inbounds": [],
  "outbounds": [],
  "routing": {},
  "dns": {},
  "log": {}
}
```

## توضیح اسم‌فیلدها

### inbounds
ورودی‌هایی که سرور V2Ray به آن‌ها گوش می‌دهد. هر ورودی شامل موارد زیر است:
- `port`: شماره پورت ورودی
- `protocol`: پروتکل (مثلاً `vmess`, `vless`, `socks`)
- `settings`: تنظیمات اختصاصی پروتکل
- `streamSettings`: تنظیمات انتقال (مانند TLS, WebSocket)

### outbounds
خروجی‌هایی که ترافیک به آن‌ها ارسال می‌شود.
- `protocol`: پروتکل خروجی (مثلاً `freedom`, `blackhole`, `vmess`)
- `settings`: تنظیمات اختصاصی پروتکل

### routing
قوانین مسیریابی ترافیک.
- `rules`: لیست قوانین مسیریابی
  - `type`: نوع قانون (مثلاً `field`)
  - `ip`, `domain`, `port`: فیلترها
  - `outboundTag`: برچسب خروجی مقصد

### dns
تنظیمات DNS سفارشی.
- `servers`: لیست سرورهای DNS

### log
تنظیمات لاگ‌گیری.
- `loglevel`: سطح لاگ (مثلاً `info`, `warning`, `error`)
- `access`: مسیر فایل لاگ دسترسی
- `error`: مسیر فایل لاگ خطا

---

برای اطلاعات بیشتر به [مستندات رسمی V2Ray](https://www.v2ray.com/) مراجعه کنید.