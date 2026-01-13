Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 1

1. Şebek e Hesaplamaya Giriş (An Introduction to the Grid Computing) 

Şebeke (Grid) kavramı ve teknolojileri, ilk olarak 1998'de Foster ve Kesselman tarafından ifade 

edilmiştir. Bu tarihten önce, geniş alanlı dağıtılmış kaynakları organize etme çabaları “meta bilgi 

işlem ” olarak adlandırılıyordu. “Bir hesaplamalı şebeke ( Grid ), güvenilir, tutarlı, yaygın ve ucuz 

erişim sağlayan üst düzey hesaplama yetenekleri olan bir donanım ve yazılım altyapısıdır .”

Grid, başlangıçta ABD'deki ulusal merkezlerde yüksek performanslı donanımlar üzerinde çalışan 

büyük uygulamaları destekleyen bir altyapıdan, kesintisiz ve dinamik bir sanal ortama doğru 

evrilmiştir. 

Grid ve Dağıtılmış Sistemler Arasındaki Fark 

Grid, bir tür dağıtılmış sistemdir. Dağıtılmış uygulamalar genellikle, kaynakları tek bir sanal 

makinede birleştiren “ara katman (middleware) ” yazılımı üzerinde çalışır. Temel soru, bir 

dağıtılmış sistem ile bir Grid arasındaki farkın ne olduğudur. 

Ian Foster, Carl Kesselman ve Tuecke'nin 2001 ’de yaptığı tanım, günümüzde en yaygın 

kullanılanıdır: “Dinamik, çok kurumlu sanal organizasyonlarda koordineli kaynak paylaşımı ve 

problem çözme .”

Foster daha sonra bir sistemin Grid olarak tanımlanıp tanımlanamayacağını anlamak için üç 

maddelik bir kontrol listesi önermiştir: 

1.  Merkezi Kontrol Olmaması: Sistem, farklı yönetim etki alanlarında bulunan ve merkezi 

bir kontrol noktası olmayan kaynakların koordineli paylaşımını sağlamalıdır. 

2.  Açık Standartların Kullanımı: Standart, açık ve genel amaçlı protokoller ve arayüzler 

kullanılmalıdır. Bu olmazsa, sistem muhtemelen uygulamaya özel bir sistemdir. 

3.  Hizmet Kalitesi: Bileşenler, tek tek parçaların toplamından önemli ölçüde daha büyük 

birleşik hizmetler sunmak için koordineli bir şekilde kullanılmalıdır. Bu hizmetler verim, 

yanıt süresi veya güvenlik gibi metriklerle ölçülebilir. 

Genel olarak Grid, bilgisayarlar, depolama, sensörler ve ağlar gibi kaynakların paylaşımıyla 

ilgilidir. Bu paylaşım; güven, politika, müzakere ve ödeme gibi koşullara bağlıdır. 

2. Şebeke Hesaplamanın Temelleri (Grid Basics) 

Bir Grid sistemi şu özellikleri taşır: 

• Merkezi kontrole tabi olmayan kaynakları koordine eder. 

• Standart, açık, genel amaçlı protokoller ve arayüzler kullanır. 

• Hizmet kalitesi sunar. 

Bir Grid üzerinde paylaşılabilecek temel kaynaklar şunlardır: 

• Bilgi işlem/işlem gücü 

• Veri depolama/ağ bağlantılı dosya 

sistemleri 

• İletişim ve bant genişliği 

• Uygulama yazılımı 

• Bilimsel araçlar Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 2

Temel Kavramlar 

• Grid Ara Yazılımı (Middleware ): Heterojen kaynakların paylaşımını ve sanal 

organizasyonların kurulmasını sağlayan özel bir yazılımdır. Bu yazılım, heterojen altyapı 

ile kullanıcı uygulamaları arasında bir sanallaştırma katmanı sağlar. 

• Grid Computing: Grid ara yazılımı tarafından etkinleştirilen, dinamik bir topluluk içinde 

esnek, güvenli ve koordineli kaynak paylaşımına dayalı bilgi işlem modelidir. 

