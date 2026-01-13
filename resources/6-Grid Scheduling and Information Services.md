Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and 

> Cloud Computing) Dersi

1

1. Şebeke Çizelgeleme ve Bilgi Hizmetleri (Grid Scheduling and Information Services) 

Şebeke (grid) sistemlerinde çizelgeleme ve bilgi hizmetleri, bir uygulamanın genel performansını doğrudan 

etkileyen iki temel bileşendir . Bilgi hizmetleri, şebeke kaynaklarının (işlemciler, bellek, ağ bant genişliği vb.) 

durumu ve kullanılabilirliği hakkında bilgi sağlayarak çizelgeleme sistemini tamamlar .

Bir işi belirli bir düğümde zamanlamak için iki temel soruya yanıt gerekir :

1.  Kaynak, işin minimum ve özel Kalite Servisi (QoS) gereksinimlerini karşılıyor mu? 

2.  Kaynak, işe hizmet vermek için uygun mu? 

Bu soruların yanıtları bilgi servisleri tarafından sağlansa da , çizelgeleme kararları genellikle daha karmaşıktır. 

Örneğin, bir görev farklı düğümlerde çalışacak ve birbirine bağımlı alt görevlerden oluşabilir . Veya büyük bir 

girdi dosyasına sahip bir işin, veri aktarım maliyetini en aza indirmek için verinin konumuna yakın bir düğüme 

zamanlanması gerekebilir . Donanım veya ağ arızası durumunda ise, şebeke zamanlayıcısının görevi bilgi 

servisinden aldığı verilerle farklı bir düğüme yeniden planlaması gerekir .

Şebeke bilgi hizmetleri büyük ölçekli ve coğrafi olarak dağınık olduğundan, merkezi bir mimari yerine hiyerarşik 

bir yapı kullanılır . Bu yapı, tek hata noktası oluşmasını engeller ve ölçeklenebilirliği artırır . Sonuç olarak, iyi bir 

yürütme çizelgesinin tasarımı, bilgi servisleri tarafından sağlanan güncel ve doğru bilgilere sıkı sıkıya bağlıdır .

2. İş Eşleme ve Planlama (Job Mapping and Scheduling) 

Şebekeler, heterojen kaynakların koordineli kullanımını sağlayarak birleşik performansı en üst düzeye çıkarmayı 

amaçlar . Bu yapıları nedeniyle şebekeler, heterojen bilgi işlem (Heterogeneous Computing - HC) sistemleri olarak 

da adlandırılabilir . Bu tür sistemlerde, görevlerin genel yürütme süresini en aza indirmek için her göreve doğru 

kaynağın atanması kritik öneme sahiptir .

Görevlerin HC sistemlerine atanması iki temel yolla yapılır: 

1.  Alt Görevlere Bölme: Bir görev, birden çok alt göreve bölünür . Her alt görev, makineye özel 

gereksinimleri karşılayan bir makineye atanır . Bu atama işlemine eşleştirme (matching) denir . Alt 

görevlerin yürütme sırasının belirlenmesine ise zamanlama (scheduling) denir . Bu iki sürecin tamamı 

eşleme (mapping) olarak adlandırılır .

2.  Meta -görev Eşleme: Birbirinden bağımsız bir görev koleksiyonu (meta -görev olarak adlandırılır) sisteme 

atanı r. Meta -görevlere örnek olarak, farklı kullanıcılar tarafından sisteme gönderilen işler verilebilir .

2.1. Sezgisel Eşleme (Mapping Heuristics) 

Görevleri eşlemeye yönelik sezgisel yöntemler, kararların ne zaman alındığına göre sınıflandırılır:  

> •

Statik Eşleme: Eşleştirme ve zamanlama kararları, uygulama çalıştırılmadan önce alınır . Bu yöntemler, 

bir görevin her makinedeki tahmini yürütme süresinin önceden bilindiğini varsayar . Bu tahminlerin 

doğruluğu, eşlemenin başarısını doğrudan etkiler . 

> •

Dinamik Eşleme: Kararlar, uygulama yürütülürken verilir . 

> •

Çevrimiçi Mod: Görev, sisteme gelir gelmez bir makineye eşlenir . 

> •

Toplu Mod: Görevler, önceden planlanmış belirli zamanlarda (eşleme olayları) gruplar halinde eşlenir .Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and 

> Cloud Computing) Dersi

2

Beklenen Hesaplama Süresi (ETC) Matrisi 

Eşleme algoritmaları, Beklenen Hesaplama Süresi (Expected Time to Compute - ETC) olarak bilinen bir matrisi 

kullanır . Bu matris, şebekedeki tüm görevlerin tüm makinelerdeki beklenen yürütme sürelerini içerir . ETC 

