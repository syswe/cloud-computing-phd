# 7. Grid Çizelgeleme ve Kaynak Yönetimi - Ders Notları

## 7.1 Çizelgeleme Paradigmaları

### 1. Merkezi Zamanlama

**Özellikler:**
- Tek merkezi makine tüm düğümler için işleri zamanlar
- Benzer özelliklere sahip kaynaklar için uygun
- Bilgi işlem merkezi ortamları için ideal

**Avantaj:**
- Güncel ve eksiksiz kaynak bilgisine sahip
- Daha iyi zamanlama kararları

**Dezavantaj:**
- Büyük ortamlarda **ölçeklenmez**
- **Tek arıza noktası** riski
- Darboğaz oluşabilir

### 2.  Dağıtılmış Zamanlama

**Özellikler:**
- Merkezi zamanlayıcı **yok**
- Birden çok yerelleştirilmiş zamanlayıcı birbiriyle etkileşir

**İletişim Türleri:**

| Tür | Açıklama |
|-----|----------|
| **Doğrudan İletişim** | Zamanlayıcılar birbirleriyle doğrudan iletişim kurar |
| **Merkezi İş Havuzu** | İşler merkezi havuza gönderilir, zamanlayıcılar seçer |

**Avantaj:**
- Ölçeklenebilirlik sorunlarını çözer
- Daha iyi hata toleransı ve güvenilirlik

**Dezavantaj:**
- Global zamanlayıcı olmaması → **optimal olmayan kararlar**

### 3. Hiyerarşik Zamanlama

**Özellikler:**
- Merkezi zamanlayıcı (meta zamanlayıcı) + yerel zamanlayıcılar
- Meta zamanlayıcı işleri yerel zamanlayıcılara gönderir

**Avantaj:**
- Genel ve yerel zamanlayıcı **farklı ilkelere** sahip olabilir

**Dezavantaj:**
- Ölçeklenebilirlik ve iletişim darboğazları olabilir

## 7.2 Kaynak Seçimi

**Amaç:** Kullanıcı kısıtlamalarına en uygun kaynakları seçmek

**İlişki:** R_selected ⊆ R_available

### Kaynak Seçim Algoritması Örneği (CPU ve RAM):

```
Değerlendirme = W_CPU × [(1 - CPU_load) × (CPU_speed / CPU_min)] 
              + W_RAM × [(1 - RAM_usage) × (RAM_size / RAM_min)]
```

**Parametreler:**
- W_CPU: CPU hızına ayrılan ağırlık
- W_RAM: RAM'e ayrılan ağırlık
- CPU_load:  Mevcut CPU yükü
- RAM_usage: Mevcut RAM kullanımı

## 7.3 İş Seçim Stratejileri

| Strateji | Açıklama | Dezavantaj |
|----------|----------|------------|
| **İlk Gelen İlk Hizmeti Alır (FCFS)** | Gönderim sırasına göre | Kaynak israfı, uzun bekleme |
| **Rastgele Seçim** | Rastgele iş seçimi | Adil değil, eski işler gecikebilir |
| **Önceliğe Dayalı Seçim** | En yüksek öncelikli iş önce | Optimal öncelik kriteri belirleme zor |

## 7.4 Platform Globus Toolkit 3. 0 (PGT3)

**Tanım:** Globus Toolkit 3.0'ın ticari dağıtımı

### Temel Özellikler: 
- **CSF (Community Scheduler Framework)** üzerine kurulu
- Meta zamanlayıcıları uygulamak için bileşenler sağlar

### Desteklenen Kaynak Yönetim Sistemleri: 
- **SGE** (Sun Grid Engine)
- **Condor**
- **LSF** (Load Sharing Facility)
- **PBS** (Portable Batch System)

### CSF Plus: 
- Temel bileşen
- Meta zamanlayıcı altyapısı sağlar
- Son kullanıcıların kaynak yönetim sistemleriyle etkileşimini sağlar

**Örnek:** LSF istemcisi → SGE tarafından yönetilen kümeye iş gönderebilir