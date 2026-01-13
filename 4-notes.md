# 4. Bilgi Hizmetleri (Information Services) - Ders Notları

## 4.1 MDS (Monitoring and Discovery Services)

**Bilgi Hizmetleri** = **İzleme ve Keşif Hizmetleri (MDS)**

### Temel Amaç:
- Hesaplama Şebekesi tarafından sağlanan yetenekler hakkında genel bakış
- Kaynak keşfi, seçimi ve optimizasyonu için bilgi sağlama

### MDS Kategorileri: 
1. **WS Öncesi Bilgi Hizmetleri (MDS2)**
2. **WS Bilgi Hizmetleri (MDS3)**

## 4.2 MDS3 - WS Bilgi Hizmetleri

### Şebeke Hizmetleri Türleri: 
- **Kalıcı (Persistent)**: Oluşturan süreçten uzun ömürlü
- **Geçici (Transient)**: Kısa ömürlü

### Bilgi Modeli - OGSA Mekanizmaları:

| Mekanizma | Açıklama |
|-----------|----------|
| **Factories** | Hizmet örnekleri oluşturan nesneler |
| **GSH (Grid Service Handle)** | Hizmet için benzersiz tanımlayıcı |
| **GSR (Grid Service Reference)** | GSH + bağlama bilgileri |
| **Registry Services** | GSH deposu |
| **Notification Services** | Asenkron mesaj gönderimi |

### Veri Toplama: 
- **Hizmet veri sağlayıcıları** aracılığıyla
- Dinamik veri üretimi
- Özel sağlayıcılar geliştirilebilir

### Sorgular:
- **SDE adıyla** veya **XPath/XQuery** kullanılarak
- **Eşzamanlı çekme modu (FindServiceData)**
- **Eşzamansız yanıt modu (bildirim aboneliği)**

### Kullanıcı Arayüzleri:
1. **Servis Tarayıcı GUI'si**
2. **Komut Satırı Araçları** (ogsi-find-service-data-by-name, ogsi-find-service-data-xpath)

### Güvenlik:
- **Grid Security Infrastructure (GSI)** ile uyumlu
- X. 509 ve proxy sertifikaları
- SSL/TLS üzerinde çalışır
- Karşılıklı kimlik doğrulama, delegasyon, yetkilendirme

### MDS3 Veri Sağlayıcıları:

| Sağlayıcı | Görev |
|-----------|-------|
| **SimpleSystemInformationProvider** | CPU, bellek, işletim sistemi, disk bilgisi |
| **HostScriptProvider** | Unix kabuk komut dosyaları |
| **ScriptExecutionProvider** | Kabuk komut dosyası yürütme |
| **AsyncDocumentProvider** | XML'i periyodik okuma |

## 4.3 MDS2 - WS Öncesi Bilgi Hizmetleri

- Globus Toolkit Sürüm 2 ve öncesi
- Geriye dönük uyumluluk için korunmaktadır
- Temel arayüz olarak **LDAP** kullanır

### MDS2 Bileşenleri:

| Bileşen | Görev |
|---------|-------|
| **GRIS (Grid Resource Information Service)** | Belirli kaynaktaki bilgileri sorgulama |
| **GIIS (Grid Index Information Service)** | Farklı GRIS'lerden bilgi birleştirme |

### MDS'nin Faydaları: 
- Statik ve dinamik bilgilere erişim
- Tek tip ve esnek erişim
- Birden fazla bilgi kaynağına erişim
- Merkezi olmayan bakım

## 4.4 Grid Monitor

### Temel Bileşenler: 
1. **Küme (Cluster)**: Küme durumu hakkında bilgi
2. **Yük (Load)**: Grid ve yerel işlemlerin grafiksel gösterimi
3. **Kuyruklama (Queuing)**: Kuyruktaki iş sayısı
4. **Arama (Search)**: Özel arama arayüzü
5. **Depolama Kaynakları**: Kullanılabilir depolama listesi