matrisleri şu özelliklere sahip olabilir:  

> •

Görev Heterojenliği: Belirli bir makinedeki görevlerin yürütme sürelerindeki değişkenlik . 

> •

Makine Heterojenliği: Belirli bir görevin farklı makinelerdeki yürütme sürelerindeki değişkenlik . 

> •

Tutarlılık: Tutarlı bir ETC matrisinde, eğer bir M1 makinesi bir T1 görevini M2 makinesinden daha hızlı 

çalıştırıyorsa, M1 diğer tüm görevleri de M2'den daha hızlı çalıştırır . Tutarsız matrislerde böyle bir 

sıralama yapılamaz .

Temel Kavramlar  

> •

Beklenen Yürütme Süresi (Expected Execution Time ): Bu, makinede yük olmadığında bir makinede 

bir görevin yürütülmesi için tahmini süredir. e ij , t i görevinin m j makinesinde beklenen yürütme süresini 

belirtir.  

> •

Beklenen Tamamlanma Süresi (Expected Completion Time ): mj makinesinin ti görevinin 

yürütülmesini tamamladığı duvar saati süresini (Wall clock time) belirtir. Bu, t i görevi atanmadan önce m j

makinesine önceden atanmış herhangi bir görevi tamamlamak için gereken süreyi içerir ve cij ile gösterilir.  

> •

Makine Kullanılabilirlik Süresi ( Machine Availability Time ): Bir makinenin serbest kaldığı en erken 

zamandır. Bu, daha önce kendisine atanan tüm görevleri yerine getirdiği anlamına gelir. mat( j) ile 

gösterilir. Yani , cij =mat( j)+e ij yukarıdaki tanımlardan türetilebilir.  

> •

Duvar saati zamanı (Wall clock time) : Bir işlemin çalışmaya başlaması ile bitmesi arasında geçen süre. 

Bu, genellikle işlem tarafından tüketilen işlemci süresinden daha uzundur, çünkü CPU, diğer kullanıcı ve 

işletim sistemi işlemlerini çalıştırmak veya disk veya ağ G/Ç'sini beklemek gibi işlem i çalıştırmanın yanı 

sıra başka şeyler de yapmaktadır.  

> •

Makespan , max(c ij ) olarak tanım lanı r. Meta görevdeki tüm görevlerin yürütmeyi tamamlaması için geçen 

maksimum süreyi belirtir. Sistemin çıktısının bir ölçüsüdür. Ancak, bireysel görevlerin QoS 

gereksinimlerini karşılamaz. Şimdi literatürde açıklanan önemli haritalama buluşsal tekniklerini 

tartışıyoruz. 

2.1.1. Fırsatçı Yük Dengeleme (Opportunistic Load Balancing) 

Bu basit algoritma, görevleri bir sonraki uygun (boş) makineye atar . Görevin o makinedeki beklenen yürütme 

süresini dikkate almaz . Bu nedenle genellikle zayıf bir performans sergiler .

2.1.2. Hızlı Açgözlü veya Minimum Tamamlama Süresi (MCT) 

Bu sezgisel yöntem, her bir görevi, o görev için en düşük tamamlanma süresini sunan makineye atar 43 . Tutarsız 

ve yarı tutarlı ETC matrisleri için genellikle iyi performans gösterir .Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and 

> Cloud Computing) Dersi

3

2.1.3. Kullanıcı Yönlü Atama veya Minimum Yürütme Süresi (MET) 

Bu yaklaşım, her görevi, o görevin yürütülmesi için en az yürütme süresi gerektiren makineye atar . Makine 

kullanılabilirlik süresini dikkate almadığı için özellikle tutarlı ETC matrislerinde ciddi yük dengesizliğine neden 

olabilir .

2.1.4. Min -Min 

Min -Min algoritması, meta -görev için küçük bir makespan üretme fikrine dayanır .

1.  Tüm görevler için tüm makinelerdeki beklenen tamamlanma süresi hesaplanır .

2.  Her görev için en düşük tamamlanma süresi bulunur .

3.  Bu minimum tamamlanma süreleri arasından en küçüğü seçilir ve bu görev ilgili makineye atanır .

4.  Makinenin kullanılabilirlik süresi güncellenir, atanan görev listeden çıkarılır ve tüm görevler atanana 

kadar işlem tekrarlanır .

2.1.5. Max -Min 

Max -Min, Min -Min'e benzer . İlk adımı aynıdır . Ancak ikinci adımda, en erken tamamlanma süresi en az olan 

görevi seçmek yerine, en erken tamamlanma süresi en fazla olan görevi seçer ve ilgili makineye atar . Bu yaklaşım, 

