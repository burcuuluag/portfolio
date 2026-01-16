# DEU Sosyal Bilimler Duyuru Botu

Bu bot, Dokuz Eylül Üniversitesi Sosyal Bilimler Enstitüsü'nün (SBE) RSS feed'ini kullanarak yayınlanan en güncel duyuruları takip eder. Yeni bir duyuru tespit edildiğinde, otomatik olarak belirlenen Telegram kanalına detayları (başlık, link, tarih) iletir.

### Öne Çıkan Özellikler:

* **Asenkron Çalışma:** `asyncio` altyapısı ile sistem kaynaklarını yormadan çalışır.
* **Birim Testleri (Unit Testing):** Proje, `unittest` ve `mock` kütüphaneleriyle test edilmiş fonksiyonlara sahiptir.
* **Akıllı Filtreleme:** Sadece sisteme daha önce düşmemiş olan "yeni" duyuruları ayıklar ve gönderir.

## Kurulum
```bash
# Depoyu klonlayın
git clone <repo-url>
cd <proje-klasörü>

# Gerekli bağımlılıkları yükleyin
pip install -r requirements.txt