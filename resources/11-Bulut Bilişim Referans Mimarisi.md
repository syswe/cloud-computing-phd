Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 1

1. Bulut Bilişim Referans Mimarisi: Kavramsal Çerçeve 

Bulut Bilişim Referans Mimarisi, bulut bilişim sistemlerinin standart, karşılaştırılabilir ve 

analiz edilebilir bir çerçevede ele alınmasını sağlar. NIST tarafından önerilen bu mimari, bulut 

bilişimin teknik, operasyonel ve yönetsel boyutlarını bütüncül olarak ele alır. 

Bu mimari çerçeve, bulut bilişimin yalnızca bir teknoloji yığını değil; aynı zamanda çok paydaşlı 

bir hizmet ekosistemi olduğunu vurgular. 

2. NIST Bulut Bilişim Referans Modeli ve Aktörler 

Şekil 1. NIST Bulut Bilişim Referans Mimarisi – Aktörler ve Etkileşimler 

(Bulut Tüketicisi, Sağlayıcısı, Aracısı, Taşıyıcısı ve Denetçisi arasındaki kavramsal ilişkiler bu 

şekil üzerinde gösterilmektedir.) 

Şekil 2: Kavramsal Referans Modeli Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 

202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi 

2

Şekil 2'de gösterildiği gibi, NIST bulut bilişim referans mimarisi beş ana aktörü tanımlar: bulut 

tüketicisi, bulut sağlayıcısı, bulut taşıyıcısı, bulut denetçisi ve bulut komisyoncusu. Her aktör, bir 

işleme veya sürece katılan ve/veya bulut bilişimde görevler ge rçekleştiren bir varlıktır (kişi veya 

kuruluş). Tablo 1, NIST bulut bilişim referans mimarisinde tanımlanan aktörleri kısaca açıklar .

Tablo 1: Bulut Bilişimdeki Aktörler         

> Aktör Tanımlaması/Açıklaması
> Bulut Tüketicisi
> Cloud Consumer
> Bulut Sağlayıcıları ile iş ilişkisini sürdüren ve Bulut Sağlayıcılarından hizmet kullanan bir
> kişi veya kuruluş.
> Bulut Sağlayıcısı
> Cloud Provider
> Bir hizmeti ilgili taraflara sunmaktan sorumlu kişi, kuruluş veya kuruluş.
> Bulut Denetçisi
> Cloud Auditor
> Bulut hizmetlerinin, bilgi sistemi operasyonlarının, bulut uygulamasının performansı ve
> güvenliğinin bağımsız değerlendirmesini yapabilen bir taraf.
> Bulut Aracısı
> Cloud Broker
> Bulut hizmetlerinin kullanımını, performansını ve dağıtımını yöneten ve Bulut Sağlayıcıları
> ile Bulut Tüketicileri arasındaki ilişkileri müzakere eden bir varlık.
> Bulut Taşıyıcısı
> Cloud Carrier
> Bulut hizmetlerinin Bulut Sağlayıcılarından Bulut Tüketicilerine bağlanmasını ve
> taşınmasını sağlayan bir aracı.

NIST referans mimarisi, bulut bilişim ortamında etkileşim halinde olan beş temel aktörü tanımlar: 

2.1 Bulut Tüketicisi (Cloud Consumer) 

Bulut tüketicisi, bulut hizmetlerini kullanan nihai kişi veya kuruluştur. Tüketici:  

> •

Hizmet kataloğunu inceler,  

> •

Hizmet talebinde bulunur,  

> •

SLA (Service Level Ag reemnet ) koşullarını kabul eder,  

> •

Kullanım miktarına göre ücretlendirilir. 

Not: SLA’lar, tüketici –sağlayıcı ilişkisinin teknik olduğu kadar hukuki bir boyuta da sahip 

olduğunu gösterir. 

2.2 Bulut Sağlayıcısı (Cloud Provider) 

Bulut sağlayıcısı, altyapıyı kuran, işleten ve hizmet olarak sunan taraftır. Sağlayıcı:  

> •

Fiziksel ve sanal kaynakları yönetir,  

> •

Hizmet sürekliliğinden sorumludur,  

> •

Güvenlik ve gizlilik mekanizmalarını uygular. 