uzun görevlerin sayısı kısa görevlerin sayısından fazla olduğunda Min -Min'den daha iyi performans gösterir .

Çünkü uzun görevler önce planlanır ve daha kısa görevler bu uzun görevlerle eş zamanlı olarak yürütülebilir .

2.1.6. Genetik Algoritma (GA) 

Genetik Algoritma (GA), görevleri makinelere eşlemek için evrimsel bir yaklaşım kullanır .

1.  Başlangıç Popülasyonu: Her biri olası bir çözümü (görev -makine eşlemesi) temsil eden bir dizi 

kromozom (vektör) oluşturulur .

2.  Değerlendirme: Her kromozomun uygunluğu, ürettiği makespan değerine göre değerlendirilir. Daha 

düşük makespan , daha yüksek uygunluk anlamına gelir .

3.  Döngü: Belirli bir durdurma kriteri (örneğin, yineleme sayısı) karşılanana kadar aşağıdaki adımlar 

tekrarlanır : 

> o

Seçim (Selection): Daha uygun kromozomlar yeni nesil için seçilir . 

> o

Çaprazlama (Crossover): İki kromozom arasında genetik materyal (görev atamaları) 

değiştirilerek yeni kromozomlar oluşturulur . 

> o

Mutasyon (Mutation): Bir kromozomdaki bir görev ataması rastgele değiştirilir . 

> o

Değerlendirme: Yeni nesil değerlendirilir .

GA, genellikle tüm ETC matris tipleri için en iyi performansı gösterir . Ancak, eşleme algoritmasının yürütme 

süresi önemliyse ve ETC matrisi tutarlıysa, Min -Min daha iyi bir seçenek olabilir .Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and 

> Cloud Computing) Dersi

4

2.2. Programlama Algoritmaları ve Stratejileri 

Şebeke ortamında iş çizelgelemesi, tek bir paralel bilgisayardakinden farklıdır, çünkü her biri farklı yerel 

politikaya sahip birçok makineyi içerir . Bu karmaşıklığı yönetmek için yerel iş planlayıcıların üzerine bir meta -

zamanlayıcı yerleştirilir . Meta -zamanlayıcı, işleri farklı yerel zamanlayıcılara dağıtmaktan sorumludur .

Bir şebeke çizelgeleme sistemi üç ana bileşenden oluşur :

1.  Çizelgeleme Politikası: Makine sahibi tarafından tanımlanan ve kaynak tahsisini belirleyen kurallar 

bütünüdür .

2.  Amaç Fonksiyonu: Bir çizelgeye sayısal bir değer atayarak en iyi çizelgenin seçilmesine yardımcı olur .

Genellikle sistemin maksimize veya minimize etmeye çalıştığı parametrelerden oluşur .

3.  Çizelgeleme Algoritması: Seçilen amaç fonksiyonuna göre optimale yakın bir çizelge üretmelidir .

2.3. Veri Yoğun Hizmet Planlaması 

Yüksek enerji fiziği gibi uygulamalar çok büyük miktarda veri üretir ve bu verilere erişir . Bu tür uygulamalarda 

veri aktarım süresi, genel yürütme süresini önemli ölçüde etkileyebilir . Bu nedenle, zamanlama kararları verilerin 

konumunu dikkate almalıdır . İki temel optimizasyon stratejisi şunlardır: 

1.  Verileri farklı konumlara kopyalamak (çoğaltma) .

2.  İşi, verinin bulunduğu konuma yakın bir işlemciye programlamak .

Gridbus aracısı gibi kaynak aracıları, kullanıcı gereksinimlerini en uygun kaynaklara eşlerken, hesaplama 

kaynakları ile veri kaynakları arasındaki ağ yakınlığını (mevcut bant genişliği) dikkate alır .

Bu tür uygulamalar için geliştirilen bir sistem modeli üç tür zamanlayıcı içerir : 

> •

Harici Zamanlayıcı (External Scheduler - ES): Kullanıcı işlerini alır ve işin gönderileceği uzak siteyi 

belirler . 

> •

Yerel Zamanlayıcı (Local Scheduler - LS): Uzak bir siteden gelen işleri yerel kaynaklarda programlar . 

> •

Veri Kümesi Zamanlayıcısı (Dataset Scheduler - DS): Sık erişilen veri kümelerini uzak sitelerde 

çoğaltarak verilerin popülerliğini yönetir .

3. Hizmet İzleme ve Keşif (Service Monitoring and Discovery) 

Zamanlayıcının bir işi uygun kaynaklara eşleyebilmesi için, şebekenin mevcut kaynakların ve bu kaynakların 

durumlarının (meşgul/uygun) farkında olması gerekir . 

> •

