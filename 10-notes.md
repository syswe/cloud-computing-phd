# 10. Bulut Bilişimin NIST Tanımı - Ders Notları

## 10.1 NIST Tanımı

**NIST (National Institute of Standards and Technology)** tanımı: 

> "Paylaşılan, yapılandırılabilir bilgi işlem kaynakları havuzuna (ağlar, sunucular, depolama, uygulamalar, hizmetler) her yerden, hızlı, isteğe bağlı ve minimum yönetim çabasıyla erişim sağlayan bir model."

## 10.2 Bulut Bilişim Modeli Bileşenleri

1. **Beş Temel Özellik**
2. **Üç Hizmet Modeli**
3. **Dört Dağıtım Modeli**

## 10.3 Beş Temel Özellik (Essential Characteristics)

### Seçenek Türleri: 
- **Seçenek A (Nesnel)**: Standart, ölçülebilir, karşılaştırılabilir
- **Seçenek B (Öznel)**: CSC ihtiyacına bağlı, öznel kriterler

### 1. İsteğe Bağlı Self-Servis (On-Demand Self-Service)

**Tanım:** İnsan etkileşimi olmadan kaynakları otomatik olarak talep edebilme

| Seçenek | Açıklama |
|---------|----------|
| A | Tam otomatik provizyon |
| B | Ön yüz otomatik, arka uç kısmen manuel |

**Önemi:** Bulut bilişimi geleneksel hosting'den ayıran en kritik parametre

### 2. Geniş Ağ Erişimi (Broad Network Access)

**Tanım:** Standart protokollerle (HTTP/HTTPS, REST, TCP/IP) farklı istemcilerden erişim

| Seçenek | Açıklama |
|---------|----------|
| A | İnternet üzerinden erişim |
| B | Kuruma özel ağ üzerinden erişim |

### 3. Kaynak Havuzu (Resource Pooling)

**Tanım:** Çok kiracılı (multi-tenant) model ile dinamik kaynak paylaşımı

**Kriter:** En az 2 CSC tarafından paylaşılabilir altyapı

**Önemi:** Bulut ekonomisinin merkezi

### 4. Hızlı Esneklik (Rapid Elasticity)

**Tanım:** Talebe göre otomatik büyüme/küçülme

| Seçenek | Açıklama |
|---------|----------|
| A | Gerçek zamanlı otomatik ölçekleme |
| B | CSC ihtiyacını karşılayacak hızda |

### 5. Ölçülen Hizmet (Measured Service)

**Tanım:** Kaynak kullanımının otomatik ölçümü, izlenmesi, raporlanması

**Önemi:** Kullanım bazlı ücretlendirme (pay-as-you-go) temelini oluşturur

## 10.4 Hizmet Modelleri

### 1. SaaS (Software as a Service)

**Kullanıcı:** Son kullanıcılar  
**Kontrol:** En düşük  
**Özellik:** Yazılım web/mobil üzerinden kullanılır  
**Örnek:** Google Workspace

### 2. PaaS (Platform as a Service)

**Kullanıcı:** Geliştiriciler, uygulama dağıtıcıları  
**Kontrol:** Orta  
**Özellik:** Uygulama geliştirme ve yayınlama platformu  
**Örnek:** Heroku, Azure App Service

### 3. IaaS (Infrastructure as a Service)

**Kullanıcı:** BT operasyonlar��  
**Kontrol:** En yüksek  
**Özellik:** Temel işlem, depolama, ağ kaynakları  
**Örnek:** AWS EC2, GCP Compute Engine

### Karşılaştırma: 

| Özellik | SaaS | PaaS | IaaS |
|---------|------|------|------|
| **Kullanıcı** | Son kullanıcı | Geliştirici | BT operasyonları |
| **Kontrol** | En düşük | Orta | En yüksek |
| **Avantaj** | Bakım yok | Hızlı geliştirme | Esneklik |
| **Risk** | Esneklik sınırlı | Vendor lock-in | Yönetim karmaşıklığı |

## 10.5 Dağıtım Modelleri

### 1. Özel Bulut (Private Cloud)
- Tek kuruluşa tahsisli
- En yüksek kontrol ve güvenlik
- Yüksek maliyet

### 2. Topluluk Bulutu (Community Cloud)
- Benzer ihtiyaçlara sahip kurumlar
- Paylaşılan maliyet ve yönetişim
- Koordinasyon zor olabilir

### 3. Genel Bulut (Public Cloud)
- Geniş kitlelere açık
- Düşük maliyet, yüksek esneklik
- Veri konumu sınırlı kontrol
- **Örnekler:** AWS, Azure, GCP

### 4. Hibrit Bulut (Hybrid Cloud)
- Birden fazla bulutun entegrasyonu
- Esneklik, optimum maliyet
- Yönetim karmaşık

### Karşılaştırma Tablosu:

| Model | Sahiplik | Avantaj | Dezavantaj |
|-------|----------|---------|------------|
| **Özel** | Kurum/üçüncü taraf | Güvenlik, kontrol | Yüksek maliyet |
| **Topluluk** | Kurumlar/üçüncü taraf | Maliyet avantajı | Koordinasyon zor |
| **Genel** | CSP | Düşük maliyet | Sınırlı kontrol |
| **Hibrit** | Paylaşımlı | Esneklik | Yönetim karmaşık |