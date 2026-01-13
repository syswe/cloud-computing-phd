# 1. Grid Computing (Şebeke Hesaplama) - Ders Notları

## 1.1 Grid Computing Tanımı

**Grid Computing**, tek bir makine için oldukça zor olan bir görevi gerçekleştirmek için **birlikte çalışan bir bilgisayar ağıdır**. Bu ağdaki tüm makineler, **sanal bir süper bilgisayar** gibi davranmak için aynı protokol altında çalışır.

### Temel Özellikler:
- Büyük veri kümelerini analiz etme
- Yüksek bilgi işlem gücü gerektiren simülasyonlar
- İşlem gücü ve depolama kapasitesi paylaşımı

## 1.2 Çalışma Prensibi

Grid Computing ağı **üç tip makineden** oluşur:

| Makine Türü | Görevi |
|-------------|--------|
| **Kontrol Düğümü** | Tüm ağı yöneten sunucu, kaynak havuzunun hesabını tutar |
| **Sağlayıcı** | Ağ kaynak havuzuna kaynak katkısında bulunan bilgisayar |
| **Kullanıcı** | Ağdaki kaynakları kullanan bilgisayar |

### Ağ Türleri:
- **Homojen Ağlar**: Aynı işletim sistemini kullanan benzer platformlara sahip makineler
- **Heterojen Ağlar**: Farklı işletim sistemi üzerinde çalışan farklı platformlara sahip makineler

## 1.3 Ara Yazılım (Middleware)

**Ara yazılım görevleri:**
- Ağ üzerinde yürütülen işlemleri yetkilendirme
- Güvenlik tehditlerini önleme
- İstenmeyen görevlerin engellenmesi

## 1.4 Grid Computing Avantajları

1. **Merkezsizlik**: Kontrol düğümü dışında sunucu gerektirmez
2. **Heterojen Destek**: Farklı işletim sistemlerine sahip makineler tek ağda çalışabilir
3. **Paralel İşlem**: Görevler farklı fiziksel konumlarda eş zamanlı gerçekleştirilebilir

## 1.5 Grid Mimarisi - Katmanlar

| Katman | İçerik |
|--------|--------|
| **1. Uygulama Katmanı** | Grid uygulamaları ve API'ler |
| **2. Ara Katman Yazılımı** | Globus Toolkit, gLite gibi yazılımlar |
| **3. Kaynak Katmanı** | Depolama, işleme yetenekleri |
| **4. Ağ Katmanı** | Yönlendiriciler, anahtarlar, protokoller |

## 1.6 Güvenlik Kavramları

### Üç Temel Güvenlik Özelliği: 

1. **Tek Oturum Açma (Single Sign-On)**:  Bir kez oturum açarak belirli süre boyunca erişim
2. **Kimlik Doğrulama (Authentication)**: Kimliği kanıtlama (kullanıcı adı/şifre)
3. **Yetkilendirme (Authorization)**: Kullanıcıya atanan ayrıcalıkların kontrolü

## 1.7 Kaynak Yönetimi

- İşin uzaktan gönderilmesi
- Durumun kontrol edilmesi
- Çıktının alınması
- **Grid Zamanlayıcı** ile kaynak tahsisi

## 1.8 Service Level Agreement (SLA)

SLA, kullanıcının beklediği: 
- Minimum hizmet kalitesi
- Kullanılabilirlik
- Hizmet ücretleri
- Minimum çalışma süresi

## 1.9 Veri Yönetimi

- Güvenli veri erişimi
- Veri kopyalama ve taşıma
- Meta veri yönetimi
- **Veri bilinçli çizelgeleme**:  Zamanlama kararlarının verinin konumunu dikkate alması

## 1.10 Bellek İçi Veri Izgaraları (IMDG)

- Veriler bellekte saklanır
- Çok hızlı veri erişimi
- Daha yüksek verim
- Daha düşük gecikme süresi