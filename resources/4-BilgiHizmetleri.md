Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 1

1. Bilgi Hizmetleri (Information Services) 

Bilgi Hizmetleri, aynı zamanda İzleme ve Keşif Hizmetleri (Monitoring and Discovery Services 

- MDS) olarak da bilinir . MDS'nin temel amacı, bir hesaplama Şebekesi (Grid) tarafından sağlanan 

yetenekler ve hizmetler hakkında genel bir bakış elde etmek için kaynak keşfi, seçimi ve 

optimizasyonu için bilgi sağlamaktır . Bu hizmetler, uygulamalar veya sanal kuruluşlar (VO) 

tarafından kullanılabilir .

Globus, bu hizmetleri iki ana kategoriye ayırmıştır : 

> •

WS Öncesi Bilgi Hizmetleri (MDS2)  

> •

WS Bilgi Hizmetleri (MDS3) 

1.1. WS Bilgi Hizmetleri (MDS3) 

MDS3, bir dizi şebeke hizmeti olarak uygulanmıştır . Bu şebeke hizmetleri, kendilerini oluşturan 

süreçten daha uzun ömürlü iseler "kalıcı" (persistent), aksi takdirde "geçici" (transient) olarak iki 

gruba ayrılır . Hizmetler durumlarını Hizmet Veri Öğeleri (Service Data Elements - SDE) 

aracılığıyla ifade ederler .

1.1.1. Bilgi Modeli (Information Model) 

MDS tarafından kullanılan model, Open Grid Services Architecture (OGSA) tarafından 

sağlanan mekanizmalara dayanmaktadır . Bu mekanizmalar şunlardır:  

> •

Factories: Hizmet örnekleri (instances) oluşturan nesnelerdir . 

> •

Grid Service Handle (GSH): Bir hizmet için benzersiz bir tanımlayıcıdır . Bir hizmetin 

kullanılabilmesi için GSH'nin bir GSR'ye dönüştürülmesi gerekir . 

> •

Grid Service Reference (GSR): GSH'yi ve taşıma protokolü ile veri kodlama formatı gibi 

bağlama bilgilerini içerir . 

> •

Registry Services: GSH'ler için bir depodur . Hizmetler, keşfedilebilmek için GSH'lerini 

buraya kaydedebilir . 

> •

Notification Services: İstemci aboneliği aracılığıyla servisler arasında asenkron mesajlar 

göndermek için kullanılır .

1.1.2. Veri Toplama (Data Collection) 

Kaynak bilgileri, hizmet veri sağlayıcıları aracılığıyla toplanır . Bu sağlayıcılar, hizmet verilerini 

dinamik olarak üreten harici programlardır . Bazı sağlayıcılar Globus Toolkit'in temel bir 

parçasıyken, geliştiriciler tarafından özel sağlayıcılar da uygulanabilir .

1.1.3. Bir Araya Getirme ve Toplama (Aggregation) 

Sağlayıcılar tarafından oluşturulan veya diğer şebeke hizmetlerinden gelen veriler, farklı toplu veri 

görünümlerinde sunulabilir . Bu verilere daha sonra bildirim veya abonelik mekanizmaları 

aracılığıyla komut satırı veya GUI istemcileri tarafından erişilebilir .Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 2

1.1.4. Sorgular (Queries) 

MDS3, hizmet veri öğelerine erişim için standart ve genişletilebilir bir sorgu arayüzü sunar .

Sorgular, SDE adıyla veya XPath ve XQuery gibi daha karmaşık diller kullanılarak yürütülebilir . 

> •

İstemci Aboneliği: İstemciler, belirli hizmet veri öğelerine veya isteğe bağlı değerlere 

bağlı mesajları almak üzere dizin hizmetlerine abone olabilirler . Abonelikler, bildirim 

mesajlarının eşzamansız olarak teslimini sağlayan NotificationSource arayüzü ile yönetilir . 

> •

Sorgu Modları: Sorgular, basit eşzamanlı bir çekme modunda ( FindServiceData ) veya 

eşzamansız bir yanıt (bildirim aboneliği) modunda yürütülebilir .

Dizin Hizmetleri, veri toplama ve hizmet grubu gibi bileşenleri birleştirerek Sanal Organizasyonlar 

(VO) oluşturmak için farklı topolojilerde bir araya getirilebilir .

1.1.5. Kullanıcı Arayüzleri (User Interfaces) 

Globus Toolkit (GT), Bilgi Servislerini sorgulamak için iki tür kullanıcı arayüzü sağlar :

1.  Servis Tarayıcı GUI'si: Grafiksel bir arayüz sunar (Bkz. Şekil 1) .

2.  Komut Satırı Araçları: ogsi -find -service -data -by -name ve ogsi -find -service -data -xpath 

gibi araçlar sunar .

Şekil 1: Bir sorgu gösteren Hizmet Veri Tarayıcısı sistem bilgisi veri sağlayıcısı .

Şekil 2: Komut satırı sorgulama aracı .Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 

202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi 

3

1.1.6. Güvenlik (Security) 

Dizin hizmeti, Grid Security Infrastructure (GSI) ile uyumludur . GSI, X.509 ve proxy 

sertifikaları gibi açık standartlara dayanan tek bir oturum açma kimlik doğrulama hizmeti sunar .

GSI, hem mesaj düzeyinde hem de aktarım düzeyinde güvenlik uygular ve SSL/TLS üzerinde 

çalışır . Karşılıklı kimlik doğrulama, kimlik bilgisi delegasyonu ve yetkilendirme gibi protokolleri 

tanımlar . Ancak, varsayılan olarak dizin hizmetlerinde güvenlik etkinleştirilmemiştir .

