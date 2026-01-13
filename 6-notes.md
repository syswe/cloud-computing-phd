# 6. Grid Çizelgeleme ve Bilgi Hizmetleri - Ders Notları

## 6.1 Şebeke Çizelgeleme Temelleri

### Temel Sorular:
1. Kaynak, işin minimum QoS gereksinimlerini karşılıyor mu?
2. Kaynak, işe hizmet vermek için uygun mu? 

### Mimari: 
- **Hiyerarşik yapı**: Merkezi mimari yerine
- Tek hata noktası önlenir
- Ölçeklenebilirlik artırılır

## 6.2 İş Eşleme ve Planlama

### Görev Atama Yöntemleri:
1. **Alt Görevlere Bölme**: Görev → Alt görevler → Makinelere atama
2. **Meta-görev Eşleme**: Bağımsız görev koleksiyonunun sisteme atanması

### Temel Kavramlar:
- **Eşleştirme (Matching)**: Alt görevlerin makineye atanması
- **Zamanlama (Scheduling)**: Yürütme sırasının belirlenmesi
- **Eşleme (Mapping)**: İki sürecin tamamı

## 6.3 Sezgisel Eşleme (Mapping Heuristics)

### Statik Eşleme: 
- Uygulama çalıştırılmadan **önce** kararlar alınır
- Tahmini yürütme süresi önceden bilinir

### Dinamik Eşleme:
- Uygulama yürütülürken kararlar verilir
- **Çevrimiçi Mod**: Görev gelir gelmez eşlenir
- **Toplu Mod**: Planlı zamanlarda gruplar halinde

## 6.4 ETC (Expected Time to Compute) Matrisi

### ETC Özellikleri:
- **Görev Heterojenliği**: Bir makinedeki farklı görevlerin yürütme süresi değişkenliği
- **Makine Heterojenliği**: Bir görevin farklı makinelerdeki yürütme süresi değişkenliği
- **Tutarlılık**:  M1 bir görevi M2'den hızlı çalıştırıyorsa, tüm görevleri hızlı çalıştırır

### Temel Kavramlar: 

| Kavram | Sembol | Açıklama |
|--------|--------|----------|
| **Beklenen Yürütme Süresi** | eij | Makinede yük olmadığında yürütme süresi |
| **Beklenen Tamamlanma Süresi** | cij | İşin tamamlandığı duvar saati süresi |
| **Makine Kullanılabilirlik Süresi** | mat(j) | Makinenin serbest kaldığı en erken zaman |
| **Makespan** | max(cij) | Tüm görevlerin tamamlanma süresi |

**Formül**:  cij = mat(j) + eij

## 6.5 Sezgisel Algoritmalar

### 1. Fırsatçı Yük Dengeleme (OLB)
- Görevleri bir sonraki **boş makineye** atar
- Yürütme süresini dikkate almaz
- Genellikle **zayıf performans**

### 2. Minimum Tamamlama Süresi (MCT)
- Her görevi **en düşük tamamlanma süresini** sunan makineye atar
- Tutarsız ETC matrisleri için iyi performans

### 3. Minimum Yürütme Süresi (MET)
- Her görevi **en az yürütme süresi** gerektiren makineye atar
- **Yük dengesizliğine** neden olabilir

### 4. Min-Min Algoritması

**Adımlar:**
1. Tüm görevler için tüm makinelerdeki tamamlanma süresi hesaplanır
2. Her görev için en düşük tamamlanma süresi bulunur
3. Bu minimumlar arasından en küçüğü seçilir
4. Makine güncellenir, görev çıkarılır, tekrar

### 5. Max-Min Algoritması
- Min-Min'e benzer
- **En erken tamamlanma süresi en fazla** olan görevi seçer
- Uzun görevler fazla olduğunda Min-Min'den iyi

### 6. Genetik Algoritma (GA)

**Evrimsel Yaklaşım:**
1. **Başlangıç Popülasyonu**: Kromozomlar (görev-makine eşlemesi)
2. **Değerlendirme**: Makespan değerine göre uygunluk
3. **Döngü**:
   - Seçim (Selection)
   - Çaprazlama (Crossover)
   - Mutasyon (Mutation)
   - Değerlendirme

## 6.6 Kaynak Seçimi

**Amaç**:  Kullanıcı kısıtlamalarına en uygun kaynakları seçmek. 

**İlişki**:  R_selected ⊆ R_available

### İş Seçim Stratejileri:

| Strateji | Açıklama | Dezavantaj |
|----------|----------|------------|
| **İlk Gelen İlk Hizmeti Alır** | Gönderim sırasına göre | Kaynak israfı, uzun bekleme |
| **Rastgele Seçim** | Rastgele iş seçimi | Adil değil |
| **Önceliğe Dayalı** | En yüksek öncelikli iş | Optimal kriter belirleme zor |

## 6.7 Veri Yoğun Hizmet Planlaması

### Optimizasyon Stratejileri: 
1. Verileri farklı konumlara **kopyalama**
2. İşi **verinin konumuna yakın** işlemciye programlama

### Zamanlayıcı Türleri:
- **ES (External Scheduler)**: Uzak siteyi belirler
- **LS (Local Scheduler)**: Yerel kaynaklarda programlar
- **DS (Dataset Scheduler)**: Veri kümelerini çoğaltır

## 6.8 Hizmet İzleme ve Keşif

### Tanımlar:
- **İzleme**: Kaynakları ve hizmetleri gözlemleme
- **Keşif**: Uygun kaynakları bulma

### Şebeke Bilgi Hizmeti Özellikleri: 
- **Dağıtılmış Mimari**: Merkezi hizmet uygun değil
- **Güncellik**:  "Yaşam süresi" meta verisi
- **Hata Toleransı**: Yumuşak durum modeli
- **Güvenlik**: Kimlik doğrulama ve yetkilendirme

## 6.9 Grid İş Akışı (Grid Workflow)

### Karmaşıklık Sınıflandırması:
- **Doğrusal**: Belirli sırayla, betik dili yeterli
- **Döngüsel Olmayan**: DAG ile temsil, iş akışı dilleri gerekli
- **Döngüsel**: En karmaşık, mesaj alışverişi

## 6.10 Hata Toleransı

### Hata Senaryoları:
1. **Makine Arızası**: İş farklı makineye yeniden zamanlanır
2. **Veri Erişilemezliği**: Veri çoğaltma ile alternatif kaynak

### Arıza Türleri:
- Donanım Arızaları
- Uygulama ve İşletim Sistemi Hataları
- Ağ Hataları
- Yazılım Hataları