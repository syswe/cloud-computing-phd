Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 202 5-202 6 Güz Dönemi 

> BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi

1

1.  Bulut Bilişimin NIST (National Institute of Standards and Technology) tarafından 

yapılan tanım, bulut bilişimi modern bilişim teknolojilerinin temel omurgalarından biri 

hâline getirmiştir. NIST’e göre bulut bilişim: 

“Paylaşılan, yapılandırılabilir bilgi işlem kaynakları havuzuna (ağlar, sunucular, depolama, 

uygulamalar, hizmetler) her yerden, hızlı, isteğe bağlı ve minimum yönetim çabasıyla erişim 

sağlayan bir modeldir.” 

NIST Bulut Bilişim Tanımı yla ilişkili teri mler ve bunlarla ilişkili tanımlar dan oluş maktadır. 

Bulut bilişim modelinin temel tanımı ( yukarıda verilmiştir )

Beş temel özellik 

• İsteğe bağlı self -servis (On -demand self -service) 

• Geniş ağ erişimi (Broad network access) 

• Kaynak havuzu (Resource pooling) 

• Hızlı esneklik (Rapid elasticity) 

• Ölçülen hizmet (Measured service )

o Üç hizmet modeli (Three service models) 

▪ Hizmet Olarak Yazılım (Software as a Service - SaaS) 

▪ Hizmet Olarak Platform (Platform as a Service -PaaS) 

▪ Hizmet Olarak Altyapı (Infrastructure as a Service -IaaS) 

Dört dağıtım modeli (deployment models) 

• Genel (Public) 

• Özel (Private) 

• Toplum (Community) 

• Hibrit (Hybrid) 

NIST tanımı, hem teknik hem de operasyonel perspektifi içeren referans bir çerçeve sunar. Bu 

çerçeve, bulut teknolojilerinin değerlendirilmesinde evrensel bir standart olarak kabul 

edilmektedir. 

2. Bulut Bilişimin Beş Temel Özelliği (NIST Essential Characteristics) 

Bu özellikler olmadan bir hizmet “bulut hizmeti” olarak sınıflandırılamaz. Her özellik için NIST 

iki doğrulama yaklaşımı sunar: 

• Bulut Hizm et Sağlayıcısı (Cloud Service Provider -CSP )

• Bulut Hizmet Tüketicisi /Müşterisi (Cloud Service Customer -CSC )

• Bu belge bağlamında “gerekli -essential ”, her bulut hizmeti sağlayıcısının (cloud 

service provider -CSP), belirli bir hizmet için bulut hizmeti müşterisine (cloud service 

customer -CSC) her temel özelliği sağlama yeteneğine sahip olması gerektiği anlamına 

gelir. CSC, gereksinimlerinin karşılanıp karşılanmadığını belirlemek ve CSP'nin Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 202 5-202 6 Güz Dönemi 

> BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi

2

teklifinin kendi amaçları için bir bulut hizmeti olarak kabul edilip edilemeyeceğine 

karar vermek için öznel bir yargıda bulunmalıdır. 

NIST'in değerlendirme yaklaşımında her bulut özelliği için iki tür seçenek bulunur: 

A Seçeneği (Nesnel ölçüt) 

• Tüm bulut kullanıcıları (CSC’ler) için ortak ve standart gereksinimlere dayanır. 

• Her durumda aynı şekilde yorumlanabilir. 

• Farklı kurumlar arasında karşılaştırma yapmaya uygundur. 

• Bu nedenle daha genel, daha ölçülebilir ve daha evrensel bir yaklaşımdır. 

B Seçeneği (Öznel ölçüt - CSC ihtiyacına bağlı )

• Belirli bir kullanıcının ya da kullanıcı grubunun kendine özgü ihtiyaçlarına göre değişir. 

• Daha çok algılanan performans gibi sübjektif kriterlere dayanır. 

• Bir CSC, B seçeneğini kullanıyorsa, bu değerlendirmenin yalnızca kendi bağlamında 

anlamlı olduğunu bilmelidir. 

• Farklı kullanıcılara göre değiştiğinden CSC’ler arasında karşılaştırma yapmak uygun 

değildir .

Önemli Not : Bir özellik için yalnızca tek bir seçenek varsa, bu otomatik olarak A Seçeneği 

sayılır. 

Tablo 1. NIST Bulut Bilişimin Beş Temel Özelliği 

Özellik  Tanım  Seçenek A 

(Nesnel) 

Seçenek B (Öznel)  Sağlayan/Onaylayan 

İsteğe Bağlı 

Self -Servis 

Hizmetlere kullanıcı 

talebiyle erişim 

Tam otomatik 

provizyon 

Ön yüz otomatik, 

arka uç kısmen 

manuel 

CSP 

Geniş Ağ 

Erişimi 

Standart protokollerle 

çoklu istemciden 

erişim 

İnternet üzerinden 

erişim 

Kuruma özel ağ 

üzerinden erişim 