Sağlayıcının sorumluluk düzeyi, SaaS, PaaS ve IaaS hizmet modellerine göre değişiklik gösterir. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 3

2.3 Bulut Denetçisi (Cloud Auditor) 

Bulut denetçisi, bulut hizmetlerinin:  

> •

Güvenlik,  

> •

Performans,  

> •

Gizlilik,  

> •

Mevzuat uyumluluğu 

bakımından bağımsız değerlendirmesini yapar. 

Not : Denetim mekanizması, özellikle kamu kurumları ve regülasyona tabi sektörler için zorunlu 

bir bileşendir. 

2.4 Bulut Aracısı (Cloud Broker) 

Bulut aracısı, tüketici ile sağlayıcı arasındaki karmaşıklığı yöneten aktördür. Üç temel hizmet türü 

sunar:  

> •

Hizmet Aracılığı (Service Intermediation)  

> •

Hizmet Toplama (Service Aggregation)  

> •

Hizmet Arbitrajı (Service Arbitrage) 

2.5 Bulut Taşıyıcısı (Cloud Carrier) 

Bulut taşıyıcısı, bulut hizmetlerinin ağ üzerinden taşınmasından sorumludur. Bu rol, geleneksel 

telekomünikasyon altyapılarını kapsar. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 4

3. Hizmet Modelleri ve Kontrol Kapsamı 

Şekil 3. Bulut Hizmet Modellerinde Kontrol Derinliği (SaaS –PaaS –IaaS) 

(Şekil, hizmet modeli derinleştikçe tüketicinin kontrol ve sorumluluk kapsamının nasıl arttığını 

göstermektedir.) 

Bulut bilişimde üç temel hizmet modeli bulunmaktadır: 

3.1 SaaS – Software as a Service  

> •

Tüketici yalnızca uygulamayı kullanır  

> •

Altyapı ve platform tamamen sağlayıcı kontrolündedir 

3.2 PaaS – Platform as a Service  

> •

Tüketici uygulama geliştirir ve yönetir  

> •

Altyapı kontrolü sağlayıcıdadır 

3.3 IaaS – Infrastructure as a Service  

> •

Tüketici sanal makineler ve işletim sistemlerini yönetir  

> •

Fiziksel altyapı sağlayıcıya aittir 

Not : Hizmet modeli derinleştikçe, tüketicinin kontrolü artar; ancak güvenlik sorumluluğu da 

paralel olarak yükselir. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 5

4. Bulut Dağıtım Modelleri 

Şekil 3. Bulut Dağıtım Modelleri ve Hibrit Bulut Yapısı 

(Genel, özel ve topluluk bulutlarının entegrasyonu ile oluşan hibrit yapı görselleştirilmektedir.) 

4.1 Genel Bulut  

> •

Çok kiracılı yapı  

> •

Yüksek ölçeklenebilirlik  

> •

Daha yüksek güvenlik riskleri 

4.2 Özel Bulut  

> •

Tek kuruluşa tahsisli  

> •

Yüksek kontrol ve güvenlik 

4.3 Topluluk Bulutu  

> •

Ortak amaçlara sahip kurumlar  

> •

Paylaşılan maliyet ve yönetişim 

4.4 Hibrit Bulut  

> •

Birden fazla bulutun entegrasyonu  

> •

Taşınabilirlik ve birlikte çalışabilirlik kritik önemdedir Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 6

5. Mimari Bileşenler ve Hizmet Orkestrasyonu 

Şekil 4. Bulut Hizmet Orkestrasyonu – Üç Katmanlı Mimari Model 

(Hizmet katmanı, kaynak soyutlama ve kontrol katmanı ile fiziksel kaynak katmanı arasındaki 

bağımlılıklar bu şekilde sunulmaktadır.) 

Bulut mimarisi üç katmanlı bir yapı olarak ele alınır: 

1.  Hizmet Katmanı (SaaS, PaaS, IaaS) 

2.  Kaynak Soyutlama ve Kontrol Katmanı 

3.  Fiziksel Kaynak Katmanı 

Bu katmanlı yapı, kaynakların verimli ve güvenli kullanımını sağlar. 

Şekil 5: Bulut Tüketicisine Sunulan Örnek Hizmetler Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 7