• Grid Altyapısı: Donanım ve Grid ara yazılımının birleşimidir. Bu altyapı, farklı donanım 

ve veri kaynaklarını, kullanıcıya tek bir bilgisayar gibi görünen bütünleşik bir sanal 

altyapıya dönüştürür. 

• Yardımcı (Utility) Bilişim: Grid Hesaplamanın bir hizmet olarak sunulmasıdır ve 

genellikle “kullanım başına ödeme ” iş modeline dayanır. 

Özetle Grid Computing, BT kaynaklarının günümüzdeki elektrik tüketimine benzer şekilde 

paylaşıldığı ve sağlandığı farklı bir bilgi işlem paradigma sıdır. 

3. Şebeke ile İlgili Standartlar (Grid -Related Standards) 

Grid teknolojilerinin yaygın olarak benimsenmesi için standartlara uyum hayati önem taşır. Bu 

alandaki en önemli standart kuruluşları şunlardır: 

• Global Grid Forum (GGF): Grid için birincil standart belirleyici kuruluştur. 

• OASIS: Kâr amacı gütmeyen bir standartlar konsorsiyumudur. 

• Distributed Management Task Force (DMTF) : Bulut, sanallaştırma, ağ, sunucular ve 

depolama gibi çeşitli yeni ve geleneksel BT altyapılarını kapsayan açık yönetilebilirlik 

standartları oluşturan, kâr amacı gütmeyen bir endüstri standartları kuruluşudur. 

• World Wide Web Consortium (W3C) : Web serv isler ve ö zellikle XML ile ilgili Web 

hizmetleri standartlarını belirlemede aktiftir. 

GGF, standartlarla ilgili dört tür belge üretir: 

• Bilgilendirici (Informational): Topluluğu faydalı bir fikir hakkında bilgilendirir. 

• Deneysel (Experimental): Yararlı bir deney, test ortamı veya bir fikrin uygulanması 

hakkında bilgi verir. 

• Topluluk Uygulaması (Community Practice): Ortak uygulamalar veya süreçler 

hakkında topluluğu bilgilendirmeyi amaçlar. 

• Öneriler (Recommendations): GGF tarafından önerilen standartları içerir; örneğin, Açık 

Şebeke Hizmetleri Altyapısı (OGSA). 

4. Şebekenin Mimarisi (Architecture of the Grid) 

En önemli standartlardan biri, GGF tarafından geliştirilen Açık Şebeke Hizmetleri Mimarisi 

(Open Grid Services Architecture - OGSA )’dır. OGSA, Grid tabanlı uygulamalar için ortak, 

standart ve açık bir mimari tanımlar. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 3

OGSA, temel teknoloji olarak Web Hizmetlerini kullanan bir Hizmet Odaklı Mimari (Service -

Oriented Architecture - SOA) belirtir. Bu standart temel olarak servis arayüzlerini ve bu 

servisleri çağırmak için gerekli protokolleri tanımlar. 

OGSA'nın üzerine inşa edildiği Web Hizmetleri standartları ve özellikleri şunları içerir: 

• Programdan programa etkileşim: SOAP, WSDL, UDDI 

• Veri paylaşımı: XML 

• Mesajlaşma: SOAP, WS -Addressing 

• Güvenilir mesajlaşma: WS -ReliableMessaging 

• Kaynak yönetimi: WS -RF (Web Services Resource Framework) 

• Güvenlik: WS -Security, WS -Trust 

İş süreci akışı: Web Servisleri için İş Süreci Yürütme Dili (Business Process Execution 

Language for Web Services - BPEL4WS ) kullanılarak, işlemlerin veya görevlerin belirli 

bir sırada ve kurallara göre bir araya getirilerek otomatize edilmesidir. 

• Olay tetikleme: WS -Notification 

5. Şebeke Mimarileri ve İşlevselliği (Grid Architectures and Functionality) 

Bir Grid mimarisi, bileşenlerin amaçlarını, işlevlerini ve birbirleriyle nasıl etkileşime girdiklerini 

