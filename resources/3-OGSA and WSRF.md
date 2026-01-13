Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 1

Açık Şebeke Hizmetleri Mimarisi ( Open Grid Services Architecture -OGSA) ve Web 

Hizmetleri Kaynak Çerçevesi ( Web Services Resource Framework -WSRF) 

Bu haftaki konumuz, Grid (Şebeke) hesaplama sistemlerinin standartlaştırılması amacıyla 

geliştirilen Açık Şebeke Hizmetleri Mimarisi (OGSA) ve Web Hizmetleri Kaynak Çerçevesi 

(WSRF) teknolojilerini incelemektedir. 

1. Grid Hesaplamaya Giriş ve Standartlaşma İhtiyacı 

Grid, bilim insanları ve mühendislerin karmaşık sorunları çözmek amacıyla farklı ve dağınık 

donanım/yazılım kaynaklarını birleştiren tek tip bir bilişim ortamıdır. Bu ortamın temel özelliği 

heterojen, yani birbirinden farklı bileşenlerden oluşmasıdır.  

> •

Sorun: Grid sistemlerinin ilk versiyonları (Globus Toolkit 2 gibi) farklı protokollerle 

geliştirildiği için kendi içlerinde de heterojen bir yapıdaydı ve bu durum sistemlerin birlikte 

çalışmasını zorlaştırıyordu.  

> •

Çözüm Arayışı: Bu heterojenliği yönetmek ve standartlar oluşturmak amacıyla Global 

Grid Forum (GGF) adında bir çalışma organı kuruldu. Aynı dönemde IBM ve Microsoft 

gibi teknoloji devlerinin desteklediği Web Servisleri, dağıtık uygulamalar için umut 

vadeden bir platform olarak ortaya çıktı.  

> •

OGSA'nın Doğuşu: Grid ve Web Servisleri dünyalarını birleştirmek amacıyla Globus 

ekibi ve IBM, hizmet odaklı yeni nesil Grid sistemleri için bir mimari olan Açık Şebeke 

Hizmetleri Mimarisi'ni (OGSA - Open Grid Services Architecture) önerdi. Bu, Grid'in 

evriminde önemli bir kilometre taşı oldu. 

2. Temel Teknoloji: Web Servisleri 

OGSA, temelini Web Servisleri teknolojisinden alır. Web Servisleri, istemcilerin servis talep ettiği 

ve sunucuların servis sağladığı sistemlerdir. 

Hizmet Odaklı Mimari'ye (SOA - Service Oriented Architecture) dayanır. CORBA, DCOM 

gibi eski teknolojilerden en büyük farkı, XML ve HTTP gibi basit ve endüstri tarafından yaygın 

olarak kabul görmüş açık standartlara odaklanmasıdır.  

> Figure 1 Dağıtılmış uygulamalar oluşturmak için Web hizmetlerini içeren paradigmalar

Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 2

2.1. Web Servisinin Tanımı ve Özellikleri 

Web hizmeti; bir iç ağ veya internet üzerinden tanımlanabilen, yayınlanabilen, keşfedilebilen ve 

çağrılabilen, gevşek bağlı, kapsüllenmiş, platformdan ve programlama dilinden bağımsız, sunucu 

taraflı bir bileşendir.  

> •

Gevşek Bağlı : Arayüzü değişmediği sürece, bir servisin uygulaması istemciyi 

etkilemeden değiştirilebilir.  

> •

Kapsüllenmiş : Servisin iç uygulaması istemciden tamamen gizlenir.  

> •

Platformdan Bağımsız: Herhangi bir dilde yazılıp herhangi bir platformda çalıştırılabilir.  

> •

Oluşturulabilir : Farklı hizmetlerden yeni hizmetler oluşturulabilir.  

> •

Tanımlı : Yetenekleri XML tabanlı bir arayüzle açıklanır.  

> •

Yayınlanabilir ve Keşfedilebilir : Bir hizmet kayıt defterine (registry) kaydedilerek 

istemciler tarafından bulunabilir.  

> •

Çağrılabilir : HTTP gibi standart protokoller üzerinden bağlanılabilir. 

2.2. Web Servisleri Temel Standartları 

Web servisleri ekosistemi üç temel standart üzerine kuruludur: 

1.  SOAP (Simple Object Access Protocol): İstemci ve sunucuların HTTP gibi bir taşıma 

protokolü üzerinden XML formatında mesaj alışverişi yapmasını sağlayan hafif bir iletişim 

protokolüdür. Bir SOAP mesajı; zarf (envelope), isteğe bağlı bir başlık (header) ve asıl 

mesaj yükünü taşıyan bir gövdede n (body) oluşur.  

> Figure 2 SOAP mesajının yapısı

Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 3

2.  WSDL (Web Services Description Language): Bir web servisinin ne yaptığını, nerede 

bulunduğunu ve nasıl çağrılacağını tam olarak tanımlayan XML tabanlı bir dildir. Bir 

WSDL belgesi; mesajları, operasyonları (portType), protokol bilgilerini (binding) ve 

hizmetin ağ adresini (port) tanımlayan bölüml erden oluşur.  

> Figure 3 Bir WSDL belgesinin yapısı

3.  UDDI (Universal Description, Discovery and Integration): Hizmet sağlayıcıların 

servislerini tanıttığı ve müşterilerin ihtiyaçlarına uygun servisleri bulabildiği bir endüstri 

standardıdır. UDDI kayıtları üç ana bölümden oluşur:  

> o

Beyaz Sayfalar: Sağlayıcı hakkında isim ve iletişim gibi genel bilgiler içerir.  

