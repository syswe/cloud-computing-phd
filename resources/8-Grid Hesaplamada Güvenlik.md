Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 1

1.  Grid Hesaplamada Güvenlik (Security in Grid Computing) 

Grid (Şebeke) güvenliği, ölçeklenebilir sanal organizasyonlar ( virtual organizations - VO'lar) 

oluşturma zorlukları nedeniyle İnternet güvenliğinden ayrılır. 

Sanal Organizasyonlar ( Virtual Vrganizations VO'lar)  

> •

Tanım: Kaynakları ve hizmetleri kendi aralarında paylaşmak için oluşturulmuş, coğrafi 

olarak dağılmış bir grup birey veya kuruluştur. Bu varlıklar kalıcı veya geçici olabilir.  

> •

Paylaşım: Paylaşım, koşullarını ve kapsamını tanımlayan bir dizi kural veya politikaya 

tabidir.  

> •

Zorluk: VO'ların dinamik ve organizasyonlar arası doğası, şebekelerde güvenliğin 

uygulanmasını zorlu hale getirir.  

> •

Kontrol Eksikliği: Şebekelerde merkezi bir kontrol noktası olmaması, her kaynak 

sağlayıcının başka bir hizmet sağlayıcı ile etkileşime geçmeden önce risk değerlendirmesi 

yapması gerektiği anlamına gelir. 

Geleneksel Güvenlik Alanları 

Grid'de güvenliği tanımlamada hayati rol oynayan geleneksel güvenlik alanları şunlardır: 

1.1. Kimlik Doğrulama (Authentication)  

> •

Tanım: Ağdaki bir varlığın kimliğini belirleme sürecidir (kullanıcı, süreç veya kaynak 

olabilir). Belirli bir kimliğe sahip olduğunu iddia eden bir varlığın iddiasını doğrulamanıza 

olanak tanır.  

> •

Basit Araç: Kullanıcı adı ve parola.  

> •

Ağ Kimlik Doğrulaması: Kerberos , simetrik anahtar şifrelemesi kullanarak 

istemci/sunucu uygulamalarına kimlik doğrulama sağlar.  

> •

Grid ’de Önemli Teknoloji: Açık Anahtar Altyapısı (Public Key Infrastructure - PKI) . 

> o

PKI, varlıkları X.509 sertifikalarının kullanımı yoluyla tanımlayan güvenlik 

sistemini açıklar.  

> o

Sertifikalar, sertifika yetkilileri ( Certification Authorities - CA'lar) olarak 

bilinen güvenilir kuruluşlar tarafından verilir.  

> •

Çoklu Kimlik Bilgileri: Bir kullanıcı farklı VO'ların parçası olabileceği için, farklı VO'lar 

üzerinde anlaşmaya varılan farklı CA'ların kullanımı olabilir ve bu nedenle kullanıcılar 

aynı anda farklı kimlik bilgileri kullanabilir. 

1.2. Yetkilendirme (Authorization)  

> •

Tanım: Şebekedeki iki kuruluş arasında güven oluşturmanın ikinci adımıdır. Grid 

tarafından sağlanan bir kaynağa veya hizmete erişmek için bir varlığa atanan ayrıcalıkların Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 2

doğrulanması anlamına gelir. Yalnızca kimlik doğrulama başarıyla gerçekleştirildikten 

sonra yapılır.  

> •

Kaynak Sahibi Yetkisi: Kaynak sahipleri, bir varlığın sanal bir organizasyonun kimliğine 

veya üyeliğine bağlı olarak bir kaynağa erişim verme veya reddetme yeteneğine sahip 

olmalıdır.  

> •

Yetkilendirme Teknikleri:  

> o

Globus Toolkit Gridmap Dosyası: Grid kullanıcılarının seçkin global adlarının 

bir listesini ve eşlendikleri ilgili yerel hesap adlarını içerirdi. Güncellenmesi yerel 

sistem yöneticisi için çaba gerektirirdi.  

> o

Topluluk Yetkilendirme Servisi (Community Authorization Service - CAS): 

Grid yetkilendirmesinin kolaylığını ve yönetilebilirliğini artırır. Bir kaynak sahibi, 

sahip olduğu bir kaynağa sanal kuruluşa sınırlı erişim verebilir. Her VO, güvenilir 

bir aracı görevi gören bir CAS sunucusundan oluşur.  

> o

Sanal Organizasyon Üyelik Hizmeti (Virtual Organization Membership 

Service - VOMS): Avrupa Birliği DataGrid projeleri tarafından geliştirilmiştir.  

> ▪

Birden fazla organizasyonu kapsayan VO'lar içinde yetkilendirme 

bilgilerinin yönetimini sağlar.  

> ▪

Kullanıcı rollerini ve yeteneklerini içeren bir veritabanı ve bunu işlemek 

için araçlar sağlar.  

> ▪

Bu araçlar, standart grid proxy sertifikalarındaki temel kimlik doğrulama 

bilgisine ek olarak VOMS veritabanından alınan rol ve yetenek bilgilerini 

içeren kimlik bilgileri oluşturur. 

1.3. Gizlilik (Confidentiality)  

> •

Tanım: Hassas bilgilerin bunlara erişim hakkı olmayanlardan saklanması anlamına gelir.  

> •

Hassas Veriler: Grid uygulamaları genellikle endüstriyel bilgiler, finansal bilgiler, tıbbi 

veriler gibi hassas veriler üzerinde çalışır.  

> •

Yaklaşım: Kriptografide izlenen en temel gizlilik yaklaşımı veri şifrelemedir . 

> •

Kontrol: Hassas bilgilere erişim dikkatli bir şekilde planlanmalı ve kontrol edilmelidir.  

> •

Kritik Kod Çalıştırma: Grid uygulamaları genellikle uzak bir kaynakta kritik kod 

çalıştırmayı gerektirir. Bu uzak kaynak, yalnızca veri sahibi tarafından güvenilen 

düğümleri içermelidir. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 3

2. Grid Ortamında Güven ve Güvenlik (Trust and Security in a Grid Environment) 

Kaynak paylaşımı, şebeke tanımının temelidir. 

Güven Kavramı  

> •

İlk Kullanım: Grid'in ilk kullanımı, etkileşim halindeki varlıkların birbirini tanıdığı 

bilimsel işbirliklerini desteklemekti. Bu, ortak amaç nedeniyle örtük bir güven ilişkisine 

sahipti.  

> •

Gelişen Kullanım: Artan popülarite ile grid ’ler, bir kaynağın bilinmeyen üçüncü şahıslarla 

paylaşılabileceği iş alanında kullanılmaya başlandı. Bu, kötü niyetli kullanıcılar nedeniyle 

risk içerir.  

> •

Tanım: Güven, hedef varlığa güvenen güvenen (özne) ile güvenilen varlık olan mütevelli 

arasındaki bir ilişki olarak tanımlanabilir.  

> •

Güvenlik Gereksinimleri: Kaynak paylaşımı, ancak dahil olan iki taraf birbirinin 

kimliğini iddia edebildiğinde gerçekleşebilir. Bu, kimlik doğrulama ve ardından 

yetkilendirme kullanılarak yapılır. 

2.1. Mevcut Güvenlik Teknolojileri 

Bu teknolojiler açık standartlara dayalıdır ve şebeke güvenliğinin ayrılmaz bir parçasını oluşturur. 

2.1.1. Açık Anahtar Altyapısı (Public Key Infrastructure - PKI)  

> •

Amaç: Kullanıcılara genel/özel anahtar çiftini kullanarak güvenli olmayan genel ağda 

güvenli iletişim yapmanın bir yolunu sunar.  

> •

Bileşen: Güvenilir bir üçüncü taraf olan Sertifika Yetkilisi (CA) içerir. CA, kullanıcılara 

(birey veya kuruluş) dijital bir sertifika verir.  

> •

Dijital Sertifika: Bir kullanıcıyı benzersiz şekilde tanımlar ve X.509 sistemi tarafından 

belirtilen yapıyı takip eder.  

> o

Sertifikanın genel anahtarı genel kullanıma açıktır.  

> o

Özel anahtar sertifika sahibi ile güvenli bir şekilde saklanır.  

> o

Özel anahtar ile imzalanan bir veri parçasının şifresi yalnızca genel anahtar 

kullanılarak çözülebilir ve tersi de geçerlidir.  

> •

Güven Zinciri (Chain of Trust): PKI, hiyerarşik bir yapı izler.  

> o

En Alt Seviye: Dijital sertifikaya sahip son kullanıcılar.  

> o

Orta Seviye: Bölgesel düzeyde sertifika vermeye yetkili CA'lar (bölge bir kuruluş 

kadar küçük veya bir devlet/ülke kadar büyük olabilir).  

> o

En Üst Seviye: Kök CA'lar (Root CA). Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 4
> o

Kullanıcı, güvendiği bir CA tarafından imzalandığını bulana kadar hiyerarşide 

yukarı çıkarak güven zincirini inceler.  

> Açık Anahtar Altyapısının (PKI) hiyerarşik yapısı
> •

X.509 Dijital Sertifikasının Alanları: 

1.  Sürüm: X.509 dijital sürümünü belirtir (Temel alanlar için 1, benzersiz tanımlayıcı 

mevcutsa 2, uzantılar kullanılıyorsa 3). 

2.  Seri Numarası: Her CA, verdiği sertifikaya benzersiz bir seri numarası atar. CA 

adı ve seri numarası bir sertifikayı benzersiz şekilde tanımlar. 

3.  Algoritma Tanımlayıcı (AlgorithmIdentifier): Sertifikada kullanılan 

algoritmaları tanımlar (örneğin, RSA Şifrelemeli md5). 

4.  Sertifikayı Veren (Issuer): Sertifikayı imzalayan CA'nın adı. 

5.  Geçerlilik (Validity): Sertifikanın geçerli olduğu süreyi belirten iki alan ("önce 

geçerli değil" ve "sonra geçerli değil"). 

6.  Konu (Subject): Sertifikaya sahip olan kuruluş veya kişinin adı. 

7.  Konu Açık Anahtar Bilgisi (SubjectPublicKeyInfo): "genel/özel anahtar çiftini" 

oluşturmak için kullanılan algoritmayı ve sertifika sahibinin ortak anahtarını içerir. 

8.  Sertifikayı Verenin Benzersiz Kimliği (IssuerUniqueId): Sertifikayı veren (CA) 

için benzersiz bir kimlik belirten isteğe bağlı alan. 

9.  Konu Benzersiz Kimliği (SubjectUniqueId): Sertifika sahibi için benzersiz bir 

kimlik belirten isteğe bağlı alan. 

10.  Uzantılar (Extensions): Temel alanlara uzantılar içerebilen isteğe bağlı alan. 

11.  Sertifika İmzası (CertificateSignature): CA'nın özel anahtarı tarafından 

imzalanmış tüm sertifikanın (imza alanı hariç) Hash değeri (hash) oluşur. Hash 

fonksiyonu temel olarak verinin bütünlüğünü sağlamak için kullanılan bir 

yöntemdir. Hash alınmış veri geri döndürülmeyecek şekilde karşı tarafa gönderilir. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 5
> ▪

Bir sertifikanın gerçekliğini doğrulamak için, kullanıcı tüm alanın Hash 

fonksiyonu nu hesaplayıp , bu değeri CA'nın ortak anahtarını kullanarak 

imzalanan Hash değeri ile karşılaştırır.  

> •

Kullanım Alanları:  

> o

Güvenli Giriş Katmanında (Secure Socket Layer - SSL) kullanılır.  

> o

Şebeke Güvenlik Altyapısındaki (Grid Security Infrastructure - GSI) kimlik 

doğrulama mekanizmalarının temelini oluşturur. 

X.509 Authentication Service:  https://www.geeksforgeeks.org/computer -networks/x -509 -

authentication -service/ 

2.1.2. Kerberos  

> •

Tanım: MIT tarafından geliştirilen bir ağ kimlik doğrulama protokolüdür.  

> •

Amaç: Simetrik anahtar şifrelemesi kullanarak istemci ve sunucuya karşılıklı kimlik 

doğrulama sağlar.  

> •

Simetrik Anahtar Şifrelemesi: Mesajın hem şifrelenmesi hem de şifresinin çözülmesi 

için aynı anahtarın kullanılmasıdır.  

> •

Temel Taraflar: Kerberos kimlik doğrulama işlemi üç taraf içerir: 

1.  İstemci (Client) 

2.  Sunucu (Server) 

3.  Anahtar Dağıtım Merkezi (Key Distribution Center - KDC): Güvenilir bir 

aracıdır.  

> •

Kerberos Terimleri:  

> o

Principal (Müdür -Güvenlik Sorumlusu): Kimliği doğrulanmakta olan 

kuruluştur.  

> o

Verifier (Doğrulayıcı): Müdürün kimliğini doğrulayan varlıktır.  

> o

Kerberos Realm (Kerberos Bölgesi): Kerberos'un çalıştığı bir yönetim alanıdır, 

genellikle büyük harflerle yazılmış organizasyonun İnternet Alan Adından oluşur.  

> o

Security Principals (Güvenlik İlkeleri): Kerberos bölgesi tarafından tanınan 

varlıklar (kullanıcı veya kullanıcı adına çalışan bir süreç).  

> •

KDC Bileşenleri: KDC, iki varlığa bölünmüştür: 

1.  Kimlik Doğrulama Sunucusu (Authentication Server - AS): Güvenlik 

sorumluları ve TGS ile uzun vadeli bir gizli anahtar (ana anahtar) paylaşır. İstemci 

tarafından TGS'ye kimlik doğrulaması yapmak için kullanılan Bilet Verme Biletini 

(Ticket Granting Ticket - TGT) düzenler. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 6

2.  Bilet Verme Sunucusu (Ticket Granting Server - TGS): Sunucuda kimlik 

doğrulaması yapmak isteyen istemcilere, TGT'yi kullanarak, erişim için normal 

Bilet sağlamak için güvenilir bir üçüncü taraftır.  

> •

Özellikler:  

> o

Geleneksel kimlik doğrulama protokollerine göre daha güvenli ve uygundur.  

> o

İlk kimlik doğrulama için gereken ileti sayısını azaltmak için zaman damgaları 

kullanılır.  

> o

Bilet verme hizmeti , parolanın yeniden girilmesini gerektirmeyen sonraki kimlik 

doğrulamayı kolaylaştırır (Tekli Oturum Açma).  

> o

Bölgeler arası kimlik doğrulaması desteği sağlar. 

2.1.3. Şebeke Güvenlik Altyapısı (Grid Security Infrastructure - GSI)  

> •

Tanım: Şebekelerde güvenliğin uygulanması için gerekli işlevleri sağlayan eksiksiz 

mimariyi tanımlar.  

> •

Özel Güvenlik İhtiyaçları: GSI, Grid'in özel güvenlik ihtiyaçlarını karşılamak için 

geliştirilmiştir: 

1.  Tek Oturum Açma (Single Sign -On): Kullanıcı bir kez kimlik doğrulamasından 

sonra, tekrar kimlik doğrulaması gerektirmeden kaynaklara erişebilir. İlk kimlik 

doğrulamada oluşturulan Proxy Sertifikası bu amaçla kullanılır. 

2.  Ayrıcalıkların Devredilmesi (Delegation of Privileges): Bir varlığın (X) 

ayrıcalıklarının bir kısmını başka bir varlığa (Y) devrederek, Y'nin X adına kısıtlı 

bir görevi (örneğin Z üzerindeki bir kaynağa erişim) gerçekleştirmesini 

sağlamaktır.  

> ▪

Bu, proxy sertifikası verilerek yapılır.  

> ▪

Proxy sertifikası ve özel anahtarı, proxy kimlik bilgisi olarak adlandırılır. 

3.  Etki Alanları Arası Güvenlik Desteği (Inter -domain security support): Farklı 

yerel güvenlik politikaları izleyebilen birden çok kuruluşu kapsayan Grid'lerde 

varlıklar arası etkileşim için destek sağlamalıdır. 

4.  Güvenli İletişim (Secure Communication): Taşıma Katmanı Güvenliği 

(Transport Layer Security - TLS) kullanarak güvenli mesaj alışverişi desteği 

sağlar. 

5.  Kimlik Doğrulama ve Yetkilendirme (Authentication & Authorization): 

Güvenli ve ölçeklenebilir kimlik doğrulama ve yetkilendirme sağlamalıdır. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 7

6.  Tek Tip Kimlik Bilgileri (Uniform credentials): Etki alanları arası etkileşim 

gerektirdiğinden, kimlik bilgilerini temsil etmenin tek tip bir yolu olmalıdır. GSI, 

bunun için X.509 sertifika biçimini kullanır. 

2.2. Gelişen Güvenlik Teknolojileri 

2.2.1. Web Hizmetleri Güvenliği (WS -Security)  

> •

Tanım: SOAP (Simple Object Access Protocol) mesajlarına bütünlük, gizlilik ve tek mesaj 

kimlik doğrulaması gibi güvenlik özellikleri sağlayan standarttır.  

> •

Amaç: Taşıma düzeyinden (SSL gibi) ziyade, ileti düzeyinde güvenlik elde etmek için 

geliştirilmiştir.  

> •

Özellik: SOAP mesajları, temel taşıma protokolünden bağımsız olarak güvence altına 

alınabilir. Güvenli web hizmetleri oluşturmak için SOAP mesajlarına bir uzantı sağlar.  

> •

Esneklik: PKI, Kerberos ve SSL dahil olmak üzere çok çeşitli güvenlik protokolleriyle 

çalışacak şekilde tasarlanmıştır. 

2.2.2. OGSA Güvenliği  

> •

OGSA: Açık Şebeke Hizmetleri Mimarisi ( Open Grid Services Architecture ) anlamına 

gelir. Web servislerine dayalı bir Grid mimarisi tanımlar.  

> •

Amaç: Grid sistemleri ve web servislerinin birleşimi olarak, kaynak yönetimi, güvenlik 

yönetimi ve iş yönetimi gibi Grid hizmetlerini standart bir arayüz sağlayarak standart hale 

getirmektir.  

> •

Temeller: Globus Toolkit ve web hizmetleri kullanılarak oluşturulmuştur.  

> o

Globus Toolkit bileşenleri: GRAM, Ağ Geçidi Bekçisi Hizmeti, Meta Dizin 

Hizmeti (MDS), ve Izgara Güvenlik Altyapısı (GSI) . 

> •

Grid (Şebeke) Hizmetleri: OGSA'nın tanıttığı yeni terimdir. Grid tabanlı uygulamalara 

uygun hale getirmek için uzantıları olan bir web hizmetidir.  

> o

Durum (State): Web hizmetleri durumsuzken (stateless ), Grid hizmetleri durum 

yönetimi ve yaşam döngüsü yönetimi için destek sağlar.  

> o

Hizmet Verileri (Service Data): Web servisinde bulunmayan, WSDL arayüzüne 

yapılandırılmış veriler eklemeye olanak tanıyan önemli bir özelliktir.  

> o

Kimlik Belirleyiciler:  

> ▪

Grid Service Handle (GSH): Bir Grid hizmeti örneğini diğerinden ayırt 

etmek için kullanılır. Değeri oluşturulduktan sonra değişmez.  

> ▪

Grid Service Reference (GSR): Protokol bağlama, yöntem tanımı ve ağ 

adresi gibi örneğe özgü bilgileri tutar. Değeri kullanım ömrü boyunca 

değişebilir. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 8
> •

Çoklu Protokol Bağlama: Web hizmeti tanımlama dili (WSDL), hizmet çağırma için 

kullanılan temel protokolden bağımsız olarak hizmet arabirimlerinin tanımı için kullanılır. 

Bu, istemci ve sağlayıcının aynı veya farklı makinelerde olmasına olanak tanır.  

> •

Hizmet Keşfi ve Güncelleme: OGSA, mevcut hizmetlerin keşfi ve istemcinin hizmet 

tanımı hakkındaki bilgilerini güncellemesine olanak tanıyan işlevsellik sağlar (örneğin, 

desteklenen işlemler ve protokol bağlamaları).