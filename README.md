# Dns Yar – data files

این مخزن فقط دو فایل عمومی دارد که برنامه‌ی Dns Yar هنگام باز شدن آن‌ها را می‌خواند. هیچ کد یا رمزی در آن نگذارید.

## dns-list.json  (لیست DNS)
- `servers`: سرورهای جدید. نمونه:
  { "name": "نام", "ips": ["1.2.3.4", "1.2.3.5"], "cc": "us", "cat": "public", "tags": ["gaming"], "alias": "کلمه‌های جستجو" }
  - `cat`: public | security | isp | unblock
  - `tags`: ["gaming"] برچسب آبی Gaming DNS را می‌دهد
- `remove`: لیست IP اول (اصلی) سرورهایی که باید از برنامه حذف شوند، مثلاً ["8.8.8.8"].
- هر بار که فایل را عوض می‌کنید `version` و `updated` را هم عوض کنید.

## update.json  (آپدیت برنامه)
- `version`: آخرین نسخه‌ی برنامه. اگر از نسخه‌ی کاربر بالاتر باشد، یک نوار آبی «نسخه‌ی جدید» نشان داده می‌شود.
- `minVersion`: پایین‌ترین نسخه‌ی مجاز. نسخه‌های پایین‌تر صفحه‌ی «به‌روزرسانی لازم است» می‌بینند. فقط وقتی لازم است بالا ببرید.
- `url`: لینک دانلود/صفحه‌ی آپدیت (خالی = صفحه‌ی فروشگاه).

## لینک‌ها (در dns.js، بخش CONFIG)
```js
updateJsonUrls: ['https://raw.githubusercontent.com/USERNAME/REPO/main/update.json'],
remoteListUrls: ['https://raw.githubusercontent.com/USERNAME/REPO/main/dns-list.json'],
```
USERNAME و REPO را عوض کنید. اگر GitHub Pages را روشن کنید، لینک پشتیبان: `https://USERNAME.github.io/REPO/dns-list.json`
