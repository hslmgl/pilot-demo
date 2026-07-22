# Pilot PWA v3.3 Final

Bu sürümde aşağıdakiler aktif hale getirildi:

- Sol üstte görünür sürüm etiketi: **v3.3**
- ChatGPT/Gemini tarzı sade ana giriş ekranı
- İstek yazarak yönlendirme
- Tüm galeri / klasör / albüm / Pilot Örnek Albümü tarama
- **Pilot Örnek Albümü**
  - 4 kırmızı araba görseli
  - 3 mavi atkılı görsel
  - 2 beyaz güvercin görseli
- Tarama sonrası önerilen işlemler
- İşlem merkezinde çalışan aksiyonlar:
  - **Albüm oluştur**
  - **Taşı**
  - **Kopyala**
  - **Sil**
- Oluşturulan albümler için Albümler ekranı
- İşlem kayıtları için Geçmiş ekranı

## Telefon üzerinden GitHub'a yükleme (özet)
1. GitHub repo aç.
2. `Pilot_PWA_v3.3_Final.zip` dosyasını indir.
3. Zip'i telefonda çıkar.
4. Repo içine tüm dosyaları yükle.
5. `index.html`, `manifest.webmanifest`, `sw.js`, `icons` ve `assets` klasörü birlikte gitmeli.
6. Repo ayarlarından GitHub Pages açılırsa web demo olarak yayınlanabilir.

## Not
Bu PWA sürümünde aksiyonlar **uygulama içinde tepki verir**.
Tarayıcı güvenliği sebebiyle gerçek Android sistem dosyası silme/taşıma işlemi native APK kadar tam yetkili değildir.
