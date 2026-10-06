# Avtigo Vehicle Data

Avtigo için sürümlenmiş marka, model, motor, donanım paketi, ekipman ve şanzıman kataloğu. Bulgarca/İngilizce etiketler içerir.

## Kullanım

Yeni seçicilerin kaynağı `data/vehicle-catalog.v2.json` dosyasıdır. `vehicle-makes-models.json` ve `vehicle-trims.json` eski ilan değerlerini koruyan uyumluluk dosyalarıdır. Motor, model kimliği kapsamında; model, marka kimliği kapsamında çözülmelidir. Belirsiz alias için ilk eşleşmeyi seçmeyin.

Uygulama kataloğu build sırasında belirli bir commit SHA üzerinden indirmeli, `manifest.json` SHA-256 değerlerini doğrulamalı ve yerel kopyadan okumalıdır. Her kullanıcı isteğinde GitHub'a bağlanmayın. Güncelleme inceleme, test ve yeni build gerektirir. Etiket değişirken mevcut kimlikleri koruyun.

## Kapsam ve doğruluk

151 marka, 2638 model kaydı, 12833 motor kaydı, 62 ekipman, 40 paket önerisi ve 19 şanzıman teknolojisi bulunur. Devralınan veriler tamamen bağımsız üretici doğrulamasından geçmemiştir; 213 modelin kendi motor listesi yoktur. Yıl/yakıt uyumluluğunu doğrulanmamış veriden tahmin etmeyin. Aday motor havuzları kesin uygunluk değildir. Bilinmeyen motor için kontrollü metin ve inceleme yolu sağlayın.

Donanım paketi seçimi ekipmanları otomatik doğrulamaz. Otomatik şanzıman bilgisi tek başına DSG anlamına gelmez. Teknoloji bilinmiyorsa null kullanın.

`sourceRefs` bilinen genel kaynaklara işaret eder. Galeriye özel kaynak referansları bu public sürümden çıkarılmıştır; boş referans listesi bağımsız doğrulama değildir. `sources.json` başlangıç kaynaklarını içerir. Üçüncü taraf kaynakların hakları saklıdır; bu depo üçüncü taraf verileri için lisans garantisi vermez.

Bu depo yalnız katalog ve form/aktarım sözleşmelerini içerir. Galeri ilanları, kişisel veriler, fotoğraflar, veritabanı bağlantıları veya site uygulama kodu içermez. JSON'lar tek başına uygulamaya entegrasyon sağlamaz.
