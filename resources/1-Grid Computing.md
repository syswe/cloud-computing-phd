Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi

Grid Computing  (Şebeke Hesaplama) 

Grid Computing, tek bir makine için oldukça zor olan bir görevi gerçekleştirmek için birlikte 

çalışan bir bilgisayar ağı olarak tanımlanabilir. Bu ağdaki tüm makineler, sanal bir süper bilgisayar 

gibi  davranmak için aynı protokol altında çalışır. Üzerinde çalıştıkları görev, büyük veri 

kümelerini analiz etmeyi veya yüksek bilgi işlem gücü gerektiren durumları simüle etmeyi 

içerebilir. Ağdaki bilgisayarlar, ağa işlem gücü ve depolama kapasitesi gibi kayn aklar sağlar. 

Grid Computing, sanal bir süper bilgisayarın, çoğunlukla Ethernet veya bazen İnternet olmak üzere 

bir veri yolu ile bağlanan bir ağ üzerindeki makinelerden oluştuğu, dağıtılmış bilgi işlemin bir alt 

kümesidir. Aynı zamanda, tek bir makinedeki birçok CPU çe kirdeği yerine çeşitli konumlara 

yayılmış birden çok çekirdek içerdiği bir Paralel Hesaplama biçimi olarak da görülebilir. Grid 

hesaplama kavramı yeni değil, ancak insanlar tarafından oluşturulmuş ve kabul edilmiş standart 

kurallar ve protokoller olmadığı  için henüz mükemmelleşmedi. 

Çalışma  Prensibi : Bir Grid Computing ağı temel olarak bu üç tip makineden oluşur. 

Kontrol Düğümü : Tüm ağı yöneten ve ağ havuzundaki kaynakların hesabını tutan bir bilgisayar, 

genellikle bir sunucu veya bir grup sunucu. 

Sağlayıcı : Ağ kaynak havuzundaki kaynaklarına katkıda bulunan bilgisayar. 

Kullanıcı : Ağdaki kaynakları kullanan bilgisayar. 

Bir bilgisayar kontrol düğümüne kaynak talebinde bulunduğunda, kontrol düğümü kullanıcıya 

ağda bulunan kaynaklara erişim  sağlar. Kullanılmadığı zaman ideal olarak kaynaklarını ağa 

katkıda bulunmalıdır. Bu nedenle, düğümdeki normal bir bilgisayar, ihtiyaçlarına göre kullanıcı 

veya sağlayıcı olmak arasında gidip gelebilir. Düğümler, homojen ağlar olarak adlandırılan aynı 

işlet im sistemini kullanan benzer platformlara sahip makinelerden veya heterojen ağlar olarak 

adlandırılan çeşitli farklı bir işletim sistemi üzerinde çalışan farklı platformlara sahip makinelerden 

oluşabilir. Bu, grid hesaplamanın diğer dağıtılmış hesaplama mi marilerinden ayırt edici kısmıdır. 

Ara yazılımın  (middleware ) diğer bir görevi, ağ üzerinde yürütülmekte olan herhangi bir işlemi 

yetkilendirmektir. Bir grid bilgi işlem sisteminde, bir sağlayıcı, kullanıcının bilgisayarında Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi

herhangi bir şeyi çalıştırmasına izin verir, bu nedenle ağ için büyük bir güvenlik tehdididir. Bu 

nedenle, bir ara yazılım, ağ üzerinde yürütülmekte olan istenmeyen bir görevin olmamasını 

sağlamalıdır. 

Ian Foster ve Carl Kesselman'ın 1999'da yayınladıkları “The Grid: Blueprint for a new computing 

altyapısı”na göre Grid Computing teriminin anlamı yıllar içinde değişti, fikir bilgi işlem gücünü 

bir güçten tüketilen elektriğin tüketilmesi gibi tüketmekti. B u fikir, mevcut bulut bilişim 

