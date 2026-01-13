Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 1

Şebeke Hesaplama ve Bulut Bilişim 

Fanı veya herhangi bir elektrikli cihazı açtığımızda, güç kaynağının nereden geldiği ve nasıl 

üretildiği ile daha az ilgileniyoruz. Evimizde aldığımız güç kaynağı veya elektrik, elektrik 

santrallerini, transformatörleri, elektrik hatlarını ve iletim istasy onlarını içeren bir ağ zinciri 

boyunca hareket eder. Bu bileşenler birlikte bir "Güç Şebekesi" oluşturur. Aynı şekilde, " Şebeke 

Hesaplama", bilgisayarlar, sunucular, iş istasyonları ve depolama öğeleri gibi bilgi işlem 

kaynaklarını birbirine bağlayan ve bu nlara erişmek için gereken mekanizmayı sağlayan bir 

altyapıdır. 

Şebeke Hesaplama , bir ağdaki farklı BT kaynaklarını koordine ederek bir bütün olarak çalışmasına 

izin veren bir ara katman yazılımıdır. Daha çok bilimsel araştırmalarda ve üniversitelerde eğitim 

amaçlı kullanılmaktadır. Örneğin, farklı bir proje üzerinde çalışan bir grup mimar öğrencisi, 

tasarım amaçları için belirli bir tasarım aracı ve yazılımı gerektirir, ancak yalnızca birkaçı bu 

tasarım aracına erişebilir, sorun bu aracı diğer öğrencilerin kullanımına nasıl sunabilecekleridir. 

Diğer öğrenciler için kul lanılabilir hale getirmek için bu tasarım aracını kampüs içi ağa koyacaklar, 

şimdi şebeke tüm bu bilgisayarları kampüs ağındaki birbirine bağlayacak ve öğrencilerin projeleri 

için gereken tasarım aracını her yerden kullanmalarına izin verecek. 

Bulut bilişim ve Şebeke bilişim genellikle kafa karıştırıcıdır, ancak işlevleri neredeyse benzerdir, 

işlevsellik yaklaşımları farklıdır. Bakalım nasıl çalışıyorlar ;

Grid Computing  Cloud Computing 

Şebeke hesaplama, ortak bir hedefi 

gerçekleştirmek için mevcut kaynakları ve 

birbirine bağlı bilgisayar sistemlerini kullanır 

Bulut bilgi işlem, bilgisayar kaynaklarını 

kullanmak için daha çok bir hizmet sağlayıcı 

olarak çalışır .

Şebeke hesaplama, merkezi olmayan bir 

modeldir ve hesaplamanın birçok yönetim 

modeli üzerinde gerçekleşebilir. 

Bulut bilişim, merkezi bir modeldir 

Şebeke hesaplama , birden çok yerde birden 

çok tarafa ait olan ve kullanıcıların 

kaynakların birleşik gücünü paylaşabilmeleri 

için birbirine bağlı bir bilgisayar 

topluluğudur. 

Bulut, genellikle tek bir tarafa ait olan 

bilgisayarlar topluluğudur. 

Şebeke , sınırlı hizmetler sunar 

Bulut, web barındırma, DB (Veri Tabanı) 

desteği ve çok daha fazlası gibi tüm 

hizmetlerin çoğunda daha fazla hizmet sunar 

Şebeke hesaplama, farklı organizasyonlarda 

bulunan kaynakları birleştirir. 

Bulut bilişim, genellikle tek bir kuruluş içinde 

sağlanır (ör: Amazon) Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 2

Grid ve Bulut Bilişim Arasındaki Benzerlikler 

• Bilgi işlem maliyetini azaltmak ,

• Güvenilirliği artırmak, 

• Bilgisayarları satın alıp kendi kendimize işlettiğimiz bir şeyden üçüncü şahıslar tarafından 

işletilen bir şeye dönüştürerek esnekliği artırmak .

Tablo : Şebeke Hesaplama ve Bulut Bilişim Karşılaştırması 

Özellikler  Şebeke Hesaplama 

(Grid Computing) 

Bulut Bilişim 

(Cloud Computing) 

Kullanım 

yöntemleri 

Birden çok sunucunun tek bir 

göreve veya işe tahsis edilmesi. 

Sunucuların sanallaştırılması; birkaç 

görevi aynı anda hesaplamak için bir 

sunucu. 

Tipik kullanım 

şekli 

Genellikle iş yürütme, yani bir 

programın sınırlı bir süre için 

yürütülmesi için kullanılır. 

Uzun süreli hizmetleri desteklemek 

için daha sık kullanılır. 

Soyutlama düzeyi  Yüksek düzeyde ayrıntıyı ortaya 

çıkarın. 

Daha üst düzey soyutlamalar 

sağlayın. 

Hesaplama (Bilgi 

İşlem) Hizmeti 

Maksimum hesaplama (bilgi 

işlem )

Talep üzerine (isteğe bağlı) 

Ulaşılabilirlik 

(Erişilebilirlik) 

Üst düzey bilgi işlem 

yeteneklerine güvenilir, tutarlı, 

yaygın ve ucuz erişim sunar. 

Kolay ve kapsamlı erişime sahip 

kullanıcılar için özelleştirilmiş, 

ölçeklenebilir ve QoS garantili bilgi 

işlem ortamları sunar. 

Altyapı 

Coğrafi olarak dağıtılmış sitelere 

yayılan ve merkezi kontrolden 

yoksun, merkezi olmayan bir 

sistem. Normalde 

donanım/yazılım 

konfigürasyonları, erişim 

arayüzleri ve yönetim ilkeleri 

gibi heterojen kaynakları içerir. 

Tek bir erişim noktasına sahip olan 

ve genel olarak Google ve Amazon 

gibi çeşitli bilgi işlem merkezlerini 

kapsayan merkezi bir bilgisayar 

sunucusu, merkezi kontrol altında 

çalıştırılan homojen kaynaklar içerir. 

Sanallaştırma  Veri ve bilgi işlem kaynaklarının 

sanallaştırılması. 

Donanım ve yazılım platformlarının 

sanallaştırılması. 

Kullanıcı 

Yönetimi 

Merkeziyetiz Yönetim  Merkezileştirilmiş Yönetim 

Ölçeklenebilirlik  Normal  Yüksek 

Mimari  Dağıtılmış bilgi işlem mimarisi.  İstemci -sunucu mimarisi. 

Bağımlılık  Bilgisayar durduğunda diğer 

bilgisayar işi alır. 

Tamamen internete bağlı. 

İşlem (Operasyon)  Kurumsal bir ağ içinde çalışır.  İnternet üzerinden de çalışabilir. Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 3

Şebeke Hesaplama: 

Şeneke Hesaplama , bir Dağıtılmış bilgi işlem mimarisidir. Şebeke hesaplamada, kaynaklar 

işbirlikçi modelde kullanılır ve ayrıca şebeke hesaplamada kullanıcılar kullanım için ödeme 

yapmazlar. 

Bulut Bilişim: 

Bulut Bilişim, bir İstemci -sunucu bilişim mimarisidir. Bulut bilişimde kaynaklar merkezi bir 

düzende kullanılır ve bulut bilişim yüksek erişilebilir bir hizmettir. Bir öde ve kullan iş aracıdır, 

bulut bilişimde, kullanıcılar kullanım için öderler.