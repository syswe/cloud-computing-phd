Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and 

> Cloud Computing) Dersi

1

1. Veri Yönetimi (Data Management) 

Şebeke ortamlarındaki veri yönetiminin, şebekelerin (Grids) kendi içinde Grid hesaplama (Grid Computing) 

ve veri şebekelerine (data grids) ayrılması nedeniyle çifte bir önemi bulunmaktadır . Daha dar bir tanıma 

göre veri yönetimi, uzak siteler arasında dağıtılmış verilerin erişimini, senkronizasyonunu ve 

koordinasyonunu destekleyen bir dağıtılmış veri yönetim sistemidir . 

> •

Hesaplama Odaklı Tanım: Bu yaklaşımda, veri yönetimi daha az önemli bir sorun olarak görülür . Bunun 

nedeni, bilgi işlem uygulamalarının kullandığı verilerin küçük dosyalara bölünebilmesi ve daha az veri 

iletimi gerektirmesidir . Sıkça kullanılan bir yöntem, girdi verilerini çalıştırılacak programla birlikte 

hesaplamanın yapılacağı düğüme göndermektir . 

> •

Veri Odaklı Tanım: Bu tanımda veri ızgarası (data grid), çok büyük miktarda dağıtılmış verinin 

işlenmesine odaklanır . Veri yoğun hesaplama, büyük veri depolama ve hızlı veri analizi gibi süreçleri 

içeren tipik bir veri ızgarası uygulamasıdır . Geleneksel bir veritabanı sunucusu, büyük miktarda veri 

üreten veri yoğun bir uygulamada, sınırlı işlem kapasitesi nedeniyle bir darboğaza dönüşebilir . Çözüm 

olarak veri ızgarası, üretilen veriyi dağınık sitelere dağıtarak ve kaynakların kapasitesini kullanarak bir iş 

yükü dengesi sağla r. CERN'in başlattığı DataGrid projesi, Büyük Hadron Çarpıştırıcısı'ndan (LHC) çıkan 

devasa verileri işlemek amacıyla geliştirilmiş en ünlü veri ağı araştırma projelerinden biridir .

Veri Izgarası (Data Grid) vs. Dağıtılmış Veri Tabanı Yönetim Sistemi (DDBMS) 

Bu iki sistem benzer ortamlarda kullanılsa da aralarında temel farklar bulunmaktadır . 

> •

Heterojenlik: Veri ızgarası tamamen heterojendir . Farklı veri temsilleri ve depolama yöntemleri gibi 

sorunlarla karşılaşır . DDBMS ise genellikle homojen veri kaynaklarına sahiptir . 

> •

Veri Kontrolü: DDBMS, ekleme, silme ve güncelleme gibi atomik işlemlerle veriler üzerinde tam 

kontrole sahiptir ve veri tutarlılığını sağlar . Veri ızgarası ise veri kaynakları üzerinde yalnızca kısmi bir 

kontrol sağlayabilir; bir veri, bir kullanıcı tarafından okunurken başka bir kullanıcı tarafından yazılabilir . 

> •

Ölçeklenebilirlik: Bir veri ızgarasının veri kaynakları, DDBMS'ye göre çok daha büyüktür . Bu nedenle 

veri ızgarası, yeni veri kaynaklarının kolayca eklenebilmesini ifade eden ölçeklenebilirliği dikkate almak 

zorundadır .

2. Veri Yönetiminin Gereksinimleri (Data Management Requirements) 

Şebekelerdeki veriler coğrafi olarak dağınık ve heterojen bir yapıdadır . Bu nedenle, ilişkisel 

veritabanlarındaki geleneksel ekleme, silme ve güncelleme gibi yöntemler bu ortamlar için uygun değildir .

2.1. Statik ve Dinamik Veri (Static and Dynamic Data) 

Veri ızgaraları temelde iki tür veriyle ilgilenir . 

> •

Statik Veri: Oluşturulduktan sonra asla değiştirilmeyen, sadece okunmak veya analiz edilmek için 

kullanılan verilerdir . Örneğin, bilim insanları tarafından yalnızca alınacak veya karşılaştırılacak olan DNA 

bilgileri statik verilere bir örnektir . Statik verilerle ilgili işlemler nispeten basittir ve genellikle verilere 

