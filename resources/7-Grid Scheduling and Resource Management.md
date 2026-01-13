Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 

202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi 

1

1.  Şebek Çizelgeleme (planlama) ve Kaynak Yönetimi 

Şebeke , bilim, mühendislik, endüstri ve ticaretteki sorunları çözmek için yeni bir paradigma olarak 

ortaya çıkıyor. Giderek artan sayıda uygulama hesaplama, depolama ve diğer ihtiyaçlarını 

karşılamak için Grid altyapısını kullanıyor. Tek bir site, günümüzün zorl u uygulamalarının tüm 

kaynak ihtiyaçlarını artık karşılayamaz ve dağıtılmış kaynakları kullanmak, uygulama 

kullanıcılarına birçok fayda sağlayabilir. Grid sistemlerinin dağıtımı, heterojen, coğrafi olarak 

dağıtılmış ve dinamik olarak mevcut kaynakların ver imli yönetimini içerir. Bununla birlikte, bir 

Grid ortamının etkinliği, büyük ölçüde, yerelleştirilmiş kaynak aracıları olarak hareket eden 

zamanlayıcılarının etkinliğine ve verimliliğine bağlıdır. Şekil 1, örneğin kullanıcı görevlerinin 

Globus aracılığıyla Condor, Sun Grid Engine (SGE), Portable Batch System (PBS) , Yük Paylaşım 

Tesisi (Load Sharing Facility LSF) gibi bir dizi kaynak yönetimi ve iş planlama sistemine 

sunulabileceğini göstermektedir. 

Şebeke çizelgeleme, Şebeke işlerini birden çok yönetim alanı üzerindeki kaynaklara eşleme süreci 

olarak tanımlanır. Bir Şebeke işi   

> Figure 1İşler, Globus aracılığıyla Condor, SGE, PBS ve LSF tarafından yönetilen sistemlere gönderilebilir.

Bir Şebeke işi birçok küçük göreve bölünebilir. Zamanlayıcı, kaynakları seçme ve işleri, genel 

yürütme süresi (iş hacmi) ve kullanılan kaynakların maliyeti açısından kullanıcı ve uygulama 

gereksinimlerinin karşılanacağı şekilde planlama sorumluluğuna sahiptir. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 2

2.  Çizelgeleme Paradigmaları 

2.1.  Merkezi zamanlama 

Merkezi bir zamanlama ortamında, merkezi bir makine (düğüm), ortamın parçası olan tüm 

çevreleyen düğümler için işleri zamanlamak üzere bir kaynak yöneticisi olarak hareket eder. Bu 

zamanlama paradigması, genellikle kaynakların benzer özelliklere ve kullanı m politikalarına sahip 

olduğu bir bilgi işlem merkezi gibi durumlarda kullanılır. Şekil 2, merkezi programlamanın 

mimarisini göstermektedir.   

> Figure 2Merkezi zamanlama

Bu senaryoda, işler önce merkezi zamanlayıcıya gönderilir, bu da işleri uygun düğümlere gönderir. 

Bir düğümde başlatılamayan işler, normalde daha sonraki bir başlatma için merkezi bir iş 

kuyruğunda depolanır. 

Merkezi bir çizelgeleme sisteminin bir avantajı, mevcut kaynaklar hakkında tüm gerekli ve güncel 

bilgilere sahip olduğundan, çizelgeleyicinin daha iyi çizelgeleme kararları üretebilmesidir. 

Bununla birlikte, merkezileştirilmiş zamanlama, yönettiği ortamın artan boyutuyla açıkça iyi 

ölçeklenmiyor. Zamanlayıcının kendisi bir darboğaz haline gelebilir ve zamanlayıcı sunucusunun 

donanımı veya yazılımıyla ilgili bir sorun, yani bir arıza varsa, ortamda tek bir arıza noktası sunar. 

2.2.  Dağıtılmış zamanlama 

Bu paradigmada, tüm işleri yönetmekten sorumlu merkezi bir zamanlayıcı yoktur. Bunun yerine, 

dağıtılmış zamanlama, işleri katılan düğümlere göndermek için birbiriyle etkileşime giren birden 

çok yerelleştirilmiş zamanlayıcı içerir. Bir zamanlayıcının diğer zamanlayıcılarla iletişim kurması 

için iki mekanizma vardır - doğrudan veya dolaylı iletişim. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 3

Dağıtılmış zamanlama, merkezi paradigmada ortaya çıkan ölçeklenebilirlik sorunlarının 

