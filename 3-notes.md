# 3. OGSA ve WSRF - Ders Notları

## 3.1 Grid Hesaplama ve Standartlaşma İhtiyacı

**Sorun**: Grid sistemlerinin ilk versiyonları (Globus Toolkit 2) farklı protokollerle geliştirildiği için heterojen yapıdaydı.

**Çözüm**: 
- **Global Grid Forum (GGF)** kuruldu
- IBM ve Microsoft destekli **Web Servisleri** ortaya çıktı
- **OGSA** (Açık Şebeke Hizmetleri Mimarisi) önerildi

## 3.2 Web Servisleri

### Tanım: 
Bir iç ağ veya internet üzerinden tanımlanabilen, yayınlanabilen, keşfedilebilen ve çağrılabilen, **platformdan ve programlama dilinden bağımsız** sunucu taraflı bileşen.

### Web Servisi Özellikleri: 

| Özellik | Açıklama |
|---------|----------|
| **Gevşek Bağlı** | Arayüz değişmediği sürece uygulama değiştirilebilir |
| **Kapsüllenmiş** | İç uygulama istemciden gizlenir |
| **Platformdan Bağımsız** | Herhangi bir dilde yazılıp çalıştırılabilir |
| **Oluşturulabilir** | Farklı hizmetlerden yeni hizmetler oluşturulabilir |
| **Tanımlı** | XML tabanlı arayüzle açıklanır |

## 3.3 Web Servisleri Temel Standartları

### 1. SOAP (Simple Object Access Protocol)
- HTTP üzerinden XML formatında mesaj alışverişi
- Hafif bir iletişim protokolü

**SOAP Mesaj Yapısı:**
- **Zarf (Envelope)**: Ana kapsayıcı
- **Başlık (Header)**: İsteğe bağlı meta bilgiler
- **Gövde (Body)**: Asıl mesaj yükü

### 2. WSDL (Web Services Description Language)
- Web servisinin ne yaptığını, nerede bulunduğunu tanımlar
- XML tabanlı

**WSDL Bölümleri:**
- **Messages**: Mesaj tanımları
- **PortType**: Operasyonlar
- **Binding**: Protokol bilgileri
- **Port**: Ağ adresi

### 3. UDDI (Universal Description, Discovery and Integration)

| Bölüm | İçerik |
|-------|--------|
| **Beyaz Sayfalar** | Sağlayıcı hakkında genel bilgiler |
| **Sarı Sayfalar** | Endüstriyel kategori sınıflandırması |
| **Yeşil Sayfalar** | Teknik bilgiler (WSDL belgesi) |

## 3.4 OGSA (Open Grid Services Architecture)

### OGSA'nın Web Servislerini Genişletme Alanları:

1. **Dinamik Yaşam Döngüsü**:  Hizmetler anlık olarak oluşturulabilir, kullanılabilir ve yok edilebilir
2. **Durum Bilgisi**: Grid hizmetleri kendileriyle ilişkili verileri (durumları) tutabilir
3. **Bildirim**:  İstemciler değişikliklere abone olabilir

### OGSA Uygulamaları: 
- **OGSI**:  "Grid Servisi" kavramının teknik şartnamesi
- **Globus Toolkit 3 (GT3)**: OGSI tabanlı araç seti
- **OGSA-DAI**: Veritabanı erişim ara katmanı

## 3.5 WSRF (Web Services Resource Framework)

### Amaç:
"Durum bilgisi olan kaynakları" Web Servisleri bağlamında modellemek ve yönetmek.

### WS-Resource Kavramı:
- Durum bilgisi olmayan Web Servisi + Durum bilgisi olan kaynak
- Dinamik olarak oluşturulabilir, tanımlanabilir, yok edilebilir
- **WS-Addressing** uç nokta referansları ile erişim

### WSRF Spesifikasyonları:

| Spesifikasyon | Görev |
|---------------|-------|
| **WS-ResourceLifetime** | WS-Resource'ların nasıl yok edileceğini tanımlar |
| **WS-ResourceProperties** | Durum bilgilerinin tanımlanması |
| **WS-Notification** | Olay aboneliği ve bildirim mekanizmaları |
| **WS-BaseFaults** | Hata mesajlarını standartlaştırır |
| **WS-ServiceGroup** | Servislerin gruplanması |

## 3.6 WSRF ve OGSA İlişkisi

- **OGSA**: Mimari (ne yapılacağını tanımlar)
- **WSRF**: Teknoloji (nasıl yapılacağını sağlar)
- WSRF, OGSA'yı etkinleştiren temel teknolojilerden biridir