> o

Sarı Sayfalar: Hizmetleri endüstriyel kategorilere göre sınıflandırır.  

> o

Yeşil Sayfalar: Hizmete nasıl erişileceğini açıklayan WSDL belgesi gibi teknik 

bilgiler içerir. 

Not: UDDI'ye tamamlayıcı bir teknoloji olan WS -Inspection , hizmet açıklamalarının merkezi bir 

kayıt defteri olmadan, doğrudan hizmetin sunulduğu yerde dağıtılmasına olanak tanır .

3. Açık Şebeke Hizmetleri Mimarisi (OGSA) 

OGSA, yeni nesil hizmet odaklı Grid sistemleri oluşturmak için fiili bir standarttır. Temelde Web 

Servisleri mimarisine dayanır ancak Grid ortamının özel ihtiyaçlarını karşılamak için onu 

genişletir. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 4

3.1. OGSA'nın Web Servislerini Genişletme Alanları 

OGSA, Web Servisleri konseptine üç temel alanda yenilik getirir: 

1.  Dinamik Yaşam Döngüsü: Grid ortamındaki hizmetler kalıcı olmak zorunda değildir; 

anlık olarak oluşturulabilir, kullanılabilir ve yok edilebilirler. OGSA, bu yaşam döngüsünü 

yönetmek için arayüzler tanımlar. 

2.  Durum Bilgisi : Standart web servisleri genellikle "durumsuz" iken, Grid hizmetleri 

kendileriyle ilişkili verileri (durumları) tutabilir. 

3.  Bildirim : İstemciler bir hizmetteki değişikliklere abone olabilir ve bir değişiklik 

olduğunda hizmet tarafından bilgilendirilebilirler. 

3.2. OGSA Uygulamaları: OGSI ve Globus Toolkit 3  

> •

OGSI (Open Grid Service Infrastructure): OGSA mimarisinde tanımlanan "Grid 

Servisi" kavramının nasıl uygulanacağını belirten teknik bir şartnamedir. GGF bünyesinde 

geliştirilmiştir.  

> •

Globus Toolkit 3 (GT3): OGSI şartnamesini temel alarak geliştirilmiş, OGSA uyumlu 

hizmet odaklı Grid sistemleri oluşturmak için kullanılan bir araç setidir. 

Ayrıca, Grid üzerindeki veritabanı gibi farklı veri kaynaklarına standart bir şekilde erişmek için 

OGSA -DAI (Data Access and Integration) adı verilen bir ara katman teknolojisi de 

geliştirilmiştir.   

> Figure 4 GT3 yapısı
> Figure 5 OGSA -DAI'nin OGSA'daki konumu

4. Web Hizmetleri Kaynak Çerçevesi (WSRF) 

WSRF, OGSI'daki fikirleri standart Web Servisleri dünyasıyla daha uyumlu hale getiren bir dizi 

spesifikasyondur. Temel amacı, "durum bilgisi olan kaynakları" Web Servisleri bağlamında 

modellemek ve yönetmektir. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 

202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi 

5

4.1. WS -Resource Kavramı 

WSRF'nin merkezinde WS -Resource kavramı yer alır. Bir WS -Resource, durum bilgisi olmayan 

bir Web Servisi ile ilişkilendirilmiş, durum bilgisi olan bir kaynaktır.  

> •

Dinamik olarak oluşturulabilir, benzersiz olarak tanımlanabilir ve yok edilebilir.  

> •

Durumu, ilişkili olduğu Web Servisine gönderilen mesajlar aracılığıyla sorgulanabilir ve 

değiştirilebilir.  

> •

Bir WS -Resource'a erişim, hangi kaynağın hedeflendiğini belirten bilgileri içeren 

WS -Addressing uç nokta referansları aracılığıyla sağlanır. 

4.2. WSRF Spesifikasyonları 

WSRF, aşağıdaki temel WS (Web Service) spesifikasyonlarından oluşur:  

> •

WS -ResourceLifetime: WS -Resource'ların nasıl ve ne zaman yok edileceğini tanımlar.  

> •

WS -ResourceProperties: Bir WS -Resource'un durum bilgilerinin (özelliklerinin) Web 

Servisi arayüzünde nasıl tanımlanacağını belirtir.  

> •

WS -Notification: Olay aboneliği ve bildirim mekanizmaları için bir yayınlama/abonelik 

modeli sunar.  

> •

WS -BaseFaults: Web servisleri arasındaki hata mesajlarını standartlaştırır.  

> •

WS -ServiceGroup: Farklı Web Servislerinin veya WS -Resource'ların bir koleksiyon 

olarak gruplanmasını sağlar.  

> Figure 6 Bir Web hizmeti aracılığıyla durum bilgisi olan bir WS -Resource'a erişme

Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 

202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi 

6

5. WSRF ve OGSA İlişkisi 

OGSA, hizmet odaklı bir Grid için gereken temel servisleri ve mimariyi tanımlarken , WSRF bu 

mimariyi hayata geçirmek için standart bir altyapı sunar.  

> •

OGSA bir mimaridir, WSRF ise bu mimariyi destekleyen bir teknolojidir.  

> •

WSRF, OGSA'nın ihtiyaç duyduğu durum bilgisi yönetimi, yaşam döngüsü ve bildirim 

gibi temel hizmetleri standart Web Servisleri araçlarıyla sağlar.  

> •

Bu nedenle OGSA -WG (OGSA Çalışma Grubu) belgeleri, WSRF'yi OGSA'yı etkinleştiren 

temel teknolojilerden biri olarak kabul eder ve dilini kullanır.