konseptine benzerken, şimdi grid bilişim, dağıtılmış bir işbirliği ağı olarak görülüyor. Halihazırda, 

grid hesaplama, birçok matematiksel, analitik ve fizik problemini çözmek için çeşitli kurumlarda 

kullanılmaktadır. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi

Grid hesaplama, ortak görevleri gerçekleştirmek için birlikte çalışmak üzere, genellikle coğrafi 

olarak dağıtılmış ancak ağlarla birbirine bağlı olan birden çok bilgisayarı kullanma pratiğidir. 

Genellikle, işleri koordine etmek için birbirleriyle doğrudan  etkileşime giren bir dizi bilgisayar 

olan bir "veri ızgarası -data grid " üzerinde çalıştırılır. 

Grid hesaplama, veri ızgarasına katılan her bilgisayarda özel yazılım çalıştırarak çalışır. Yazılım, 

tüm sistemin yöneticisi olarak hareket eder ve şebekedeki çeşitli görevleri koordine eder. Spesifik 

olarak, yazılım her bilgisayara alt görevler atar, böyl ece ilgili alt görevlerinde aynı anda 

çalışabilirler. Alt görevlerin tamamlanmasından sonra, çıktılar toplanır ve daha büyük ölçekli bir 

görevi tamamlamak için toplanır. Yazılım, her bilgisayarın diğer bilgisayarlarla ağ üzerinden 

iletişim kurmasını sağlar , böylece her bir bilgisayarın alt görevlerin hangi bölümünü çalıştırdığı 

ve çıktıların nasıl birleştirilip teslim edileceği hakkında bilgi paylaşabilirler. 

Şebeke hesaplama ile, veri şebekesine katılan her bilgisayarda özel yazılımlar çalışır. Bu kontrolör 

yazılımı, tüm sistemin yöneticisi olarak hareket eder ve şebeke boyunca çeşitli görevleri koordine 

eder. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi

Grid Hesaplamanın Avantajları: 

a)  İşleme için değil, sadece kontrol için kullanılan kontrol düğümü dışında, gerekli sunucu 

olmadığı için merkezi değildir. 

b)  Birden çok heterojen makine, yani farklı İşletim Sistemlerine sahip makineler, tek bir 

ızgara bilgi işlem ağı kullanabilir. 

c)  Görevler, çeşitli fiziksel konumlarda paralel olarak gerçekleştirilebilir .

Grid Hesaplama Nasıl Kullanılır ? 

Grid hesaplama, özellikle farklı konu uzmanlarının bir proje üzerinde işbirliği yapması 

gerektiğinde yararlıdır, ancak tek bir sitede veri ve bilgi işlem kaynaklarını hemen paylaşmak için 

gerekli araçlara sahip değildir. Coğrafi mesafeye rağmen güçlerini b irleştirerek, dağıtılmış ekipler 

daha büyük bir çabaya katkıda bulunan kendi kaynaklarından yararlanabilir. Bu, tüm bilgi işlem 

kaynaklarının aynı belirli görev üzerinde çalışması gerekmediği, ancak toplu olarak nihai hedefi 

oluşturan alt görevler üzerinde  çalışabileceği anlamına gelir. Örneğin, bir araştırma ekibi Kuzey 

Atlantik bölgesindeki hava durumunu analiz ederken, başka bir ekip güney Atlantik bölgesini 

analiz eder ve her iki sonuç da Atlantik hava durumu modellerinin eksiksiz bir resmini sunmak 

içi n birleştirilebilir. 

Genellikle büyük ölçekli dağıtılmış bir bilgi işlem çabası olarak görülse de, ızgara hesaplama yerel 

düzeyde de kullanılabilir. Örneğin, belirli bir görevi ortaklaşa gerçekleştirmek için bir kümede 

çalışan bir dizi bilgisayar düğümünü tahsis eden bir şirke t, eylem halindeki ızgara hesaplamanın 

