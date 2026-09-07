# LUXE — Android APK

این نسخه برای تبدیل پروژه LUXE به اپلیکیشن Android با Capacitor آماده شده است.

## پیش‌نیاز
- Node.js
- Android Studio
- Android SDK
- JDK سازگار با نسخه Android Gradle Plugin پروژه

## ساخت پروژه Android
در پوشه پروژه اجرا کنید:

```bash
npm install
npm run android:build
npx cap open android
```

سپس در Android Studio پروژه را Build کنید.

## ساخت APK از خط فرمان
پس از اجرای `npx cap add android` و sync شدن پروژه:

```bash
cd android
./gradlew assembleDebug
```

فایل APK معمولاً در مسیر زیر ساخته می‌شود:

`android/app/build/outputs/apk/debug/app-debug.apk`

## Supabase
فایل `.env.example` را به `.env` تبدیل کنید و این متغیرها را قرار دهید:

```env
VITE_SUPABASE_URL=...
VITE_SUPABASE_ANON_KEY=...
```

سپس دوباره build بگیرید.

## نکته
پوشه `android/` عمداً در این بسته ایجاد نشده است؛ Capacitor آن را با `npx cap add android` بر اساس محیط Android شما تولید می‌کند. این کار باعث می‌شود Android Studio/SDK محلی شما نسخه native سازگار را ایجاد کند.