SaaS uygulamaları bulutta ve bir ağ aracılığıyla SaaS tüketicilerine erişilebilir hale getirildi. SaaS 

tüketicileri, üyelerine yazılım uygulamalarına erişim sağlayan kuruluşlar, doğrudan yazılım 

uygulamalarını kullanan son kullanıcılar veya son kullanıcılar iç in uygulamaları yapılandıran 

yazılım uygulama yöneticileri olabilir. SaaS tüketicileri, son kullanıcı sayısına, kullanım süresine, 

tüketilen ağ bant genişliğine, depolanan veri miktarına veya depolanan verilerin süresine göre 

faturalandırılabilir. 

PaaS'ın bulut tüketicileri, bir bulut ortamında barındırılan uygulamaları geliştirmek, test etmek, 

dağıtmak ve yönetmek için bulut sağlayıcıları tarafından sağlanan araçları ve yürütme kaynaklarını 

kullanabilir. PaaS tüketicileri, uygulama yazılımı tasarla yan ve uygulayan uygulama geliştiricileri, 

bulut tabanlı ortamlarda uygulamaları çalıştıran ve test eden uygulama test uzmanları, 

uygulamaları bulutta yayınlayan uygulama dağıtımcıları ve bir platformda uygulama 

performansını yapılandıran ve izleyen uygula ma yöneticileri olabilir. PaaS tüketicileri, PaaS 

uygulaması tarafından tüketilen işleme, veritabanı depolama ve ağ kaynaklarına ve platform 

kullanım süresine göre faturalandırılabilir. 

IaaS tüketicilerinin sanal bilgisayarlara, ağdan erişilebilir depolamaya, ağ altyapısı bileşenlerine 

ve üzerinde isteğe bağlı yazılımları dağıtabilecekleri ve çalıştırabilecekleri diğer temel bilgi işlem 

kaynaklarına erişimi vardır. IaaS tüketicileri, BT a ltyapı operasyonları için hizmetler oluşturmak, 

kurmak, yönetmek ve izlemekle ilgilenen sistem geliştiricileri, sistem yöneticileri ve BT 

yöneticileri olabilir. IaaS tüketicilerine bu bilgi işlem kaynaklarına erişme yetenekleri sağlanır ve 

sanal bilgisayar lar tarafından kullanılan CPU saatleri, depolanan verilerin hacmi ve süresi, 

tüketilen ağ bant genişliği, IP adresi sayısı gibi tüketilen kaynakların miktarına veya süresine göre 

faturalandırılır. 

6. Bulut Hizmeti Yönetimi 

6.1 İş Desteği  

> •

Müşteri yönetimi  

> •

Sözleşme ve SLA yönetimi  

> •

Faturalandırma 

6.2 Sağlama ve Yapılandırma  

> •

Hızlı kaynak tahsisi  

> •

İzleme ve ölçüm  

> •

SLA uygulaması 

6.3 Taşınabilirlik ve Birlikte Çalışabilirlik  

> •

Taşınabilirlik eksikliği, bulut sağlayıcı bağımlılığının (vendor lock -in) temel nedenidir. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 

202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi 

8

7. Güvenlik ve Gizlilik 

Bulut bilişimde güvenlik:  

> •

Paylaşılan bir sorumluluktur  

> •

Hizmet ve dağıtım modeline göre değişir  

> •

Kimlik yönetimi, veri bütünlüğü ve denetimi kapsar 

7.1 Gizlilik 

Kişisel verilerin (Personally Identifiable Information - PII ) korunması, bulut bilişimin 

benimsenmesinde kritik bir faktördür. 

Kişisel Tanımlanabilir Bilgiler (PII) : belirli bir bireyi tanımlamak için kullanılabilecek bilgidir. 

Tek başına veya diğer bilgilerle birleştirildiğinde bir kişinin tanımlanmasını sağlayan verileri 

içerir. Örnekler: İsimler, Adresler, Telefon Numaraları, E -posta Adresleri, Sosyal Güvenlik 

Numa raları, Pasaport Numaraları, Sürücü Belgesi Numaraları, Devlet Tarafından Verilen 

Kimlikler (Vergi Kimlikleri), Doğum Tarihi, Irk, Doğum Yeri, vb. 

EK -1: Kısaltmalar (Acronyms)