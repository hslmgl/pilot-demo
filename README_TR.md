# Pilot v3.5 — İş Akışı ve Yerel AI Sürümü

Bu sürüm, ürün manifestosu ve son 9 maddelik gereksinim listesine göre yeniden kurulmuştur.

## Alt menü
Yalnızca dört ana sayfa vardır:

1. Ana Sayfa
2. Araçlar
3. Geçmiş
4. Ayarlar

İşlem, kapsam seçimi, tarama ve analiz ekranları alt menüde ayrı düğme olarak yer almaz.

## Ana Sayfa
- Kullanıcı doğal dilde veya eksik bir cümleyle isteğini yazar.
- Yerel yönlendirme motoru cümleyi niyet ve hedef açısından değerlendirir.
- Kullanıcının cümlesine bağlı dört farklı öneri oluşturulur.
- Öneriler alt panel biçiminde açılır.
- Panel sağ üstteki çarpıdan veya dış alana dokunularak kapanabilir.

## Araçlar
- Silme
- Akıllı albüm
- Taşıma
- Düzenleme
- Benzer ve kopyalar
- Ekran görüntüleri
- Büyük medya

Her kit, kullanıcının yazdığı hedefe göre üç kit-özel seçenek oluşturur.

## İşlem akışı
1. İşlem seçilir.
2. Genel galeri, albüm veya klasör kapsamı sorulur.
3. Yalnızca seçilen işlem amacıyla tarama yapılır.
4. Ayıklanan sonuçlar analiz ekranında gösterilir.
5. Ekranın altında sabit `İŞLEMLER · 3 ÖNERİ` düğmesi bulunur.
6. Kullanıcının isteğine bağlı üç aksiyondan biri uygulanır.

## İşlem devamlılığı
Kullanıcı başka ana sayfaya geçtiğinde aktif iş akışı kaybolmaz. Ana sayfalarda görünen “Devam eden işlem” kartı, kapsam, tarama veya analiz aşamasını kaldığı yerden açar.

## Geçmiş ve geri alma
Her uygulanan işlem geçmişe kaydedilir. Kayda dokunulduğunda:

- Kaydı sil
- İşlemi geri al

seçenekleri açılır. Geri alma, işlemin değiştirdiği öğe ve albüm alanlarını tersine çevirirken daha sonra yapılmış bağımsız değişiklikleri mümkün olduğunca korur.

## Ayarlar
Tema, analiz derinliği, onay düzeyi, düşük güvenli sonuçlar, favori koruması, yerel öğrenme, kompakt görünüm ve varsayılan kapsam vurgusu gerçek davranışlara bağlıdır.

## Önemli teknik kapsam
Bu paket GitHub Pages üzerinde çalışan PWA sürümüdür. Pilot içindeki albüm, taşıma, kopyalama, silme, geçmiş ve geri alma işlemleri gerçekten uygulanır.

Tarayıcı, Android ortak galerideki fiziksel dosyaları doğrudan silme veya taşıma yetkisi vermez. Telefonun gerçek MediaStore koleksiyonunu değiştiren sürüm native Android APK içinde sistem onayıyla uygulanmalıdır. Bu PWA, bu yetkiye sahipmiş gibi davranmaz.
