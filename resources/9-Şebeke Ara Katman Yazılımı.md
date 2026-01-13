Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 1

1. Şebeke Ara Katman Yazılımı (Gr id Middleware) 

1.1. Tanım ve Kapsam  

> •

Şebeke Sistemleri Bileşenleri: Grid sistemleri, coğrafi olarak dağıtılmış çeşitli 

kuruluşlarda bulunan heterojen kaynakların bir araya getirilmesini içerir:  

> o

Hesaplama kaynakları (Süper bilgisayarlar, sunucular, özel bilgisayarlar, kümeler).  

> o

Depolama kaynakları.  

> o

Ağ kaynakları.  

> o

Bilimsel araçlar (Teleskoplar, sensör ağları gibi, gerçek zamanlı veri sağlayan).  

> •

Şebeke Dokusu (Grid Fabric): Bu kaynakların tamamı, Grid Dokusunu (Grid Fabric) 

oluşturur.  

> •

Ara Katman Yazılımının Tanımı: Kullanıcılara heterojen bir şebeke ortamında 

kesintisiz bilgi işlem yeteneği ve kaynaklara tek tip erişim sağlayan yazılımdır. 

1.2. Amaç 

Şebeke ara katman yazılımına duyulan ihtiyaç, aşağıdaki temel amaçlara hizmet etmekten 

kaynaklanır: 

• Kaynak Erişimi: Şebeke kaynaklarına erişimi sağlamak. 

• Kullanımı Kolaylaştırma: Bu kaynakların kullanımını kolaylaştırmak. 

• Kaynak Sağlayıcıyı Koruma: Kaynak sağlayıcıların çıkarlarını korumak. 

Ara katman yazılımının etkili olabilmesi için aşağıdaki özelliklere sahip olması gerekir: 

• Paylaşılabilirlik 

• Yeniden Kullanılabilirlik 

• Genişletilebilirlik 

• Geliştirme Süresini En Aza İndirme: Geliştirme, yeniden geliştirme ve devreye alma 

için gereken süreyi en aza indirmek.   

> Şekil 1Şebeke mimarisindeki şebeke ara katmanı yazılımı

Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD  

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 2

2. Şebeke Portalları (Grid Portals) 

2.1. Tanım ve Fonksiyon  

> •

Tanım: Şebeke portalları, kullanıcılara Grid kaynaklarına erişmek için birleşik ve tutarlı 

bir yol sunar.  

> •

İçerik: Portal sayfaları, farklı kullanıcılar için içerik oluşturan farklı portlet setlerine 

sahip olabilir. 

2.2. Temel Bileşenler: Portletler  

> •

Tanım: İstekleri işleyen ve dinamik içerik üreten, Java teknolojisi tabanlı bir web 

bileşenidir.  

> •

Yönetim: Bir portlet kapsayıcısı (portlet container) tarafından yönetilirler. 

3. Portal Geliştirme Araçları ve Örnekler 

3.1. Geliştirme Araçları 

Grid portallarının geliştirilmesi için kullanılan araçlar şunlardır:  

> •

Grid Portal Geliştirme Kiti (Grid Portal Development Kit - GPDK)  

> •

Grid Portal Toolkit (GPT) 

3.2. GridSphere: Portlet Tabanlı Web Portalı 

Geliştirme ve Kapsam:  

> •

GridLab projesi tarafından geliştirilmiştir.  

> •

Aslında yaygın bir web geliştirme ortamıdır ve herhangi bir Grid teknolojisi ile 

doğrudan bağlantılı değildir .

Temel Amaçları:  

> •

İyi entegre edilmiş ve kullanımı kolay portletler oluşturmak.  

> •

Çevrimiçi işbirliği, hesaplama, veri yönetimi ve veri görüntülemeyi gerçekleştirmek için 

kullanılabilir. 

Geliştirici Desteği:  

> •

Kullanıcılara özelleştirilmiş portlet geliştirmeleri için üst düzey bir API sunar. 

3.3. Grid Portletleri (Grid Portlets)  

> •

Tanım: GridSphere ile işbirliği yapan bir dizi portlettir.  

> •

İşlevler: Bu portletler, indirilip GridSphere'e yerleştirildiğinde bir dizi Grid uygulamasına 

yönelik işlevsellik sağlar: Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD   

> 202 5-202 6Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi
> 3
> o

Kimlik bilgisi talebi ve yönetimi.  

> o

Kaynak arama.  

> o

İş gönderme (job submission).  

> o

Dosya aktarımı.  

> •

Geliştirici Kullanımı: Geliştiriciler, bu mevcut portletlere dayanarak daha yüksek seviyeli 

API'ler kullanarak daha güçlü portletler oluşturabilirler.