# 9. Şebeke Ara Katman Yazılımı (Grid Middleware) - Ders Notları

## 9.1 Tanım ve Kapsam

### Grid Sistemleri Bileşenleri:

| Bileşen | Örnekler |
|---------|----------|
| **Hesaplama Kaynakları** | Süper bilgisayarlar, sunucular, kümeler |
| **Depolama Kaynakları** | Disk sistemleri, NAS |
| **Ağ Kaynakları** | Yönlendiriciler, anahtarlar |
| **Bilimsel Araçlar** | Teleskoplar, sensör ağları |

**Grid Fabric (Şebeke Dokusu):** Tüm kaynakların bütünü

### Ara Katman Yazılımı Tanımı: 
Kullanıcılara heterojen şebeke ortamında **kesintisiz bilgi işlem yeteneği** ve kaynaklara **tek tip erişim** sağlayan yazılım.

## 9.2 Ara Katman Yazılımının Amaçları

1. **Kaynak Erişimi**:  Şebeke kaynaklarına erişim sağlamak
2. **Kullanımı Kolaylaştırma**: Kaynakların kolay kullanımı
3. **Kaynak Sağlayıcıyı Koruma**: Sağlayıcı çıkarlarını koruma

### Gerekli Özellikler: 
- Paylaşılabilirlik
- Yeniden Kullanılabilirlik
- Genişletilebilirlik
- Geliştirme süresini minimize etme

## 9.3 Şebeke Portalları (Grid Portals)

**Tanım:** Grid kaynaklarına birleşik ve tutarlı erişim yolu sunan arayüzler. 

### Portlet: 
- Java teknolojisi tabanlı web bileşeni
- İstekleri işler ve dinamik içerik üretir
- **Portlet container** tarafından yönetilir

## 9.4 Portal Geliştirme Araçları

- **GPDK (Grid Portal Development Kit)**
- **GPT (Grid Portal Toolkit)**

## 9.5 GridSphere

**Geliştiren:** GridLab projesi

**Tanım:** Portlet tabanlı web portalı geliştirme ortamı

**Temel Amaçları:**
- İyi entegre edilmiş ve kullanımı kolay portletler oluşturmak
- Çevrimiçi işbirliği
- Hesaplama
- Veri yönetimi
- Veri görüntüleme

**Özellik:** Herhangi bir Grid teknolojisi ile doğrudan bağlantılı değil (yaygın web geliştirme ortamı)

## 9.6 Grid Portletleri

**Tanım:** GridSphere ile işbirliği yapan portlet seti

### Sağladığı İşlevler: 

| İşlev | Açıklama |
|-------|----------|
| **Kimlik Bilgisi Yönetimi** | Credential talebi ve yönetimi |
| **Kaynak Arama** | Grid kaynaklarını bulma |
| **İş Gönderme (Job Submission)** | İşlerin gönderilmesi |
| **Dosya Aktarımı** | Dosya transferi |

**Geliştirici Kullanımı:** Mevcut portletlere dayanarak daha yüksek seviyeli API'ler ile güçlü portletler oluşturulabilir. 