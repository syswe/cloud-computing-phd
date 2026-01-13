# 12. Bulut Bilişim Uygulama Alanları ve Ölçeklenebilirlik - Ders Notları

## 12.1 Bulut Bilişim Tanımı (Tekrar)

**Tanım:** Bilgi işlem kaynaklarının internet üzerinden **isteğe bağlı**, **ölçeklenebilir** ve **kullandıkça öde** modeliyle sunulması. 

### Temel Özellikler: 
- Kaynak soyutlama (resource abstraction)
- Dinamik kaynak tahsisi
- Çok kullanıcılı (multi-tenant) mimari
- Otomatik ölçekleme

### Önemli Nokta:
**CAPEX → OPEX dönüşümü** (Sermaye harcaması → İşletme gideri)

## 12.2 Günlük Hayatta Bulut Bilişim Örnekleri

| Kategori | Örnekler |
|----------|----------|
| **E-posta** | Gmail, Outlook |
| **Sosyal Medya** | Facebook, Instagram |
| **Video Akışı** | YouTube, Netflix |
| **Ofis Uygulamaları** | Google Docs |
| **Fotoğraf Depolama** | Google Photos, Flickr |

**Ortak Nokta:** Verinin yerel cihazda değil, uzaktaki bulut veri merkezlerinde tutulması

## 12.3 Önde Gelen Bulut Sağlayıcıları

### Amazon Web Services (AWS)
- İlk büyük ölçekli bulut sağlayıcı
- IaaS, PaaS ve SaaS birleşimi
- EC2, S3, RDS servisleri

### Microsoft Azure
- Microsoft ekosistemiyle güçlü entegrasyon
- **Hibrit bulut çözümlerinde lider**
- Kurumsal uygulamalarda yaygın

### Google Cloud Platform (GCP)
- Büyük veri, AI ve ML odaklı
- **Kubernetes ve container teknolojilerinde öncü**

### Diğer Sağlayıcılar
- **Salesforce**:  CRM odaklı SaaS
- **Oracle Cloud**:  Veritabanı merkezli
- **IBM Cloud**: AI ve kurumsal çözümler

## 12.4 Bulut Mimarisi Bileşenleri

### Front-End (Ön Uç)
- Kullanıcının etkileşimde bulunduğu katman
- Web tarayıcıları, mobil uygulamalar, masaüstü istemciler
- **Örnek:** Gmail arayüzü, Google Docs editörü

### Back-End (Arka Uç)
- Bulut sağlayıcı tarafından yönetilen gizli katman
- Veri merkezleri, sanallaştırma altyapısı, yük dengeleyiciler
- Mikroservis mimarisi, Kubernetes, SDN

## 12.5 Bulut Bilişimin Çalışma Mantığı

1.  Kullanıcı → Ön uçtan istek gönderir
2. Kimlik doğrulama yapılır
3. İstek uygun servise yönlendirilir
4. Veri işlenir ve sonuç döndürülür

## 12.6 Uygulama Alanları

### İş Uygulamaları
- MailChimp, QuickBooks, Google Workspace

### Veri Depolama ve Yedekleme
- Google Drive, Dropbox, OneDrive

### Yönetim ve Organizasyon
- Trello, Accelo, Easynote

### Sosyal, Eğlence ve Eğitim
- **Sosyal:** Facebook, LinkedIn
- **Eğlence:** Netflix, Spotify
- **Eğitim:** Google Classroom, Blackboard

### Avantajlar: 
- Maliyet düşüşü
- Gerçek zamanlı işbirliği
- Ölçeklenebilir altyapı

## 12.7 Ölçeklenebilirlik (Scalability)

**Tanım:** Sistemin değişen iş yüküne göre kaynaklarını **dinamik biçimde artırıp azaltabilme** yeteneği

**Önemi:** Bulut bilişimin en kritik avantajı

### Ölçeklenebilirlik Türleri

| Tür | Açıklama | Özellik |
|-----|----------|---------|
| **Dikey (Vertical)** | Sunucu güçlendirme (↑CPU, ↑RAM) | Donanımsal sınır var |
| **Yatay (Horizontal)** | Sunucu ekleme | Dağıtık sistemler için ideal |
| **Çapraz (Diagonal)** | Vertical + Horizontal | Önce güç artır, sonra sunucu ekle |

### Ölçekleme Yöntemleri

| Yöntem | Açıklama |
|--------|----------|
| **Manuel** | Elle yapılan ölçekleme |
| **Planlı** | Önceden belirlenmiş zamanlarda |
| **Otomatik (Auto-scaling)** | CPU, istek sayısı, gecikme metriklerine göre |

## 12.8 Yedeklilik (Redundancy)

**Tanım:** Sistem bileşenlerinin ve verilerin birden fazla kopyasının tutulması

### Amaçlar:
- Veri kaybını önleme
- Süreklilik sağlama (High Availability)

### Faydaları:
- Otomatik veri yedekleme
- Her yerden erişim
- SLA ile garanti edilen çalışma süresi
- **Felaket kurtarma (Disaster Recovery)**