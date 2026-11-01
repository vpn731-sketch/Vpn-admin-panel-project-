# TOOFAN V2RAY Android Client — Starter

এটি Android Studio-তে খোলা যায় এমন native Kotlin client skeleton। এটি HTTPS API login, encrypted bearer-token storage (Android Keystore), `/me` এবং `/servers` endpoint থেকে তথ্য পড়ার ভিত্তি দেয়। আসল logo asset APK resources নয়, assets folder থেকে UI-তে লোড হয়।

## Build
1. Android Studio-তে `android-client` folder open করুন।
2. Gradle sync করুন (JDK 17, Android SDK 35 প্রয়োজন)।
3. `API_BASE_URL` আপনার HTTPS backend URL দিয়ে দিন, উদাহরণ: `./gradlew assembleDebug -PAPI_BASE_URL=https://vpn.example.com/api/v1`।
4. Debug APK: `app/build/outputs/apk/debug/app-debug.apk`।

## গুরুত্বপূর্ণ
- এই starter-এ Xray native core/AAR/JNI glue bundled নয়। তাই Connect disabled; কোনো VPN tunnel শুরু হয় না।
- Official libXray Android artifact build ও integrate করতে হবে; `docs/XRAY_ANDROID_INTEGRATION_BN.md` দেখুন।
- API server URL অবশ্যই HTTPS হতে হবে।
- এখানে কোনো free-data, carrier billing bypass বা operator data-cap bypass functionality নেই।