tanımlar. Protokoller genellikle katmanlar halinde düzenlenir. Bu katmanlar şunlardır: 

1.  Fabric ( Donanım ) Katmanı : Grid içinde paylaşılan fiziksel kaynakları içerir. Bunlar; 

hesaplama kaynakları, depolama sistemleri, ağlar ve sensörlerdir. 

2.  Connectivity (Bağlantı) Katmanı: Temel iletişim ve kimlik doğrulama protokollerini içerir. 

Veri alışverişi, yönlendirme, adlandırma ve güvenli iletişim gibi işlevler bu katmanda yer alır. 

3.  Resource (Kaynak) Katmanı: Bireysel kaynakların paylaşımı için güvenli görüşme, 

başlatma, izleme ve ödeme gibi fonksiyonları kontrol eder. Bu katman, kaynakların yapısı ve 

durumu hakkında bilgi sağlayan protokolleri ve kaynaklara erişimi müzakere eden yönetim 

protokollerini içerir. 

4.  Collective (Kolektif) Katman: Kaynak koleksiyonları ile etkileşimden ve küresel kaynak 

yönetiminden sorumludur. Dizin hizmetleri, zamanlama, aracılık, izleme ve veri çoğaltma gibi 

hizmetler bu katmanın önemli işlevleridir. 

5.  Application (Uygulama) Katmanı: Grid üzerinde konuşlandırılan kullanıcı uygulamalarını 

içerir. Yalnızca “Grid -etkin ” (Grid -enabled), yani paralel çalışacak şekilde tasarlanmış 

uygulamalar bu altyapıdan tam olarak yararlanabilir. 

Bu beş katman, Grid ara yazılımını oluşturur. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 4

6. Şebekelerin Sınıflandırılması (Classification of Grids) 

Grid Computing, odaklanılan kaynaklara ve kaynak paylaşımının kapsamına göre 

sınıflandırılabilir. 

6.1. Kaynak Odağına Göre Sınıflandırma 

• Hesaplama Şebekeleri (Computational Grids): CPU gibi bilgi işlem kaynaklarının 

paylaşımına odaklanır. 

• Veri Şebekeleri (Data Grids): Büyük ölçekli, heterojen ve dağıtılmış verilerin yönetimine 

ve paylaşımına odaklanır. 

• Uygulama Şebekeleri (Application Grids): Uzak yazılımlara ve kütüphanelere şeffaf 

erişim sağlanması ile ilgilenir. 

Servis Şebekeleri (Service Grids): Hizmetlerin verimli paylaşımını destekler ve Grid ile 

Hizmet Odaklı Bilişim'in yakınsamasından doğmuştur. 

6.2. Kaynak Paylaşımı Kapsamına Göre Sınıflandırma 

• Küme Şebekeleri (Cluster Grids): Yüksek hızlı bir yerel ağ ile birbirine bağlı, ortak 

konumlu bilgisayarlar topluluğudur ve tek bir kaynak olarak kullanılır. 

• Kurumsal Şebekeler (Enterprise Grids): Tek bir şirket sınırları içinde kaynakların 

paylaşılmasıdır. Bileşenler şirketin güvenlik duvarı içindedir ancak coğrafi olarak 

dağıtılmış olabilir. 

• Yardımcı Şebeke Hizmetleri (Utility Grid Services): Üçüncü taraf bir hizmet 

sağlayıcının sahip olduğu ve dağıttığı bir şebekedir. Hizmetler, "kullanım başına ödeme" 

esasına göre sunulur ve kullanıcının güvenlik duvarı dışında çalışır. 

• İş Ortağı/Topluluk Şebekeleri (Partner/Community Grids): Farklı kurumlar arasında 

iş birliği ve kaynak paylaşımını sağlar. Bu iş birliği genellikle bir Sanal Organizasyon 

(Virtual Organization - VO) ile sonuçlanır. Başlangıçta e -Bilim (eScience) alanında 

ortaya çıkmış olup, günümüzde küresel tedarik zincirleri gibi iş dünyası süreçlerinde de 

kullanılmaktadır.