CSC/CSP 

Kaynak 

Havuzu 

Çok kiracılı, dinamik 

kaynak paylaşımı 

≥ 2 CSC tarafından 

paylaşım 

— CSP 

Hızlı 

Esneklik 

Dinamik ölçekleme  Gerçek zamanlı 

otomatik 

ölçekleme 

CSC ihtiyacını 

karşılayacak hızda 

CSC/CSP 

Ölçülen 

Hizmet 

Otomatik ölçüm, 

izleme ve raporlama 

Kaynakların 

detaylı ölçümü 

— CSC Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 202 5-202 6 Güz Dönemi 

> BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi

3

2.1. İsteğe Bağlı Self -Servis (On -Demand Self -Service) 

Bir tüketici, hizmet sağlayıcıyla insan etkileşimi olmadan; sunucu zamanı, depolama, işlem 

birimi gibi kaynakları otomatik olarak talep edebilir. 

Birincil Kriter  

> •

Hizmet, CSC tarafından tek taraflı ve otomatik olarak sağlanabilir. 

Seçenekler 

A) Tam otomatik provizyon (arka uç tamamen otonom çalışır). 

B) Ön yüz otomatik; arka uç kısmen manuel olabilir. 

Fayda  

> •

Zaman kazanımı, otomasyon, hızlı kaynak temini. 

Önemli Not : Bu özellik, bulut bilişimi geleneksel hosting’den ayıran en kritik parametredir. “Tek 

taraflı” erişim, kurumsal iş akışlarında otomasyonun temelini oluşturur. 

2.2. Geniş Ağ Erişimi (Broad Network Access) 

Bulut kaynaklarına standart internet protokolleri aracılığıyla çok farklı istemcilerden 

erişilebilmelidir. 

Birincil Kriter  

> •

Kaynaklar geniş ağ üzerinde, HTTP/HTTPS, REST, TCP/IP gibi protokollerle erişilebilir 

olmalıdır. 

Seçenekler 

A) İnternet üzerinden erişilebilirlik. 

B) Kurumun gerektirdiği herhangi bir ağ üzerinden erişim. 

Fayda  

> •

Hızlı erişim, mobilite, küresel erişilebilirlik. 

2.3. Kaynak Havuzu (Resource Pooling) 

CSP’nin altyapısı, çoklu kiracılı (multi -tenant) bir modelle dinamik olarak kaynakları paylaştırır. 

Birincil Kriter  

> •

En az iki CSC’nin paylaşabileceği altyapı. 

Fayda  

> •

Maliyetlerin paylaşılması, yüksek ölçeklenebilirlik. 

Önemli Not : Multi -tenancy modeli, bulut ekonomisinin merkezidir. Bu model olmadan bulutun 

maliyet avantajı oluşmaz. 

2.4. Hızlı Esneklik (Rapid Elasticity) 

Kaynaklar, talebe göre otomatik olarak büyüyebilir veya küçülebilir . Kullanıcıya sınırsız 

görünür. 

Birincil Kriter  

> •

Kaynak tahsisinde hızlı ölçeklenebilirlik. 

Seçenekler 

A) Gerçek zamanlı otomatik ölçekleme 

B) Otomatik olmasa da CSC’nin ihtiyacını karşılayacak kadar hızlı 

Fayda  

> •

Talep patlamalarıyla başa çıkma (ör. e -ticaret kampanyaları). Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 202 5-202 6 Güz Dönemi 

> BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi

4

2.5. Ölçülen Hizmet (Measured Service) 

Kaynak kullanımı otomatik ölçülür, izlenir, raporlanır .

Birincil Kriter  

> •

Kaynak ölçümü CSC ihtiyaçlarını karşılayacak detayda olmalıdır. 

Önemli Not : Ölçümleme, bulut ekonomisinin temelidir. Kullanım bazlı ücretlendirme (pay -as -

you -go), bulutun finansal modelini oluşturur. 

3. Bulut Hizmeti Modelleri: SaaS, PaaS, IaaS 

NIST’e göre bulut hizmetleri üç üst kategoriye ayrılır. 

3.1. SaaS – Hizmet Olarak Yazılım 

Kullanıcı uygulamayı kullanır; altyapı, platform veya uygulamanın teknik bileşenleri üzerinde 

kontrol sahibi değildir. 

Temel Özellikler  

> •

Yazılım doğrudan web/mobil istemci üzerinden kullanılır.  

> •

CSC yalnızca sınırlı yapılandırmalar yapabilir. 

Birincil CSC  

> •

Son kullanıcılar. 

Önemli Not : Modern SaaS uygulamaları API ile genişletilebilir, fakat bu onları PaaS yapmaz. 

3.2. PaaS – Hizmet Olarak Platform 

Geliştiricilere uygulama geliştirme ve yayınlama platformu sağlar. Temel altyapı CSP tarafından 

yönetilir. 

Özellikler  

> •

CSC yalnızca uygulamayı geliştirir ve dağıtır.  