nasıl erişileceği, verilerin belirli bir düğüme nasıl taşınacağı ve verilerin nasıl verimli bir şekilde 

aktarılacağı gibi konulara odaklanır .Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and 

> Cloud Computing) Dersi

2 

> •

Dinamik Veri: Dinamik güncellemeler ve değişiklikler içeren verilerdir . Kurumsal düzeydeki e -iş 

uygulamalarındaki veriler bu kategoriye girer . Bir iş akışında her adımın mevcut veriyi değiştirme 

potansiyeli bulunur . Bu durum, güncellemeleri, işlemlerin senkronizasyonunu ve harici sistemlerle 

entegrasyonu içerebilir .

Şebeke üzerindeki hesaplamalar karmaşıklaştıkça, veriler statikten dinamiğe doğru kayar; uygulamalar 

verileri sadece okumakla kalmaz, aynı zamanda yazarlar . Verilerin sürekli değiştiği bu ortamda, farklı 

sitelerdeki kopyalar (replikalar) arasındaki senkronizasyonun sağlanması önemli bir sorundur . Ayrıca, 

veriler heterojen sistemlerde depolandığından, bu kaynaklara birleşik erişim sağlanması ve farklı 

depolama sitelerinden (veritabanı sunucuları, dosya sistemleri vb.) gelen verilerin entegrasyonu kritik 

öneme sahiptir .

3. Veri Yönetiminin İşlevleri (Functionalities of Data Management) 

3.1. Veri Çoğaltma Yönetimi (Data Replication Management) 

Veri çoğaltma, veri erişimini optimize etmek amacıyla veri ızgaralarına dahil edilmiş bir yöntemdir . Veri 

kopyaları (replikalar) bir tür veri önbelleği olarak düşünülebilir . Verilerin aynı kopyaları oluşturulup 

çeşitli depolama sitelerine dağıtılır . Bu sayede kullanıcılar veya uygulamalar, orijinal veriyi arayıp 

aktarmak yerine kendilerine en yakın kopyaya erişerek veri erişim gecikmesini azaltırlar .

Bir çoğaltma yönetim hizmetinin (Replication Management Service - RMS) sorumlulukları şunlardır : 

> •

Bir veri kümesinin tamamı veya bir parçası için çoğaltma oluşturmak . 

> •

Replika dosyalarını ekleme, silme ve değiştirme gibi işlemleri yönetmek . 

> •

RMS'ye yeni bir kopya kaydetmek . 

> •

Kullanıcıların sorgulayabilmesi için kayıtlı replikaları kataloglamak . 

> •

Kullanıcı gereksinimlerine göre en uygun kopyayı seçmek . 

> •

Aynı veri kümesinden gelen kopyalar arasında tutarlılığı otomatik olarak sağlamak ve orijinal veri kümesi 

değiştirildiğinde kopyaları güncellemek .

3.2. Meta Veri Yönetimi (Metadata Management) 

Meta veri, verilerle ilgili tanımlayıcı bilgidir . Bir verinin nasıl ve hangi bilimsel araçla oluşturulduğu, boyutu, 

konumu, erişim yetkisi ve sahipleri gibi köken bilgilerini kaydeder . Meta veriler üç ana başlıkta 

toplanabilir : 

> •

Sistem Bilgileri: Veri şebekesinin kendisiyle ilgili yapısal bilgilerdir; örneğin, internet hizmet durumu, 

depolama kapasitesi ve kullanım politikası gibi verileri içerir . 

> •

Çoğaltma Bilgisi: Mantıksal bir dosya ile bu dosyanın fiziksel kopyaları arasındaki eşleştirme ilişkisini 

kaydeder . 

> •

Uygulama Bilgileri: Veri içeriği, yapısı ve verinin elde edildiği koşullar gibi bir uygulama topluluğu 

tarafından özel olarak tanımlanmış veri niteliklerini kaydeder .

Meta veri, grid ortamlarında verilerin bulunması, erişilmesi ve yönetilmesi için kritik öneme sahiptir .Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and 

> Cloud Computing) Dersi

3

3.3. Yayın ve Keşif (Publication and Discovery) 

Bu işlev, meta veri hizmetinin iki temel rolü olarak tanımlanır ve bu hizmete dayanır . 

