# RİTİM Android — APK build package

Bu paket mevcut RİTİM web prototipini Capacitor ile Android uygulaması olarak paketlemek için hazırlanmıştır.

## APK oluşturma (bilgisayara Android Studio kurmadan)

1. GitHub hesabında yeni, **private** bir repository oluştur: `ritim-android`.
2. Bu ZIP'in içeriğini repository'nin ana dizinine yükle (ZIP dosyasının kendisini değil, içindeki dosyaları).
3. GitHub'da **Actions** sekmesine gir.
4. `Build RITIM APK` iş akışını seç ve **Run workflow** düğmesine bas. İlk yüklemede workflow otomatik görünmezse `main` dalına `.github/workflows/build-apk.yml` dosyasının geldiğini kontrol et.
5. İşlem yeşil tik ile tamamlanınca ilgili çalışmayı aç, **Artifacts** bölümündeki `RITIM-Android-debug-APK` dosyasını indir.
6. İnen ZIP'i aç. İçindeki `app-debug.apk` dosyasını Galaxy S22'ye gönder ve telefonda açarak kur.

## Önemli sınırlar

- Bu bir **debug APK**'dır; ilk cihaz testleri içindir, Play Store yayını için imzalı release paketi değildir.
- Uygulama mevcut web arayüzünü Android WebView/Capacitor içinde çalıştırır.
- Görev ve rutin verileri şu an cihazdaki uygulama depolamasında kalır. Bulut hesabı/senkronizasyon henüz bağlı değildir.
- Mevcut hatırlatma kodu Android'de güvenilir arka plan alarmı sağlamaz. Yerel bildirim/alarmlar, Android izinleri ve yeniden başlatma sonrası geri yükleme sonraki geliştirme aşamasıdır.
- APK üretimi GitHub Actions üzerinde yapılır; bu paket tek başına APK değildir.

## Paket kimliği

`com.fatih.ritim`