basit bir örneğidir. Belirli bir yerel veri ızgarası türü, bilgisayarların koordinasyon yazılımı ve bir 

ağ bağlantısı aracılığıyla bellekteki verileri toplu olarak işlemek için sıkı bir şekilde bağlandığı bir 

bellek i çi veri ızgarasıdır (in -memory data grid -IMDG). Avantajı, verilerin veri şebekesindeki tüm 

bilgisayarlarda bellekte saklanmasıdır, bu nedenle tüm veri erişimleri çok hızlıdır. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi

Bellek İçi Veri Izgaraları  (In -Memory Data Grids ), daha yüksek verim ve daha düşük gecikme 

süresi sağlayarak grid  hesaplamanın  performansını artırır. 

Grid (Izgara -Şebeke) Mimarisi: Temel Kavramlar 

Grid  mimarisi, katmanlı bir mimari olarak görselleştirilebilir. En üstteki katman, bir kullanıcının 

bakış açısından  Grid  uygulamaları ve API'lerden oluşur. Ardından, grid uygulaması için kullanılan 

yazılım ve paketleri içeren ara katman yazılımına sahibiz, örneğin Globus Toolkit, gLite. Üçüncü 

katman, depolama, işleme yetenekleri ve diğer uygulamaya özel donanımlar gibi şebe keye sunulan 

kaynakları kapsar. Son olarak dördüncü katman, yönlendiriciler, anahtarlar ve şebekedeki herhangi 

iki sistem arasındaki iletişi m için kullanılan protokoller gibi ağ bileşenleriyle ilgilenen ağ 

katmanıdır. 

Güvenlik (Security) 

Tıpkı dünyadaki herhangi bir sistem gibi, güvenlik de grid hesaplamanın hayati yönünü oluşturur. 

Bir şebekenin sağlaması gereken en çok arzu edilen üç güvenlik özelliğine bakıyoruz. Bunlar çoklu 

oturum açma, kimlik doğrulama ve yetkilendirmedir. Tek oturum  açma, kullanıcının güvenlik 

kimlik bilgilerini kullanarak bir kez oturum açabilmesi ve ardından belirli bir süre boyunca şebeke 

hizmetine erişebilmesi anlamına gelir. Kimlik doğrulama, kişinin kimliğini oluşturmak için gerekli 

kanıtın sağlanması anlamına  gelir. Bu nedenle, e -posta hesabınıza giriş yaptığınızda, kullanıcı Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi

adınızı ve şifrenizi girerek sunucuya kimlik doğrulaması yaparsınız. Yetkilendirme, bir kullanıcıya 

atanan ayrıcalıkları kontrol eden işlemdir. Örneğin, bir web sitesinde misafir kullanıcı ve kayıtlı 

kullanıcı olmak üzere iki tür kullanıcı olabilir. Konuk  kullanıcının temel görevleri 

gerçekleştirmesine izin verilirken, kayıtlı kullanıcının tercihlerine göre bir dizi görevi 

gerçekleştirmesine izin verilebilir. Yetkilendirme, bir kullanıcının kimliği kimlik doğrulama 

yoluyla oluşturulduktan sonra gerçekleştir ilir. Güvenlik altyapısının parçası olan şebekenin diğer 

bileşenleri, kimlik bilgisi yönetimi ve ayrıcalıkların devredilmesidir. 

Kaynak yönetimi (Resource Management) 

Bir şebeke  (grid) , mümkün olan maksimum verimi elde etmek için emri altındaki kaynakları 

optimize etmelidir. Kaynak yönetimi, bir işin uzaktan gönderilmesini, devam ederken durumunun 

kontrol edilmesini ve yürütme bittiğinde çıktının alınmasını içerir. Bir iş gönderildiğind e, mevcut 

kaynaklar bir rehber hizmeti aracılığıyla keşfedilir. Ardından, tek tek işi çalıştırmak için kaynaklar 

seçilir. Bu karar, şebekenin başka bir kaynak yönetimi bileşeni, yani şebeke zamanlayıcısı 