> •

Veri Yayınlama: Veri araştırmasını hızlandırmak ve verinin ilgili niteliklerini kullanıcı için erişilebilir 

kılma sürecidir . Bu süreç, bazen meta veri bilgilerini veri kümesiyle birleştirerek veri keşif hizmetine 

sunar . 

> •

Veri Keşfi: Meta veri hizmetleri tarafından yayınlanan nitelik bilgilerini kullanarak istenen veriyi bulma 

sürecidir . Keşif başarılı olduğunda, hizmet kullanıcının orijinal veri kaydına veya bir kopyasına erişimini 

sağlar . Bazı keşif hizmetleri, kullanıcıya verilerin istatistiksel bir görünümünü sunmak için veri kaynağı 

içeriğini şema olarak görüntüleyebilir .

3.4. Veri Senkronizasyonu (Data Synchronization) 

Statik ortamlarda replikalar salt okunurdur ve dosyalar sadece bir siteden diğerine kopyalandığı için 

senkronizasyon sorunu yaşanmaz . Ancak çoğu grid ortamında veriler kullanıcılar veya uygulamalar 

tarafından değiştirilir . Her kopyanın birbiriyle %100 tutarlı olması ideal olsa da, bu pratik değildir ve 

bazen kullanıcılar tarafından istenmez . Bu nedenle farklı tutarlılık düzeyleri tanımlanmıştır : 

> •

Düzey -1: Muhtemel Tutarsız Kopya (Possibly Inconsistent Copy): En düşük tutarlılık düzeyidir .

Kopya, dosya üzerinde birden çok yazma işlemi devam ederken oluşturulur ve ortaya çıkan dosya, orijinal 

dosyanın herhangi bir andaki durumuyla eşleşmez . 

> •

Düzey 0: Tutarlı Dosya Kopyası (Consistent File Copy): Bu düzeyde, dosyanın içeriği belirli bir 

zamanda orijinal dosyanın anlık görüntüsüyle eşleşebilir . Kopyalanan dosyaya bir okuma kilidi eklenerek 

bu seviye sağlanabilir . 

> •

Düzey 1: Tutarlı İşlem Kopyası (Consistent Transactional Copy): Kopya, devam eden hiçbir yazma 

işleminin olmadığı bir anda üretilir . Bu, tek bir dosyada tutarlılığı garanti eder, ancak birbiriyle ilişkili 

birden fazla dosya söz konusu olduğunda aralarındaki tutarsızlığı garanti edemez . 

> •

Düzey 2: Tutarlı İşlem Kopyaları Seti (Consistent Set of Transactional Copies): Bu düzey, birbiriyle 

ilişkili dosyaların kopyaları aynı işlemde üretilirse, bir site içindeki birden çok kopya arasındaki tutarlılığı 

sağlar . Ancak, farklı bir sitedeki orijinal dosyanın kopyasının güncel olduğunu garanti etmez . 

> •

Düzey 3: Tutarlı Güncel İşlem Kopyaları Seti (Consistent Set of Up -to -Date Transactional Copies): 

En katı tutarlılık düzeyidir . Izgaradaki her bir kopya birbiriyle aynı tutulur . Bu seviyeye ulaşmak zordur 

çünkü tüm operasyonel isteklerin tek bir arayüzden gönderilmesini ve şebeke dışı erişime izin 

verilmemesini gerektirir .

3.5. Kimlik Doğrulama, Erişim Kontrolü ve Hesap Oluşturma (Authentication, Access Control, and 

Accounting) 

Grid ortamlarında bilgi işlem kaynakları gibi veri kaynaklarının da korunması gerekir . Grid Security 

Infrastructure (GSI) tabanlı çözümler, kullanıcının kimlik bilgilerini imzalayarak yetkilendirme yapar ve 

kaynaklara erişim izni verir . Veri yönetimi, düşük seviyeli (örneğin bir tablodan kayıt silme) ve yüksek 

seviyeli (örneğin çok siteli bir işlemi yürütme) erişimler için çok parçalı bir erişim kontrol mekanizmasını 

desteklemelidir . Kontrol kararları, hem küresel hem de yerel politika ve kuralları dikkate alır . Bir kaynak 

