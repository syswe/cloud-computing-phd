# 2. Şebeke Hesaplamaya Giriş (Introduction to Grid Computing) - Ders Notları

## 2.1 Grid Tanımı ve Tarihçesi

**Grid kavramı** ilk olarak **1998'de Foster ve Kesselman** tarafından ifade edilmiştir. 

### Ian Foster'ın Grid Kontrol Listesi (3 Madde):

1. **Merkezi Kontrol Olmaması**: Farklı yönetim etki alanlarında bulunan kaynakların koordineli paylaşımı
2. **Açık Standartların Kullanımı**: Standart, açık ve genel amaçlı protokoller ve arayüzler
3. **Hizmet Kalitesi**: Verim, yanıt süresi veya güvenlik gibi metriklerle ölçülebilir hizmetler

## 2.2 Grid'de Paylaşılabilecek Temel Kaynaklar

- Bilgi işlem/işlem gücü
- Veri depolama/ağ bağlantılı dosya sistemleri
- İletişim ve bant genişliği
- Uygulama yazılımı
- Bilimsel araçlar

## 2.3 Temel Kavramlar

| Kavram | Tanım |
|--------|-------|
| **Grid Ara Yazılımı** | Heterojen kaynakların paylaşımını ve VO kurulmasını sağlayan yazılım |
| **Grid Computing** | Dinamik toplulukta esnek, güvenli ve koordineli kaynak paylaşımı |
| **Grid Altyapısı** | Donanım ve Grid ara yazılımının birleşimi |
| **Yardımcı (Utility) Bilişim** | "Kullanım başına ödeme" iş modeli |

## 2.4 Grid İle İlgili Standart Kuruluşları

| Kuruluş | Açıklama |
|---------|----------|
| **GGF (Global Grid Forum)** | Grid için birincil standart belirleyici |
| **OASIS** | Kâr amacı gütmeyen standartlar konsorsiyumu |
| **DMTF** | Açık yönetilebilirlik standartları |
| **W3C** | Web servisleri ve XML standartları |

### GGF Belge Türleri:
1. **Bilgilendirici (Informational)**
2. **Deneysel (Experimental)**
3. **Topluluk Uygulaması (Community Practice)**
4. **Öneriler (Recommendations)** - Örnek:  OGSA

## 2.5 OGSA (Açık Şebeke Hizmetleri Mimarisi)

- Grid tabanlı uygulamalar için ortak, standart ve açık mimari
- **Hizmet Odaklı Mimari (SOA)** temel teknoloji olarak Web Hizmetlerini kullanır

### OGSA'nın Üzerine İnşa Edildiği Standartlar: 
- **SOAP, WSDL, UDDI**:  Programdan programa etkileşim
- **XML**:  Veri paylaşımı
- **WS-Addressing**: Mesajlaşma
- **WS-ReliableMessaging**: Güvenilir mesajlaşma
- **WS-RF**: Kaynak yönetimi
- **WS-Security, WS-Trust**: Güvenlik
- **BPEL4WS**: İş süreci akışı
- **WS-Notification**: Olay tetikleme

## 2.6 Grid Mimarisi Katmanları

| Katman | Görev |
|--------|-------|
| **1. Fabric (Donanım)** | Fiziksel kaynaklar (hesaplama, depolama, ağlar, sensörler) |
| **2. Connectivity (Bağlantı)** | İletişim ve kimlik doğrulama protokolleri |
| **3. Resource (Kaynak)** | Bireysel kaynakların paylaşımı için güvenlik |
| **4. Collective (Kolektif)** | Kaynak koleksiyonları ile etkileşim, küresel yönetim |
| **5. Application (Uygulama)** | Grid üzerindeki kullanıcı uygulamaları |

## 2.7 Şebekelerin Sınıflandırılması

### A) Kaynak Odağına Göre: 
- **Hesaplama Şebekeleri**: CPU paylaşımı
- **Veri Şebekeleri**: Büyük ölçekli veri yönetimi
- **Uygulama Şebekeleri**: Uzak yazılımlara erişim
- **Servis Şebekeleri**:  Hizmet paylaşımı

### B) Kaynak Paylaşımı Kapsamına Göre:
- **Küme Şebekeleri (Cluster)**: Yerel ağla bağlı bilgisayarlar
- **Kurumsal Şebekeler (Enterprise)**: Şirket içi kaynak paylaşımı
- **Yardımcı Şebeke Hizmetleri (Utility)**: Üçüncü taraf sağlayıcı
- **İş Ortağı/Topluluk Şebekeleri**: Kurumlar arası işbirliği (Sanal Organizasyon - VO)