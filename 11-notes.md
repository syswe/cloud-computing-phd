# 11. Bulut Bilişim Referans Mimarisi - Ders Notları

## 11.1 NIST Referans Mimarisi

**Amaç:** Bulut bilişim sistemlerinin standart, karşılaştırılabilir ve analiz edilebilir çerçevede ele alınması. 

**Önemli Nokta:** Bulut bilişim sadece teknoloji yığını değil, **çok paydaşlı bir hizmet ekosistemidir**.

## 11.2 Beş Temel Aktör

### 1. Bulut Tüketicisi (Cloud Consumer)

**Tanım:** Bulut hizmetlerini kullanan nihai kişi veya kuruluş

**Görevleri:**
- Hizmet kataloğunu inceleme
- Hizmet talebinde bulunma
- SLA koşullarını kabul etme
- Kullanım miktarına göre ücretlendirme

### 2. Bulut Sağlayıcısı (Cloud Provider)

**Tanım:** Altyapıyı kuran, işleten ve hizmet olarak sunan taraf

**Sorumlulukları:**
- Fiziksel ve sanal kaynakları yönetme
- Hizmet sürekliliğinden sorumlu olma
- Güvenlik ve gizlilik mekanizmalarını uygulama

**Not:** Sorumluluk düzeyi hizmet modeline (SaaS, PaaS, IaaS) göre değişir.

### 3. Bulut Denetçisi (Cloud Auditor)

**Tanım:** Bulut hizmetlerinin bağımsız değerlendirmesini yapan taraf

**Değerlendirme Alanları:**
- Güvenlik
- Performans
- Gizlilik
- Mevzuat uyumluluğu

**Önemi:** Kamu kurumları ve regülasyona tabi sektörler için zorunlu

### 4. Bulut Aracısı (Cloud Broker)

**Tanım:** Tüketici ile sağlayıcı arasındaki karmaşıklığı yöneten aktör

**Üç Temel Hizmet Türü:**

| Hizmet | Açıklama |
|--------|----------|
| **Hizmet Aracılığı** | Service Intermediation |
| **Hizmet Toplama** | Service Aggregation |
| **Hizmet Arbitrajı** | Service Arbitrage |

### 5. Bulut Taşıyıcısı (Cloud Carrier)

**Tanım:** Bulut hizmetlerinin ağ üzerinden taşınmasından sorumlu

**İçerik:** Geleneksel telekomünikasyon altyapıları

## 11.3 Hizmet Modelleri ve Kontrol Kapsamı

### SaaS (Software as a Service)
- Tüketici yalnızca uygulamayı kullanır
- Altyapı ve platform sağlayıcı kontrolünde

### PaaS (Platform as a Service)
- Tüketici uygulama geliştirir ve yönetir
- Altyapı kontrolü sağlayıcıda

### IaaS (Infrastructure as a Service)
- Tüketici sanal makineler ve OS'i yönetir
- Fiziksel altyapı sağlayıcıya ait

**Kural:** Hizmet modeli derinleştikçe: 
- Tüketicinin kontrolü **artar**
- Güvenlik sorumluluğu da **artar**

## 11.4 Bulut Dağıtım Modelleri

### Genel Bulut
- Çok kiracılı yapı
- Yüksek ölçeklenebilirlik
- Daha yüksek güvenlik riskleri

### Özel Bulut
- Tek kuruluşa tahsisli
- Yüksek kontrol ve güvenlik

### Topluluk Bulutu
- Ortak amaçlara sahip kurumlar
- Paylaşılan maliyet ve yönetişim

### Hibrit Bulut
- Birden fazla bulutun entegrasyonu
- **Taşınabilirlik ve birlikte çalışabilirlik kritik**

## 11.5 Mimari Bileşenler - Üç Katmanlı Yapı

| Katman | İçerik |
|--------|--------|
| **1. Hizmet Katmanı** | SaaS, PaaS, IaaS |
| **2. Kaynak Soyutlama ve Kontrol** | Sanallaştırma, yönetim |
| **3. Fiziksel Kaynak Katmanı** | Donanım, veri merkezleri |

## 11.6 Bulut Hizmeti Yönetimi

### İş Desteği
- Müşteri yönetimi
- Sözleşme ve SLA yönetimi
- Faturalandırma

### Sağlama ve Yapılandırma
- Hızlı kaynak tahsisi
- İzleme ve ölçüm
- SLA uygulaması

### Taşınabilirlik ve Birlikte Çalışabilirlik
- **Vendor lock-in** (sağlayıcı bağımlılığı) riski
- Taşınabilirlik eksikliği temel neden

## 11.7 Güvenlik ve Gizlilik

**Güvenlik Özellikleri:**
- Paylaşılan sorumluluk
- Hizmet ve dağıtım modeline göre değişir
- Kimlik yönetimi, veri bütünlüğü, denetim

### PII (Personally Identifiable Information)

**Tanım:** Belirli bir bireyi tanımlamak için kullanılabilecek bilgi

**Örnekler:**
- İsimler, Adresler
- Telefon Numaraları
- E-posta Adresleri
- Sosyal Güvenlik Numaraları
- Pasaport Numaraları
- Doğum Tarihi