sağlayıcısı da hangi kullanıcının hangi haklara sahip olacağına karar verebilir . Bir muhasebe mekanizması Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and 

> Cloud Computing) Dersi

4

ise kullanım süresi, sıklığı gibi kaynak kullanım geçmişini kaydederek kaynak kullanım oranını 

hesaplamak ve gelecekteki kullanımı tahmin etmek için kullanılır . Bu bilgiler aynı zamanda veri 

kopyalarının nereye yerleştirileceğine karar vermede de yardımcı olur .

3.6. Veri Entegrasyonu (Data Integration) 

Veri entegrasyonu, farklı kaynaklardan gelen verileri birleştirerek kullanıcıya tek tip bir görünüm sunmayı 

amaçlar . Bu süreç temel olarak şu adımlardan oluşur :

1.  Veri Keşfi: Meta veri hizmetinden ilgili verileri bulmasını istemek .

2.  Veri Erişimi: Bulunan verilerin kullanılabilirliğini ve sorun için yararlı olup olmadığını doğrulamak .

3.  Veri Aktarımı: Yararlı verileri işlenmek üzere yerel ana bilgisayara aktarmak .

4.  Veri Analizi: Yerel ve uzak veriler arasında bir kombinasyon yapılıp yapılmayacağına karar vermek . Bu 

analiz, heterojen kaynaklar arasındaki anlamsal çelişkileri çözmeye odaklanabilir .

5.  Veri Sentezi: Verilerin bir bölümünü dönüştürüp mevcut verilerle birleştirerek yeni bir görünüm 

oluşturma sürecidir . Bu işlem, kullanıcıların eski verilerden yeni bilgiler elde etmesini sağlar .

4. Şebeke Hesaplamada Meta Veri Hizmeti (Metadata Service in Grids) 

Meta veriler, veriyi tanımlayan verilerdir . Bir kütüphanedeki kitap kayıtları eski bir meta veri örneğidir . Kitap 

adı, yazar, anahtar kelimeler gibi bilgiler okuyucuların istedikleri kitabı bulmalarını sağlar; bu bilgiler bir 

tür meta veridir .

Grid ortamlarında meta veriye ihtiyaç duyulmasının nedenleri şunlardır : 

> •

Veri Miktarı: Geleneksel veri araştırma teknikleri (örneğin SQL sorgusu) bu kadar büyük miktarda veriyi 

işleyemez . 

> •

Heterojenlik: Gridlerdeki veriler depolama formatı, veri gösterimi ve kontrol edilme biçimleri açısından 

farklılık gösterir, bu da doğrudan veri keşfini zorlaştırır . 

> •

Ek Açıklamalar: Bilim insanları tarafından verilere eklenen açıklamaların düzenlenmesi ve veri 

sorgularına yardımcı olması gerekir .

4.1. Meta Veri Türleri (Metadata Types) 

Meta veriler çeşitli kategorilere ayrılabilir : 

> •

Veri Meta Verileri (Data Metadata): Verilerin kendisi hakkındaki bilgilerdir ve en önemlileri olarak 

kabul edilir . 

> o

Fiziksel Meta Veriler: Bir veri dosyasının boyutu, konumu, oluşturma zamanı ve dosya türü gibi 

fiziksel özelliklerini tanımlar . 

> o

Çoğaltma Meta Verileri: Mantıksal bir veri dosyası ile onun fiziksel kopyaları arasındaki 

bağlantıyı kurar . 

> o

Etki Alanı Meta Verileri: Veriyi üreten alana özgü veri niteliklerini ve veri öğeleri arasındaki 

ilişkileri (örneğin hiyerarşik sınıflandırma) tanımlar .Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and 

> Cloud Computing) Dersi

5 

> •

Kullanıcı Meta Verileri (User Metadata): Verileri oluşturan, kullanan veya değiştiren kişilerle ilgili 

bilgileri içerir (ad, e -posta, ait olduğu kuruluş vb.) . Kullanıcıların gruplandırılması, kaynak erişim 

haklarının yönetimini kolaylaştırır . 

> •

Uygulama Meta Verileri (Application Metadata): Uygulamalar tarafından üretilir ve verilerin içeriği, 

