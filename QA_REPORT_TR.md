# Pilot v3.5 — Dört Uzman QA Raporu

## İnceleme kapsamı

Son 9 gereksinim, Pilot manifestosu, mobil ekran akışı, yerel AI yönlendirmesi, işlem devamlılığı, geçmiş ve geri alma davranışı incelendi.

## 1. Kıdemli Mobil Uygulama Geliştiricisi

**Kontrol edilenler**

- Alt menüde yalnızca Ana Sayfa, Araçlar, Geçmiş ve Ayarlar bulunması
- İşlem ekranlarının ayrı rota olması fakat alt menüye eklenmemesi
- Genel galeri, albüm ve klasör kapsamlarının her işlemde sorulması
- Seçilen işlem dışında analiz kartı üretilmemesi
- Silme, albüm, taşıma, düzenleme, kopya, ekran görüntüsü ve büyük medya kitlerinin bağımsız çalışması
- Aktif işlemin sayfa geçişlerinde korunması

**Karar:** PWA uygulama mantığı için onaylandı.

## 2. UI/UX Tasarımcısı

**Kontrol edilenler**

- Ana sayfanın sade ve tek odaklı olması
- Dört önerinin modal alt panelde sunulması
- Panelin çarpı ve dış alanla kapanabilmesi
- İşlem sayfalarının ana navigasyondan ayrıştırılması
- Analiz ekranındaki sabit İŞLEMLER düğmesinin erişilebilir kalması
- Koyu/açık tema ve kompakt görünümün gerçek arayüzü değiştirmesi
- Yıkıcı eylemlerde onay adımı

**Karar:** Onaylandı.

## 3. Mobil Ürün Yöneticisi

**Kontrol edilenler**

- “Pilot önerir, kullanıcı karar verir” ilkesinin tüm akışta korunması
- İlk taramanın salt okunur olması
- Her işlemin kapsam ve son onayla ilerlemesi
- Kullanıcının aktif görevini kaybetmemesi
- Geçmiş ve geri alma ile güven oluşturulması
- Fazladan alt menü sayfası eklenmemesi
- Araç kitlerinin belirgin kullanıcı problemlerine karşılık gelmesi

**Karar:** PWA ürün kapsamı için onaylandı.

## 4. Mobil Yazılım Mühendisi

**Kontrol edilenler**

- İş akışı durum makinesi: kapsam → tarama → analiz → aksiyon
- Ana sayfada 4 dinamik öneri, araç kitlerinde 3 dinamik öneri
- Yerel öğrenme ağırlıklarının cihaz içinde saklanması
- Tarama sürerken başka sayfaya geçildiğinde işlemin devam etmesi
- Uygulanan işlem için önce/sonra durumunun kaydedilmesi
- Geri almanın yalnızca ilgili değişiklikleri tersine çevirmesi
- Servis çalışanı önbellek sürümünün v3.5 olarak ayrılması

**Karar:** Onaylandı.

## Otomatik mobil tarayıcı testleri

Chromium, 390×844 mobil ekran boyutunda iki senaryo grubu çalıştırıldı.

### Ana akış testleri — 16/16 geçti

- v3.5 etiketi
- Dört alt menü düğmesi
- Giriş cümlesinden dört farklı öneri
- Pop-up çarpı ve dış alan kapatma
- Gizli işlem rotasına geçiş
- Kırmızı araba sorgusunda dört doğru sonuç
- Sabit İŞLEMLER düğmesi
- Üç AI aksiyonu
- Albüm oluşturma
- Geçmiş kaydı
- Geri alma
- Araç kitinde üç seçenek
- Sayfa değişiminde kaldığı yerden devam
- Tema ayarı
- Kompakt görünüm
- JavaScript çalışma zamanı

### Yıkıcı işlem ve geri alma testleri — 6/6 geçti

- Silme kitinin yalnızca ekran görüntülerini ayıklaması
- Silme işleminin geçmişe kaydolması
- Silinen öğelerin geri alınması
- Analiz aşamasının sayfa geçişinden sonra korunması
- Geçmiş kaydının silinmesi
- Aksiyon senaryolarında JavaScript hatası bulunmaması

## Düzeltilen kritik hata

İlk QA turunda geri alma sırasında `undefined` bir alanın JSON kopyasına alınması JavaScript hatasına yol açtı. Kopyalama yardımcısı ve alan bazlı geri alma algoritması düzeltildi. Düzeltme sonrasında iki test grubu yeniden çalıştırıldı ve tümü geçti.

## Dürüst kapsam notu

GitHub Pages/PWA, Android ortak galerisindeki fiziksel dosyaları sistem düzeyinde silme veya taşıma yetkisine sahip değildir. Bu sürümde işlemler Pilot’un gerçek uygulama durumu, albümleri, seçili medya kayıtları, geçmişi ve geri alma sistemi üzerinde çalışır.

Fiziksel Android galeri değişiklikleri için aynı iş akışının MediaStore izinleriyle native APK içine aktarılması gerekir. Bu sınırlama saklanmamış ve uygulamada olmayan yetenek varmış gibi sunulmamıştır.