1.1.7. MDS3 Veri Sağlayıcıları (Data Providers) 

Çekirdek veri sağlayıcıları, İşletim Sistemi Türü, CPU sayısı ve RAM miktarı gibi temel kaynak 

bilgilerini sağlar . Ayrıca basit komut dosyası yürütme yetenekleri de sunarlar .

Tablo 1: GT3'teki Temel Veri Sağlayıcılar          

> Sağlayıcı Adı (Provider Name )Tanımı
> SimpleSystemInformationProvider Ana bilgisayar hakkında bilgi sağlar: CPU, bellek, işletim sistemi ve disk birimleri
> HostScriptProvider Ana bilgisayar kaynak bilgilerini sağlamak için bir dizi Unix kabuk komut dosyası sağlar
> ScriptExecutionProvider Kabuk komut dosyalarını yürütmek için bir sağlayıcı
> AsyncDocumentProvider Bir XML'i periyodik olarak okumak için zaman uyumsuz bir yardımcı program; AsyncDataProvider
> arabirimini uygular.

Sağlayıcı Arayüzleri Geliştiriciler, SimpleDataProvider gibi arayüzleri kullanarak özel bilgi 

sağlayıcıları oluşturabilir . Bu temel arayüz, tüm sağlayıcıların uygulaması gereken ve XML 

formatında çıktı üreten metodları tanımlar .

SimpleDataProvider: Bu, tüm sağlayıcıların uygulaması gereken temel arabirimdir. XML 

formatında çıktı üretir. Bu arayüz aşağıdaki yöntemleri tanımlar: 

// Sağlayıcının görünen adını döndürür. 

String getName(); 

// Sağlayıcının işlevselliğinin bir açıklamasını döndürür. 

String getDescription(); 

// Sağlayıcının bir dizi varsayılan argümanı varsa, 

// bu fonksiyonla alınabilirler. 

String getDefaultArgs(); 

// Sağlayıcı bir dize temsili döndürmelidir 

// varsa mevcut hatanın. 

String getErrorString(); 

// Sağlayıcının sırayla yürütülmesini tetikler 

// sağlayıcının dahili durumunu güncellemek için, 

// çıktıyı belirtilen OutputStream'e gönderiyoruz. 

void run(String args, java.io.OutputStream outStream); Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 4

1.2. WS Öncesi Bilgi Hizmetleri (MDS2) 

MDS2, Globus Toolkit Sürüm 2 ve öncesi sürümlerin bilgi hizmetleri bileşenidir ve geriye dönük 

uyumluluk için korunmaktadır . MDS2, şebeke kaynakları hakkında bilgi toplamak için Grid 

Resource Information Service (GRIS) ve Grid Index Information Service (GIIS) bileşenlerini 

kullanır . Temel arayüz olarak LDAP (Lightweight Directory Access Protocol) kullanmasıyla 

MDS3'ten ayrılır .

MDS'nin faydaları şunları içerir : 

> •

Sistem bileşenleri hakkında statik ve dinamik bilgilere erişim . 

> •

Bilgiye tek tip ve esnek erişim . 

> •

Birden fazla bilgi kaynağına erişim . 

> •

Merkezi olmayan bakım .

1.2.1. Mimari: GRIS ve GIIS  

> •

GRIS (Grid Resource Information Service): Belirli bir kaynaktaki konfigürasyon, 

yetenek ve durum gibi bilgileri sorgulamak için kullanılır . Örneğin, bir ana bilgisayarın 

işletim sistemi, CPU ve bellek kullanılabilirliği gibi bilgileri sağlayabilir . 

> •

GIIS (Grid Index Information Service): Farklı GRIS hizmetlerinden gelen bilgileri 

birleştirerek şebeke genelinde keşif ve arama yetenekleri sunar . Bu, bir Sanal Organizasyon 

(VO) içindeki hesaplama, depolama ve ağ kaynaklarının tutarlı bir görünümünü sağlar .

Şekil 3: Bir VO içindeki Bilgi Hizmetleri modeli .

1.2.2. LDAP Yapılandırması 

MDS2, kaynak bilgilerini yayınlamak için LDAP tabanlı bir yapılandırma kullanır . Geliştiriciler, 

özel sağlayıcılar için özel LDAP şemaları oluşturabilirler . Bu şemalar, yayınlanacak her bir 

öznitelik için bir nesne kimliği (OID) içermelidir ve kayıtlı bir formatı izlemelidir .Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 5

1.3. Grid Monitor Örneği 

Grid Monitor, şebeke kaynaklarının durumunu izlemek için kullanılan bir araçtır. Şekil 4'te

görülen arayüz, tıklanabilir nesneler aracılığıyla detaylı bilgi sunar .

Şekil 4: Grid Monitor .

Arayüzdeki temel bileşenler şunlardır: 

1.  Küme (Cluster): Tıklandığında, kümenin mevcut durumu hakkında tam bilgi veren 

açıklama modülüne yönlendirir .

2.  Yük (Load): Kümedeki Şebekeli (Grid) ve yerel olarak gönderilen işlemleri grafiksel 

olarak gösterir . Renkli çubuk Grid işlemlerini, gri çubuk ise toplam doluluğu temsil eder .

3.  Kuyruklama (Queuing): Hem yerel kaynak yönetim sisteminde ( Local Ressource 

Management System -LRMS) hem de Grid Manager tarafından işlenen kuyruktaki iş 

sayısını gösterir .

4.  Arama (Search): Kullanıcıların standart dışı izleme istekleri oluşturmasına olanak tanıyan 

özel arama arayüzüne bağlanır .

5.  Depolama Kaynakları (Storage resources): Kullanılabilir depolama kaynaklarının 

listesine bağlantı sağlar .