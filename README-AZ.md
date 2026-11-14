# 🏁 BAKU RUSH v2 — Azneft ➜ Hövsan

Eninə oynanan mobil yarış oyunu. 5 zolaqlı yolda Azneft dairəsindən Bulvar boyu Hövsana qədər sürürsən.
Bütün oyun bir fayldadır: `www/index.html`.

## 🆕 v2-də nə dəyişdi
- **Xəta düzəldi:** bir sürüşdürmə artıq həmişə yalnız **1 zolaq** keçir.
- **Eninə ekran** (landscape) və **5 zolaqlı yol**.
- **Marşrut:** Azneft — Bulvar → Park Bulvar → Port Baku → Crescent Mall → Çinar Plaza → Zığ neft mədənləri → Hövsan. Yolun üstündə yaşıl istiqamət lövhələri var: "Siz buradasınız / Hövsan X km".
- **Qıl atmaq:** zolaq dəyişən kimi maşının yanından keçsən 🐍 QIL ATDIN olur: ikiqat xal və çox nitro. İki maşının arasından keçsən 🧵 İYNƏ GÖZÜ olur: +200.
- **📯 Korna:** qabaqdakı maşın siqnal verib yol verir.
- **Telefonu əyməklə idarə** (Ayarlar → İdarəetmə → Əyməklə). Həssaslığı 3 səviyyədə seçmək olar.
- **Düymə rejimi:** ekranda ◀ ▶ düymələri çıxır.
- **9 realist maşın:** Klassik 07, Şəhər Sedanı, Bakı Taksi, **Biznes Van (ağ, 99-XZ-785)**, **Premium SUV (ağ, 99-CC-877)**, Polis, Qutu SUV, Sport Kupe, Hiper X.
- Yoldakı trafik də realistdir: sedan, hetçbek, SUV, mikroavtobus, taksi, köhnə maşınlar, yük maşınları və avtobuslar.
- **Bakı ikonu:** Alov Qüllələri, dəniz və yol.

> ⚠️ Real markaların adları və loqoları (Audi, Mercedes və s.) oyuna qoyulmayıb. Google Play icazəsiz marka istifadəsinə görə tətbiqi rədd edir. Traffic Racer kimi oyunlar da eyni səbəbdən uydurma adlardan istifadə edir. Maşınlar görünüşcə real siniflərə oxşayır: böyük ağ SUV, ağ mikroavtobus və s.

## 📁 Qovluq
```
baku-rush/
├── www/index.html                 ← OYUN
├── .github/workflows/build-apk.yml← GitHub-da avtomatik APK yığımı
├── capacitor.config.json          ← paket adı: az.qrbs.bakurush
├── package.json
├── res/icons/                     ← Android ikonları (5 ölçü)
├── assets/icon.png                ← 1024×1024 ikon
└── assets/icon-512-playstore.png  ← Play Market üçün ikon
```

## 📦 APK — 1-ci yol: GitHub (kompüter lazım deyil)
1. https://github.com saytında hesab aç və **New repository** yarat (məsələn `baku-rush`).
2. **Add file → Upload files** seç. Bu qovluğun **bütün** fayllarını yüklə, `.github` qovluğu da daxil olmaqla. Sonra **Commit changes** bas.
   (Telefondan `.github` qovluğu yüklənmirsə: **Add file → Create new file** seç, adını `.github/workflows/build-apk.yml` yaz və faylın mətnini içinə yapışdır.)
3. **Actions** bölməsinə keç. "Build APK" avtomatik başlayacaq, təxminən 5–8 dəqiqə çəkir.
4. Yaşıl ✓ çıxandan sonra işə daxil ol. Aşağıda **Artifacts → BakuRush-APK** var. Yüklə, zip-i aç, `BakuRush.apk` faylını telefona quraşdır.

## 📦 APK — 2-ci yol: Android Studio
```bash
npm install
npx cap add android
npx cap sync android
npx cap open android
```
Sonra:
- `android/app/src/main/AndroidManifest.xml` faylında `<activity` sətrinə `android:screenOrientation="sensorLandscape"` əlavə et.
- **Build → Build APK(s)** seç.

## 🏪 Google Play
Göndərmək üçün imzalı `.aab` lazımdır: **Build → Generate Signed Bundle**. Play Console hesabı birdəfəlik 25$-dır. Yeni şəxsi hesablar üçün əvvəlcə 12 testçi ilə 14 günlük qapalı test tələb olunur.
Play Market ikonu: `assets/icon-512-playstore.png`.