> •

Programlama dilleri, kütüphaneler, servisler CSP tarafından sağlanır. 

Birincil CSC  

> •

Geliştiriciler ve uygulama dağıtıcıları. 

Not : PaaS genişletilebilir SaaS’tan farkı: hedef kitlenin geliştirici olmasıdır. 

3.3. IaaS – Hizmet Olarak Altyapı 

Temel işlem, depolama ve ağ kaynakları sağlanır. Kullanıcı işletim sistemi, yazılımlar ve 

uygulamaları kendisi yönetir. 

Birincil CSC  

> •

BT Operasyonları ekipleri. 

Not : IaaS, bulut bilişimin en esnek ama yönetimi en zor seviyesidir. 

Tablo 2: Hizmet Modellerinin Karşılaştırma sı                          

> Özellik SaaS PaaS IaaS
> Kullanıcı Tipi Son kullanıcı Geliştirici / Dağıtıcı BT operasyonları
> Yönetim
> Seviyesi
> Uygulama düzeyi Uygulama + çalışma ortamı OS, uygulamalar, VM'ler
> Kontrol En düşük Orta En yüksek
> Örnek Google Workspace Heroku, Azure App Service AWS EC2, GCP Compute
> Engine
> Avantaj Bakım yok Hızlı geliştirme Esneklik
> Risk Esnekliğin sınırlı
> olması
> Kilitlenme riski (vendor lock -
> in)
> Yönetim karmaşıklığı Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 202 5-202 6Güz Dönemi
> BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi

5

4. Bulut Dağıtım Modelleri 

4.1. Özel Bulut (Private Cloud) 

Tek bir kuruluş tarafından kullanılır. 

Özellikler 

• En yüksek kontrol. 

• Güvenlik ve veri konumu avantajı. 

4.2. Topluluk Bulutu (Community Cloud) 

Benzer güvenlik, politika veya iş ihtiyaçlarına sahip kuruluşlar tarafından ortak kullanılır. 

Özellikler 

• Paylaşılan altyapı. 

• Benzer güvenlik/süreç gereksinimleri. 

4.3. Genel Bulut (Public Cloud) 

Geniş kitlelere açık bulut modelidir (AWS, Azure, GCP gibi). 

4.4. Hibrit Bulut (Hybrid Cloud) 

İki veya daha fazla bulut modelinin veri ve uygulama taşınabilirliği sağlayacak şekilde 

birleştirilmesi. 

Özellikler 

• Çok esnek. 

• Farklı bulutların avantajları bir araya getirilir. 

Tablo 3: Bulut Dağıtım Modelleri nin Karşılaştırılması 

Model  Tanım  Sahiplik  Kullanıcı 

Grubu 

Avantaj  Dezavantaj 

Özel Bulut  Tek kuruluş için 

ayrılmış 

Kurum veya 

üçüncü taraf 

Kurum içi  En yüksek 

güvenlik ve 

kontrol 

Yüksek maliyet 

Topluluk 

Bulutu 

Benzer ihtiyaçları 

olan kuruluşlarca 

ortak 

Kurumlar veya 

üçüncü taraf 

Ortak amaçlı 

grup 

Maliyet avantajı + 

özel bulut 

güvenliği 

Koordinasyon zor 

olabilir 

Genel 

Bulut 

Herkese açık  CSP  Geniş 

kullanıcı 

kitlesi 

Düşük maliyet, 

yüksek esneklik 

Veri konumu 

sınırlı kontrol 

Hibrit 

Bulut 

Birden fazla bulutun 

birleşimi 

Paylaşımlı  Kurumlar  Esneklik, 

optimum maliyet 

Yönetim 

karmaşık Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 202 5-202 6 Güz Dönemi 

> BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi

6

5.  Bulut Hizmeti Modellerinin Analizi 

Bulut hizmetleri, CSP tarafından sağlanan ve bulut bilişimin beş temel özelliğini sergileyen bilgi 

işlem yetenekleridir. NIST Bulut Bilişim Tanımı, üç olası bulut hizmeti kategorisi sağlar :

• Hizmet Olarak Yazılım (SaaS), 

• Hizmet Olarak Platform (PaaS) 

• Hizmet Olarak Altyapı (IaaS )

NIST Bulut Bilişim Referans Mimarisi ile ilgili olarak, bulut hizmetleri, Şekil 1'de gösterilen 

Hizmet Düzenleme yığınının bir parçası olan Hizmet katmanında kullanıma sunulur. 

Hizmet Modelleri, yatay ve dikey bileşenler olarak gösterilmektedir. Bunun nedeni, bulut 

hizmetleri yığında birbirine bağımlı olsa da , hizmetlerin bağımsız olarak uygulanması ve her 

katmanın mimarisine bağlı olarak (gösterildiği gibi) kaynak soyutlama ve kontrol katmanı ile 

doğrudan etkileşime girmesi de mümkün olabilir. (Şekil 1).