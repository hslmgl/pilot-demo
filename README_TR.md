# Pilot v3.2 — Yerel AI Yönlendirme

Pilot, gizlilik odaklı akıllı galeri asistanıdır.

## Bu sürümün ana değişikliği

Ana ekrandaki metin alanı artık yalnızca sabit komut aramaz. Kullanıcının günlük dilde, eksik, hatalı veya belirsiz biçimde anlattığı sorunu cihaz içinde yorumlayarak en yakın üç işlemi önerir.

Örnekler:

- “Telefonum doldu ama neyi silsem bilmiyorum” → Depolamada yer aç
- “Galerim çok karışık, hiçbir şeyi bulamıyorum” → Galeriyi düzene sok
- “Aynı şeyden çok var galiba” → Benzer ve olası kopyaları bul
- “Sonra bakarım diye bir sürü şey kaydetmişim” → Ekran görüntülerini düzenle
- “Eskiden kalanlara bakmak istiyorum” → Eski medyaları gözden geçir

## Yerel AI motoru

Motor tamamen tarayıcı içinde çalışır ve şunları birlikte kullanır:

- Türkçe metin normalizasyonu
- Yazım hatası düzeltme
- Türkçe ekleri sadeleştirme
- Anlam kavramları ve problem örüntüleri
- Karakter benzerliği ve kelime örtüşmesi
- Birden fazla olası sonuç üretme
- Güven düzeyi gösterme
- Kullanıcının seçtiği yönlendirmeleri yalnızca cihazda hatırlama
- “Evet”, “tamam”, “devam” gibi bağlamsal kısa cevapları anlama

Net olmayan bir istekte Pilot kullanıcı adına kesin karar vermez. En yakın seçenekleri sunar ve seçimi kullanıcıya bırakır.

## Sürüm görünürlüğü

Sürüm numarası uygulamanın sol üst kısmında kalıcı olarak gösterilir. Bu paket `v3.2` olarak işaretlenmiştir.

## Tarama ve işlem güvenliği

- Galeri, klasör ve albüm seçimi kullanıcı onayıyla yapılır.
- Seçilen medyanın analizi cihaz içinde gerçekleştirilir.
- Pilot önerir; son kararı kullanıcı verir.
- Onay olmadan silme, taşıma veya düzenleme işlemi uygulanmaz.

## Android APK aşaması

PWA içindeki yerel yönlendirme motoru tüm cihazlarda hızlı bir geri dönüş katmanı olarak korunacaktır. Uyumlu Android cihazlarda daha gelişmiş doğal dil anlama için cihaz üzerindeki üretken model katmanı eklenebilir; desteklenmeyen cihazlarda v3.2 motoru çalışmaya devam eder.