üstesinden gelir; ayrıca daha iyi hata toleransı ve güvenilirlik sunabilir. Ancak, mevcut kaynaklar 

hakkında gerekli tüm bilgilere sahip olan global bir zamanlayıcının ol maması, genellikle optimal 

olmayan zamanlama kararlarına yol açar. 

2.2.1.  Doğrudan iletişim 

Bu senaryoda, her yerel zamanlayıcı, iş dağıtımı için diğer zamanlayıcılarla doğrudan iletişim 

kurabilir. Her zamanlayıcının etkileşimde bulunabilecekleri uzak zamanlayıcıların bir listesi vardır 

veya her zamanlayıcıyla ilgili tüm bilgileri tutan merkezi b ir dizin bulunabilir. Şekil 3, dağıtılmış 

zamanlama paradigmasında doğrudan iletişim mimarisini göstermektedir. 

Bir iş yerel kaynaklarına gönderilemiyorsa, planlayıcısı, işi yürütmek için uygun ve kullanılabilir 

kaynakları bulmak için diğer uzak zamanlayıcılarla iletişim kurar. Her zamanlayıcı, iş yönetimi 

için yerel bir iş kuyruğu/kuyrukları tutabilir.   

> Figure 3Dağıtılmış zamanlamada doğrudan iletişim

2.2.2.  Merkezi bir iş havuzu aracılığıyla iletişim 

Bu senaryoda, hemen yürütülemeyen işler merkezi bir iş havuzuna gönderilir. Doğrudan iletişim 

ile karşılaştırıldığında, yerel zamanlayıcılar potansiyel olarak kaynaklarını planlamak için uygun 

işleri seçebilirler. Havuzdaki tüm işlerin aynı anda yürütülmes i için politikalar gereklidir. Şekil 4, 

dağıtılmış zamanlama için bir iş havuzu kullanma mimarisini göstermektedir. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 

202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi 

4  

> Figure 4İş havuzuyla dağıtılmış zamanlama

2.3.  Hiyerarşik zamanlama 

Hiyerarşik çizelgelemede, merkezi bir çizelgeleyici, iş teslimi için yerel çizelgeleyicilerle 

etkileşime girer. Merkezi zamanlayıcı, gönderilen işleri yerel zamanlayıcılara gönderen bir tür 

meta zamanlayıcıdır. Şekil 5, bu paradigmanın mimarisini göstermektedir. Merkezi zamanlama 

paradigmasına benzer şekilde, hiyerarşik zamanlamada ölçeklenebilirl ik ve iletişim darboğazları 

olabilir. Bununla birlikte, merkezi zamanlama ile karşılaştırıldığında, hiyerarşik zamanlamanın bir 

avantajı, genel zamanlayıcı ve yerel zamanlayıcının işleri zamanlamak için farklı ilkelere sahip 

olabilmesidir.   

> Figure 5Hiyerarşik zamanlama

Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 

202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi 

5

3.  Kaynak seçimi 

Olası hedef kaynakların listesi bilindiğinde, programlama sürecinin ikinci aşaması, CPU 

kullanımı, kullanılabilir RAM veya disk depolama gibi kullanıcı tarafından dayatılan kısıtlamalara 

ve koşullara en uygun kaynakları seçmektir. Kaynak seçiminin sonucu, tüm kaynakların 

gönderilen bir iş veya iş listesi için minimum gereksinimleri karşılayabileceği R selected bir kaynak 

listesi belirlemektir. Kullanılabilir R available kaynaklar ve seçilen R selected kaynaklar arasındaki ilişki 

şöyledir: 

𝑅 𝑠𝑒𝑙𝑒𝑐𝑡𝑒𝑑 ⊆ 𝑅 𝑎𝑣𝑎𝑖𝑙𝑎𝑏𝑙𝑒 

3.1.  İş seçimi 

Kaynak seçim süreci, belirli bir iş için (Rselected )kaynak listesinden kaynak(lar) seçmek için 

kullanılır. Rselected listesindeki tüm kaynaklar işin gerektirdiği minimum gereksinimleri 

karşılayabildiğinden, işi yürütmek için en iyi kaynak(lar)ı seçmek için bir algoritmaya ihtiyaç 

vardır. Rastgele seçim bir seçim olsa da ideal bir kaynak seçimi politikası değildir. Kayna k seçim 

algoritması, kaynakların mevcut durumunu dikkate almalı ve nicel bir değerlendirmeye dayalı 

olarak en iyisini seçmelidir. Yalnızca C PU ve RAM'i dikkate alan bir kaynak seçim algoritması 

aşağıdaki gibi tasarlanabilir: 

