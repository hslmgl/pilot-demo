# Pilot PWA Full Demo v1

Bu sürüm yalnızca Android telefonla test edilmek üzere hazırlanmış kurulabilir bir PWA demosudur.

## Ne yapar?
- Telefon galerisinden kullanıcının seçtiği fotoğraf ve videoları yerel olarak okur.
- Fotoğraf/video sayısı ve toplam boyutu hesaplar.
- Ekran görüntülerini, 100 MB üzerindeki videoları ve aynı tür+boyuttaki olası kopyaları öneri olarak gösterir.
- İnceleme kuyruğu ve işlem simülasyonu sunar.
- Dosya yüklemez, silmez veya taşımaz.
- İnternet kesildiğinde daha önce açılmış sürümü çevrimdışı çalıştırabilir.

## Telefonda yayınlama (GitHub Pages)
1. GitHub'da yeni, public bir depo oluşturun.
2. Bu klasördeki tüm dosyaları depo köküne yükleyin. `index.html` kökte olmalı.
3. Depoda Settings > Pages bölümüne gidin.
4. Source: Deploy from a branch; Branch: main; Folder: /(root) seçin ve Save deyin.
5. GitHub'ın verdiği HTTPS adresini Chrome'da açın.
6. Chrome menüsünden "Ana ekrana ekle" / "Uygulamayı yükle" seçin.

## Önemli sınır
Web/PWA, Android'in tüm galerisini arka planda MediaStore gibi otomatik tarayamaz. Kullanıcı dosyaları seçer. Tam galeri erişimi, gerçek taşıma/silme ve Android medya izinleri için sonraki aşamada native Android uygulaması gerekir.