tarafından verilir. Zamanlama karar ı bir dizi faktöre dayanabilir. Örneğin, bir uygulama, bir işin 

sonucuna başka bir iş tarafından ihtiyaç duyulduğundan sıralı yürütmeye ihtiyaç duyan bazı 

işlerden oluşuyorsa, zamanlayıcı bu işleri sıralı olarak zamanlayabilir. Zamanlama kararı, SLA'da 

bel irtildiği gibi kullanıcının işinin önceliğine de dayalı olabilir. 

Service  Level  Agreement (SLA)  - Hizmet  Düzeyi  Sözleşmes i

SLA, kullanıcının beklediği minimum hizmet kalitesini, kullanılabilirliği vb. ve bu hizmetlerden 

alınan ücretleri belirtir. Daha spesifik olmak gerekirse, SLA, sistem için beklenen minimum 

çalışma süresini belirtebilir. 

Veri yönetimi (Data Management) 

Şebekelerdeki  (gridler)  veri yönetimi, büyük miktarda veriyi yönetmek için gereken çok çeşitli 

yönleri kapsar. Buna güvenli veri erişimi, verilerin kopyalanması ve taşınması, meta verilerin 

yönetimi, dizin oluşturma, veriye duyarlı zamanlama, önbelleğe alma vb. dahildir. Veri bi linçli 

çizelgeleme, çizelgeleme kararlarının verilerin konumunu dikkate alması gerektiği anlamına gelir. 

Örneğin, şebeke zamanlayıcı, önemli performans giderlerine neden olabilecek büyük miktarda 

veriyi ağ üzerinden aktarmak yerine v erilere yakın bulunan bir kaynağa bir iş atayabilir. İşin, iş Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi

için gerekli verilere sahip olmayan bir sistemde çalışacak şekilde programlandığını varsayalım. Bu 

veriler işin yürütüleceği sisteme aktarılmalıdır. Bu nedenle, bir şebeke veri yönetimi modülü, 

şebeke içinde veri aktarımı için güvenli ve güvenilir bir yol  sağlamalıdır. 

Bilgi Keşfi ve İzleme (Information Discovery and Monitoring) 

Şebeke zamanlayıcısının bir işi gerçekleştirmek için kaynakları tahsis etmek için mevcut 

kaynakların farkında olması gerektiğinden bahsetmiştik. Bu bilgiler, ızgarada çalışan bir bilgi 

bulma hizmetinden elde edilir. Bilgi bulma hizmeti, şebekenin elden çık arılması için mevcut 

kaynakların bir listesini ve mevcut durumlarını içerir. Bir ızgara zamanlayıcı, mevcut kaynaklar 

için bilgi hizmetini sorguladığında, ilgili ve bir iş için en uygun kaynakları bulmak gibi kısıtlamalar 

koyabilir. Kaynağın uygunluğu ile,  iş için kullanılabilecek kaynakları kastediyoruz. Bir iş için 

gereken bilgi işlem kapasitesinden bahsedersek ve iş, yürütülmesi için hızlı CPU'lar gerektiriyorsa, 

yalnızca işin zamanında tamamlanması için yeterince hızlı olan makineleri seçeriz. Bilgi bul ma 

hizmeti iki şekilde çalışabilir. Mevcut kaynakların durumunu tanımlanmış bir arayüz (web 

servisleri) üzerinden yayınlayabilir veya mevcut kaynakların listesi için sorgulanabilir. Bilgi 

bulma hizmeti, hiyerarşik bir biçimde düzenlenebilir, burada alt bil gi keşif hizmetleri, üstte 

bulunana bilgi sağlar. Hiyerarşik yapı, çok miktarda kaynak içeren şebekeler için gereken esnekliği 

sağlar, çünkü mevcut tüm kaynaklar hakkındaki bilgileri tek bir yerde saklamak pratik olarak 

imkansız hale gelebilir.