İzleme (Monitoring): Kullanım modellerini veya hataları tespit etmek için kaynakları ve hizmetleri 

gözlemleme sürecidir . 

> •

Keşif (Discovery): Belirli bir görevi gerçekleştirmek için uygun kaynakları bulma sürecidir .

Kaynakların sisteme haber vermeden katılabildiği veya ayrılabildiği dinamik bir şebeke ortamında verimli bir 

keşif mekanizması zorunludur . Bir şebeke bilgi hizmetinin sahip olması gereken özellikler şunlardır:  

> •

Dağıtılmış Mimari: Coğrafi olarak dağıtılmış kaynaklar ve arıza olasılığı nedeniyle merkezi bir hizmet 

uygun değildir . 

> •

Güncellik: Kaynak durumu değişebileceğinden, bilgiler bayatlayabilir . Bu nedenle, bilgilerle birlikte bir 

"yaşam süresi" meta verisi tutulmalıdır . 

> •

Hata Toleransı: Bilgi sistemi, kaynak veya ağ arızalarına karşı dayanıklı olmalıdır . Yumuşak durum 

(soft -state) modeli kullanılır: Bir kaynak hakkındaki bilgi, sağlayıcıdan zamanında bildirim alınarak 

yenilenmezse sistemden atılır . 

> •

Güvenlik: Bilgiler, yalnızca talep edenin kimliği doğrulandıktan ve yeterli yetkiye sahip olduğu 

anlaşıldıktan sonra sağlanmalıdır . Bu, güçlü bir kimlik doğrulama ve yetkilendirme mekanizması 

gerektirir .Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and 

> Cloud Computing) Dersi

5

4. Izgara İş Akışı (Grid Workflow) 

Izgara iş akışı, belirli bir sorunu çözmek veya yeni bir hizmet oluşturmak için birkaç farklı faaliyetin veya 

hizmetin (alt süreçler) birleştirilmesi ve otomasyonudur . Bu süreç, hizmetler arasında kontrol ve veri 

bağımlılıkları aracılığıyla koordinasyon gerektirir . Örneğin, bir A alt görevi, B alt görevinin ürettiği sonuca 

ihtiyaç duyabilir ve bu nedenle B tamamlandıktan sonra çalışmalıdır .

Izgara iş akışları karmaşıklıklarına göre sınıflandırılabilir:  

> •

Doğrusal (Linear): Görevler belirli bir doğrusal sırayla gerçekleştirilir . Tanımlanması basittir ve 

genellikle bir betik dili yeterlidir . 

> •

Döngüsel Olmayan (Non -cyclic): Görevler ve aralarındaki bağımlılıklar, yönlendirilmiş döngüsel 

olmayan grafikler (DAG) olarak temsil edilebilir . Bu tür iş akışları, iş akışı dillerinin kullanılmasını 

gerektirir . 

> •

Döngüsel (Cyclic): En karmaşık seviyedir . Grafikteki kenarlar, bir dizi mesaj alışverişi yoluyla birbirine 

bağlanan hizmetleri temsil eder .

5. Şebekelerde Hata Toleransı (Fault Tolerance in Grids) 

Şebekelerdeki makineler bozulabilir veya ağ arızaları nedeniyle erişilemez hale gelebilir . Hata toleransı, bu tür 

durumların kullanıcı için şeffaf bir şekilde ele alınmasını sağlar; kullanıcı şebekeyi tek bir sanal makine olarak 

görür ve arızalarla ilgilenmek zorunda kalmaz .

İki temel hata senaryosu ve çözüm stratejisi vardır: 

1.  Makine Arızası: Bir işi yürüten makine kapanırsa, iş farklı bir makineye yeniden zamanlanır (re -

scheduling) .

2.  Veri Erişilemezliği: Uzak bir konumdaki veriye ağ bağlantısı kesilirse, şebeke veri çoğaltma (data 

replication) stratejisini kullanarak alternatif veri kaynaklarını bulmaya çalışır .

Şebekelerde meydana gelebilecek arıza türleri şunlardır:  

> •

Donanım Arızaları: CPU, bellek veya depolama aygıtlarındaki arızalardan kaynaklanır . 

> •

Uygulama ve İşletim Sistemi Hataları: Bellek sızıntıları, kilitlenmeler veya hatalı kaynak yönetimi gibi 

sorunları içerir . 

> •

Ağ Hataları: Ağların fiziksel olarak zarar görmesi veya düğümlerin düşmesi sonucu oluşur ve önemli 

paket kaybına neden olabilir . 

> •

Yazılım Hataları: Sıfıra bölme veya beklenmeyen girdi gibi işlenmeyen istisnai durumlar nedeniyle 

oluşabilir .