# 13. Şebeke Hesaplama ve Bulut Bilişim Karşılaştırması - Ders Notları

## 13.1 Şebeke Hesaplama Tanımı

**Tanım:** Farklı BT kaynaklarını koordine ederek bir bütün olarak çalışmasına izin veren bir **ara katman yazılımıdır**.

### Kullanım Alanları:
- Bilimsel araştırmalar
- Üniversitelerde eğitim amaçlı

### Örnek Senaryo: 
Mimar öğrencilerin tasarım aracını kampüs ağında paylaşması

## 13.2 Grid vs Cloud Temel Farklar

| Özellik | Şebeke (Grid) | Bulut (Cloud) |
|---------|---------------|---------------|
| **Amaç** | Ortak hedefi gerçekleştirmek için mevcut kaynakları kullanır | Hizmet sağlayıcı olarak çalışır |
| **Model** | **Merkezi olmayan** | **Merkezi** |
| **Sahiplik** | Birden çok tarafa ait | Genellikle tek tarafa ait |
| **Hizmetler** | Sınırlı hizmetler | Tüm hizmetlerin çoğunda daha fazla hizmet |
| **Kaynak Birleştirme** | Farklı organizasyonlardaki kaynaklar | Tek kuruluş içinde (ör:  Amazon) |

## 13.3 Grid ve Bulut Bilişim Benzerlikleri

1. **Bilgi işlem maliyetini azaltmak**
2. **Güvenilirliği artırmak**
3. **Esnekliği artırmak** - Bilgisayarları üçüncü şahıslar tarafından işletilen bir şeye dönüştürme

## 13.4 Detaylı Karşılaştırma Tablosu

| Özellik | Şebeke Hesaplama | Bulut Bilişim |
|---------|------------------|---------------|
| **Kullanım Yöntemleri** | Birden çok sunucunun tek göreve tahsisi | Sunucuların sanallaştırılması; bir sunucu birçok görev |
| **Tipik Kullanım** | İş yürütme (sınırlı süre) | Uzun süreli hizmetler |
| **Soyutlama Düzeyi** | Yüksek düzeyde ayrıntı | Üst düzey soyutlamalar |
| **Hesaplama Hizmeti** | Maksimum hesaplama | Talep üzerine (isteğe bağlı) |
| **Erişilebilirlik** | Güvenilir, tutarlı, yaygın, ucuz erişim | Özelleştirilmiş, ölçeklenebilir, QoS garantili |
| **Altyapı** | Merkezi olmayan, heterojen kaynaklar | Merkezi, homojen kaynaklar |
| **Sanallaştırma** | Veri ve bilgi işlem kaynaklarının sanallaştırılması | Donanım ve yazılım platformlarının sanallaştırılması |
| **Kullanıcı Yönetimi** | **Merkeziyetsiz Yönetim** | **Merkezileştirilmiş Yönetim** |
| **Ölçeklenebilirlik** | Normal | Yüksek |
| **Mimari** | **Dağıtılmış bilgi işlem mimarisi** | **İstemci-sunucu mimarisi** |
| **Bağımlılık** | Bilgisayar durduğunda diğer bilgisayar işi alır | Tamamen internete bağlı |
| **İşlem (Operasyon)** | Kurumsal ağ içinde çalışır | İnternet üzerinden de çalışabilir |

## 13.5 Şebeke Hesaplama Özellikleri

### Mimari: 
- **Dağıtılmış bilgi işlem mimarisi**
- Kaynaklar **işbirlikçi modelde** kullanılır
- Kullanıcılar kullanım için **ödeme yapmazlar**

### Avantajlar:
- Merkezi kontrol noktası yok
- Hata toleransı (bir bilgisayar durduğunda diğeri işi alır)
- Kurumsal ağ içinde çalışır

## 13.6 Bulut Bilişim Özellikleri

### Mimari:
- **İstemci-sunucu bilişim mimarisi**
- Kaynaklar **merkezi düzende** kullanılır
- **Yüksek erişilebilir** hizmet

### İş Modeli:
- **Öde ve kullan** (Pay-as-you-go)
- Kullanıcılar kullanım için öderler

### Avantajlar: 
- Yüksek ölçeklenebilirlik
- QoS garantisi
- Geniş hizmet yelpazesi (web barındırma, DB desteği vb.)

## 13.7 Özet Karşılaştırma

| Kriter | Grid | Cloud |
|--------|------|-------|
| **Yönetim** | Merkeziyetsiz | Merkezi |
| **Ödeme** | Ücretsiz (paylaşım) | Kullanım başına ödeme |
| **Mimari** | Dağıtılmış | İstemci-sunucu |
| **Odak** | Hesaplama gücü | Hizmet sunumu |
| **Ölçeklenebilirlik** | Normal | Yüksek |
| **Kaynak Sahipliği** | Çoklu organizasyon | Tek organizasyon |