üretildiği ortam veya bir veri işleme prosedürü gibi bilgileri temsil edebilir . 

> •

Kaynak Meta Verileri (Resource Metadata): Veri oluşturma, depolama ve aktarmada kullanılan 

kaynaklarla ilgili erişim adresi, fiziksel konum ve erişim kontrol listesi (ACL) gibi karakteristik bilgileri 

tanımlar .

4.2. Meta Veri Hizmeti (Metadata Service)  

> •

Meta Veri Depolama: Meta verileri depolamanın iki yaygın yolu vardır: ilişkisel bir veritabanı veya bir 

XML dosyası . Veritabanları, standart SQL ifadeleriyle erişim kolaylığı sunarken, dağıtılmış veritabanları 

ölçeklenebilirlik sorununu çözebilir . XML ise platformdan bağımsız yapısı, ücretsiz ve genişletilebilir 

olması nedeniyle esneklik ve doğal bir ölçeklenebilirlik avantajı sunar . 

> •

Veri Yayınlama ve Keşif: Meta veri hizmetleri, bilim insanlarının ham verilere ek açıklamalar gibi meta 

bilgiler eklemesine olanak tanıyarak veri keşfini kolaylaştırır . Kullanıcı bir sorguda istediği dosyanın 

özelliklerini belirttiğinde, bu sorgu bir meta veri kataloğuna gönderilir ve ilgili niteliklere sahip verilerle 

eşleştirilir .

5. Çoğaltma/Kopyalama (Replication) 

Veri çoğaltma, önbellek kavramından türemiştir ve daha iyi performans veya erişilebilirlik sağlamak amacıyla 

yeni bir kopyanın oluşturulmasıdır . Bu yöntem, şebeke veri erişimindeki darboğazları çözmekle kalmaz, 

aynı zamanda verimli veri erişim yeteneğini de artırır .

Çoğaltma Sürecindeki Bileşenler  

> •

Çoğaltma Meta Verileri (Replica Metadata): Mantıksal bir dosya adını, verilerin grid ortamında 

benzersiz bir tanımlayıcıya sahip olmasını sağlayan Küresel Benzersiz Tanımlayıcı (GUID) ile eşleştiren 

bilgileri depolar . 

> •

Çoğaltma Kataloğu (Replica Catalogue): Veri replikalarını kaydetmek ve sorgulamak için kullanılan 

bir hizmettir . Bir kullanıcı mantıksal bir dosya adı verdiğinde, katalog bir veya daha fazla fiziksel veri 

örneğinin konum bilgisini döndürür . 

> •

Replika Yönetimi (Replica Management): Bir depolama sitesinde veri kopyalarının oluşturulmasından 

ve silinmesinden sorumludur . Ayrıca replika kataloğunun bakımını da içerir . 

> •

Replika Seçimi (Replica Selection): Mevcut birden fazla kopya arasından en uygun olanının seçilmesi 

anlamına gelir . Optimum replika, yüksek erişim hızı sunan, transfer masraflarını azaltan veya daha yüksek 

güvenlik sağlayan kopyadır . Bu süreç, bazen büyük bir veri setinin sadece ihtiyaç duyulan bir alt 

kümesinin kopyasını oluşturarak veri aktarım yükünü de azaltabilir . 

> •

Replika Konumu (Replica Location): Bir kopyanın depolama konumunun bulunmasıdır . Yerel Konum 

Replika Kataloğu (LRC) yalnızca yerel bir sitenin kopyalarını kaydettiği için, tüm kopyalara genel bir 

bakış sunan Replika Konum İndeksi (RLI) adlı bir aracı kullanılır . RLI'lar, daha alt seviyedeki RLI'ları 

veya LRC'leri indeksleyerek hiyerarşik bir topolojide oluşturulabilir .Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and 

> Cloud Computing) Dersi

6

Aşağıdaki Şekil 1: Replika Konum Mimarisi , LRC'ler ve hiyerarşik olarak yapılandırılmış RLI'lar tarafından 

oluşturulan replika konum hizmetinin mimarisini göstermektedir .

Şekil 1 İki seviyeli hiyerarşik yapıda birden fazla LRC (location replica catalogue ) ve RLI (Replica Location 

Index ) tarafından oluşturulan replika konumu.