burada W CPU - CPU hızına ayrılan ağırlık; CPU load – mevcut CPU yükü; CPU speed – gerçek CPU 

hızı; CPU min – minimum CPU hızı; W RAM – RAM'e ayrılan ağırlık; RAM usage – mevcut RAM 

kullanımı; RAM size – orijinal RAM boyutu; ve RAM min – minimum RAM boyutu. 

Şimdi üç olası aday arasından bir kaynak seçmek için kullanılan algoritmayı açıklamak için bir 

örnek veriyoruz. Her kaynakla ilişkili varsayılan parametreler Tablo 1'de verilmiştir. 

Algoritmada kullanılan toplam ağırlığın 10, CPU ağırlığı 6 ve RAM ağırlığı 4 olduğunu 

varsayalım. Minimum CPU hızı 1 GHz ve minimum RAM boyutu 256 MB'dir. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 6

Tablo 1: Kaynak bilgi matrisi 

Ardından, kaynaklar için değerlendirme değerleri üç formül kullanılarak hesaplanabilir: 

Sonuçlardan, Kaynak3'ün (Resource 3) gönderilen iş için en iyi seçim olduğunu biliyoruz. 

3.2.  Kaynak seçimi 

İş seçiminin amacı, yürütme için bir iş kuyruğundan bir iş seçmektir. Bir iş seçmek için 

kullanılabilecek dört strateji aşağıda verilmiştir. 

İlk gelen ilk hizmeti alır(First come first serve ): Zamanlayıcı, gönderim sırasına göre 

yürütülecek işleri seçer. Seçilen iş için kullanılabilecek kaynak yoksa, planlayıcı iş başlatılıncaya 

kadar bekleyecektir. İş kuyruğundaki diğer işler beklemek zorunda. Bu tür iş seçiminin iki ana 

dezavantajı vardır. Ör neğin, seçilen iş başlamadan önce daha fazla kaynağa ihtiyaç duyduğunda 

kaynakları boşa harcayabilir ve bu da uzun bir bekleme süresine neden olur. Ve düşük önceliğe 

sahip bir işin tamamlanması için daha fazla zamana ihtiyacı varsa, yüksek önceliklere sahi p işler 

hemen gönderilemez. 

Rastgele seçim (Random Selection) : Planlanacak bir sonraki iş, iş kuyruğundan rastgele seçilir. 

İlk gelen ilk hizmet stratejisinin iki dezavantajı dışında, iş seçimi adil değildir ve daha önce teslim 

edilen işler çok sonraya kadar planlanmayabilir. 

Önceliğe dayalı seçim (Priority -based selection): Zamanlayıcıya gönderilen işlerin farklı 

öncelikleri vardır. Planlanacak bir sonraki iş, iş kuyruğunda en yüksek önceliğe sahip iştir. İş 

gönderildiğinde bir iş önceliği ayarlanabilir. Bu stratejinin bir dezavantajı, bir iş önceliği için Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 7

optimal bir kriter belirlemenin zor olmasıdır. En yüksek önceliğe sahip bir iş, mevcut olandan daha 

fazla kaynağa ihtiyaç duyabilir ve ayrıca uzun bir bekleme süresine ve mevcut kaynakların iyi 

kullanılmamasına neden olabilir. 

4.  Platform Globus Toolkit 3.0 

Şekil 6' da gösterildiği gibi Platform Globus Toolkit 3.0 (PGT3), Globus Toolkit 3.0'ın (GT3) ticari 

bir dağıtımıdır. GT3'te bulunan temel hizmetlere ek olarak, PGT3, GT3 üzerine kurulu bir dizi 

Grid hizmetinin açık kaynaklı bir uygulaması olan Topluluk Zamanlayıcı Çerçevesi'ne 

(Community Scheduler Framework CSF) dayalı uzantılar içerir. CSF, meta zamanlayıcıları 

uygulamak için bileşenler sağlar.     

> Figure 6Platform Globus Toolkit 3.0 ( PGT3) Mimarisi

PGT3, SGE, Condor, LSF ve PBS gibi çeşitli kaynak yönetim sistemleri arasında şeffaf etkileşim 

ve birlikte çalışabilirlik sağlar. Bir LSF istemcisinin işleri SGE tarafından yönetilen bir kümeye 

göndermesine olanak tanır. PGT3'ün temel bileşeni CSF Plus'tır. Son kullanıcıların temel kaynak 

yönetim sistemleriyle etkileşime girmesine olanak tanıyan bir meta zamanlayıcı altyapısı sağla r.