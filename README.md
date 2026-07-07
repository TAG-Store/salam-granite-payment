# AL-SALAM GRANITE – Payment Page

صفحة دفع فاخرة (Luxury Design) لمصنع السلام الصيني للجرانيت المصري، بخلفية سوداء وتفاصيل ذهبية، مبنية بـ HTML + CSS + JavaScript فقط بدون أي مكتبات Frontend خارجية. الصفحة تعرض وسائل الدفع (Instapay – Vodafone Cash – Etisalat Cash) مع زر نسخ الرقم، وQR Code رسمي حقيقي من تطبيق Instapay نفسه.

## الملفات

```
salam-granite/
├── index.html        # الصفحة الرئيسية (بنية HTML)
├── style.css          # كل التنسيقات (تصميم أسود/ذهبي فاخر + Responsive)
├── script.js           # وظيفة النسخ
├── instapay-qr.jpg    # صورة QR الرسمي من تطبيق Instapay (jjalp@instapay)
└── README.md           # هذا الملف
```

## وسائل الدفع المعروضة

| الوسيلة        | الرقم         |
|----------------|---------------|
| Instapay       | 01091855903   |
| Vodafone Cash  | 01000462112   |
| Etisalat Cash  | 01146618871   |

## ملاحظة مهمة عن الـ QR

الـ QR في هذه الصفحة **ليس مولّدًا تلقائيًا من رابط الموقع**، بل هو صورة ثابتة (`instapay-qr.jpg`) لكود QR رسمي تم توليده من داخل تطبيق Instapay نفسه (IPA: `jjalp@instapay`). هذا يعني:

- لازم يتم مسحه (Scan) **من خلال تطبيق Instapay مباشرة** (مش أي كاميرا عادية) عشان يفتح شاشة التحويل جاهزة بالبيانات.
- لو غيّرت الـ IPA أو احتجت تحدّث الـ QR، لازم تولّد صورة جديدة من تطبيق Instapay وتستبدل بيها ملف `instapay-qr.jpg` بنفس الاسم.

## خطوات الرفع على GitHub

1. أنشئ مستودع جديد على [github.com](https://github.com)، مثلًا باسم: `salam-granite-payment`.
2. اجعله **Public**، بدون تفعيل إضافة README تلقائيًا.
3. ارفع الملفات الخمسة (`index.html`, `style.css`, `script.js`, `instapay-qr.jpg`, `README.md`) عبر:
   - **Add file → Upload files** من المتصفح مباشرة، أو
   - عبر Git من جهازك:
   ```bash
   git init
   git add .
   git commit -m "Initial commit - Al-Salam Granite payment page"
   git branch -M main
   git remote add origin https://github.com/USERNAME/salam-granite-payment.git
   git push -u origin main
   ```

## خطوات النشر على Vercel

1. ادخل على [vercel.com](https://vercel.com) وسجّل الدخول بحساب GitHub.
2. **Add New... → Project** → استورد المستودع `salam-granite-payment`.
3. سيب الإعدادات كما هي (Framework: Other، بدون Build Command).
4. اضغط **Deploy**.
5. بعد ثوانٍ هتحصل على رابط مباشر شبيه بـ:
   ```
   https://salam-granite-payment.vercel.app
   ```

كل مرة تحدّث أي ملف على GitHub (زي تغيير صورة الـ QR أو تعديل رقم)، Vercel هيعمل نشر جديد تلقائيًا خلال دقيقة أو اتنين.
