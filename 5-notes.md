# 5. Veri Yönetimi (Data Management) - Ders Notları

## 5.1 Veri Yönetimi Tanımı

**Veri Yönetimi**:  Uzak siteler arasında dağıtılmış verilerin erişimini, senkronizasyonunu ve koordinasyonunu destekleyen dağıtılmış sistem. 

### İki Yaklaşım:

| Yaklaşım | Odak |
|----------|------|
| **Hesaplama Odaklı** | Veri yönetimi daha az önemli, küçük dosyalar |
| **Veri Odaklı** | Büyük miktarda dağıtılmış veri işleme |

### Örnek Proje: 
**DataGrid** - CERN'in Büyük Hadron Çarpıştırıcısı (LHC) verilerini işlemek için geliştirildi.

## 5.2 Veri Izgarası vs DDBMS

| Özellik | Veri Izgarası | DDBMS |
|---------|---------------|-------|
| **Heterojenlik** | Tamamen heterojen | Homojen |
| **Veri Kontrolü** | Kısmi kontrol | Tam kontrol |
| **Ölçeklenebilirlik** | Çok büyük veri kaynakları | Sınırlı |

## 5.3 Statik ve Dinamik Veri

### Statik Veri: 
- Oluşturulduktan sonra **değiştirilmez**
- Sadece okunur veya analiz edilir
- Örnek: DNA bilgileri

### Dinamik Veri: 
- **Güncellemeler ve değişiklikler** içerir
- E-iş uygulamaları
- Senkronizasyon sorunu önemli

## 5.4 Veri Yönetiminin İşlevleri

### 1. Veri Çoğaltma Yönetimi (RMS)

**Veri Çoğaltma**:  Veri erişimini optimize etmek için kopyaların oluşturulması. 

**RMS Sorumlulukları:**
- Çoğaltma oluşturma
- Replika dosyalarını yönetme
- Kopyaları kaydetme ve kataloglama
- En uygun kopyayı seçme
- Tutarlılığı sağlama

### 2. Meta Veri Yönetimi

**Meta Veri**:  Verilerle ilgili tanımlayıcı bilgi.

**Meta Veri Kategorileri:**
- **Sistem Bilgileri**: İnternet hizmet durumu, depolama kapasitesi
- **Çoğaltma Bilgisi**: Mantıksal-fiziksel kopya eşleştirmesi
- **Uygulama Bilgileri**:  Veri içeriği, yapısı

### 3. Yayın ve Keşif

- **Veri Yayınlama**: Meta veri bilgilerini erişilebilir kılma
- **Veri Keşfi**: İstenen veriyi bulma

### 4. Veri Senkronizasyonu - Tutarlılık Düzeyleri

| Düzey | Ad | Açıklama |
|-------|-----|----------|
| **-1** | Muhtemel Tutarsız | Kopya orijinalle eşleşmez |
| **0** | Tutarlı Dosya Kopyası | Anlık görüntüyle eşleşebilir |
| **1** | Tutarlı İşlem Kopyası | Tek dosyada tutarlılık |
| **2** | Tutarlı İşlem Kopyaları Seti | Site içi çoklu kopya tutarlılığı |
| **3** | Tutarlı Güncel İşlem Kopyaları | En katı - tüm kopyalar aynı |

### 5. Kimlik Doğrulama, Erişim Kontrolü ve Hesap Oluşturma

- **GSI (Grid Security Infrastructure)** tabanlı çözümler
- Çok parçalı erişim kontrol mekanizması
- Muhasebe mekanizması ile kullanım geçmişi kaydı

### 6. Veri Entegrasyonu

**Adımlar:**
1. Veri Keşfi
2. Veri Erişimi
3. Veri Aktarımı
4. Veri Analizi
5. Veri Sentezi

## 5.5 Meta Veri Hizmeti

### Meta Veri Türleri: 

| Tür | Açıklama |
|-----|----------|
| **Fiziksel** | Boyut, konum, oluşturma zamanı, dosya türü |
| **Çoğaltma** | Mantıksal-fiziksel bağlantı |
| **Etki Alanı** | Alana özgü nitelikler |
| **Kullanıcı** | Ad, e-posta, kuruluş |
| **Uygulama** | İçerik, ortam bilgisi |
| **Kaynak** | Erişim adresi, fiziksel konum, ACL |

### Meta Veri Depolama: 
- **İlişkisel Veritabanı**:  SQL ile kolay erişim
- **XML Dosyası**: Platform bağımsız, genişletilebilir

## 5.6 Çoğaltma (Replication)

### Temel Bileşenler:

| Bileşen | Görev |
|---------|-------|
| **GUID** | Küresel Benzersiz Tanımlayıcı |
| **Replika Kataloğu** | Kopyaları kaydetme ve sorgulama |
| **Replika Yönetimi** | Kopya oluşturma ve silme |
| **Replika Seçimi** | En uygun kopyayı seçme |
| **LRC** | Yerel Konum Replika Kataloğu |
| **RLI** | Replika Konum İndeksi |