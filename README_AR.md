# الحظ (AL HAZZ) — مشروع Flutter

## محتويات المشروع
- تطبيق Android مكتوب بـ Flutter.
- واجهة عربية/فرنسية/إنجليزية.
- ملف `codemagic.yaml` لبناء APK على Codemagic.
- جلب المباريات من خدمة خلفية Netlify Functions.

## مهم قبل أن تعمل البيانات
في `lib/main.dart` غيّر:
`https://YOUR-SITE.netlify.app/.netlify/functions`
إلى عنوان Netlify الحقيقي بعد نشر وظائف البيانات. لا تضع مفتاح API-Football داخل التطبيق أو GitHub.

## رفع المشروع إلى GitHub
1. أنشئ مستودعاً جديداً باسم `al-hazz`.
2. ارفع كل محتويات هذا المجلد إلى جذر المستودع، وليس ملف ZIP نفسه.
3. افتح Codemagic واربط حساب GitHub.
4. اختر مستودع `al-hazz`، ثم ملف الإعداد `codemagic.yaml`.
5. ابدأ البناء، وبعد نجاحه نزّل `app-release.apk` من Artifacts.

## ملاحظة
هذه نقطة انطلاق لبناء APK. لا تعمل بيانات المباريات حتى تنشر خدمة Netlify الخلفية وتضع عنوانها في التطبيق. يجب إعداد API-Football Key كمتغير سري في Netlify باسم `API_FOOTBALL_KEY`.
