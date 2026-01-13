Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 

202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi 

1

Bulut Bilişim: Mimari, Uygulama Alanları ve Ölçeklenebilirlik 

1. Bulut Bilişim 

Bulut bilişim (Cloud Computing) ; bilgi işlem kaynaklarının (sunucu, depolama, ağ, yazılım ve 

platformlar) internet üzerinden isteğe bağlı , ölçeklenebilir ve kullandıkça öde modeliyle 

sunulmasını ifade eden bir bilişim paradigmasıdır. 

Bulut bilişim: 

• Kaynak soyutlama (resource abstraction) 

• Dinamik kaynak tahsisi 

• Çok kullanıcılı (multi -tenant) mimari 

• Otomatik ölçekleme 

özellikleriyle klasik veri merkezi anlayışından ayrılır. 

Önemli Nokta :

Bulut bilişim yalnızca bir teknoloji değil, aynı zamanda işletim modeli ve ekonomik model 

değişimidir (CAPEX → OPEX dönüşümü). 

1. 1 Günlük Hayatta Bulut Bilişim Örnekleri  

> •

E-posta servisleri → Gmail, Outlook  

> •

Sosyal medya → Facebook, Instagram  

> •

Video akışı → YouTube, Netflix  

> •

Ofis uygulamaları → Google Docs  

> •

Fotoğraf depolama → Google Photos, Flickr 

Bu uygulamaların ortak noktası: Verinin yerel cihazda değil , uzaktaki bulut veri merkezlerinde 

tutulmasıdır. 

Şekil 1 – Bulut Bilişim Temel Fikri Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 

202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi 

2

2. Bulut Hizmet Sağlayıcıları 

2.1 Önde Gelen Bulut Sağlayıcıları 

* Amazon Web Services (AWS)  

> •

İlk büyük ölçekli bulut sağlayıcı  

> •

IaaS, PaaS ve SaaS hizmetlerinin birleşimi  

> •

EC2, S3, RDS gibi servislerle esnek mimari 

* Microsoft Azure  

> •

Microsoft ekosistemiyle güçlü entegrasyon  

> •

Hibrit bulut çözümleri açısından lider  

> •

Kurumsal uygulamalarda yaygın kullanım 

* Google Cloud Platform (GCP)  

> •

Büyük veri, yapay zekâ ve makine öğrenmesi odaklı  

> •

Kubernetes ve container teknolojilerinde öncü 

* Diğer Sağlayıcılar  

> •

Salesforce (CRM odaklı SaaS)  

> •

Oracle Cloud (veritabanı merkezli)  

> •

IBM Cloud (AI ve kurumsal çözümler) 

Not: Sağlayıcı seçimi; performans, regülasyon, veri egemenliği (data sovereignty) ve maliyet 

optimizasyonu gibi çok boyutlu kriterlere bağlıdır. 

3. Bulut Mimarisinin Temelleri 

3.1 Bulut Mimarisi Kavramı 

Bulut mimarisi; istemci ile bulut altyapısı arasındaki donanım, yazılım ve ağ bileşenlerinin nasıl 

yapılandığını tanımlar. 

Temel olarak iki ana bileşenden oluşur:  

> •

Front -End (Ön Uç)  

> •

Back -End (Arka Uç) 

Şekil 2 – Bulut Mimarisinin Genel Yapıs ıKocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 

202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi 

3

3.2 Front -End (Ön Uç) 

Ön uç:  

> •

Kullanıcının doğrudan etkileşimde bulunduğu katmandır  

> •

Web tarayıcıları, mobil uygulamalar, masaüstü istemciler bu kapsamdadır 

Örnek: 

Gmail arayüzü, Google Docs editörü 

3.3 Back -End (Arka Uç) 

Arka uç:  

> •

Bulut sağlayıcı tarafından yönetilen gizli katmandır  

> •

Veri merkezleri, sanallaştırma altyapısı, yük dengeleyiciler içerir 

Açıklama: Back -end genellikle mikroservis mimarisi, container orkestrasyonu (Kubernetes) ve yazılım 

tanımlı ağ (SDN) gibi modern teknolojilerle çalışır. 

4. Bulut Bilişimin Çalışma Mantığı 

1.  Kullanıcı → Ön uçtan istek gönderir 

2.  Kimlik doğrulama yapılır 

3.  İstek uygun servise yönlendirilir 

4.  Veri işlenir ve sonuç döndürülür 

Şekil 3 – Bulut Bilişim İş Akışı Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 

202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi 

4

5. Bulut Bilişimin Uygulama Alanları 

5.1 İş Uygulamaları  

> •

MailChimp  

> •

QuickBooks  

> •

Google Workspace 

5.2 Veri Depolama ve Yedekleme  

> •

Google Drive  

> •

Dropbox  

> •

OneDrive 

5.3 Yönetim ve Organizasyon  

> •

Trello  

> •

Accelo  

> •

Easynote 

5.4 Sosyal, Eğlence ve Eğitim  

> •

Sosyal: Facebook, LinkedIn  

> •

Eğlence: Netflix, Spotify  

> •

Eğitim: Google Classroom, Blackboard 

Avantajlar:  

> •

Maliyet düşüşü  

> •

Gerçek zamanlı iş birliği  

> •

Ölçeklenebilir altyapı 

6. Ölçeklenebilirlik (Scalability) 

Ölçeklenebilirlik , sistemin değişen iş yüküne göre kaynaklarını dinamik biçimde artırıp azaltabilme 

yeteneğidir. 

Bulut bilişimin en kritik avantajıdır. 

6. 1 Ölçeklenebilirlik Türleri 

* Dikey Ölçekleme (Vertical Scaling) 

[ Sunucu ]: ↑ CPU ↑ RAM  

> •

Donanımsal sınır vardır  

> •

Kısa vadede etkilidir 

* Yatay Ölçekleme (Horizontal Scaling)  

> •

Dağıtık sistemler için idealdir  

> •

Mikroservis mimarileriyle uyumludur Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 

202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi 

5

* Çapraz Ölçekleme (Diagonal Scaling) 

Vertical + Horizontal 

Önce güç artı r → sonra sunucu ekle 

7. Ölçekleme Yöntemleri  

> •

Manuel Ölçekleme  

> •

Planlı Ölçekleme  

> •

Otomatik Ölçekleme (Auto -scaling) 

Not: Otomatik ölçekleme, genellikle CPU kullanımı , istek sayısı veya gecikme metriklerine dayanır. 

8. Yedeklilik (Redundancy) 

8.1 Yedeklilik Kavramı 

Yedeklilik , sistem bileşenlerinin ve verilerin birden fazla kopyasının tutulmasıdır. 

Amaç:  

> •

Veri kaybını önlemek  

> •

Sürekliliği sağlamak (High Availability) 

Şekil 4 – Yedekli Bulut Mimar i Yapı ları Kocaeli Üniversitesi Fen Bilimleri Enstitüsü Bilişim Sistemleri Mühendisliği ABD 

202 5-202 6 Güz Dönemi BTM535: Şebeke ve Bulut Hesaplama (Grid and Cloud Computing) Dersi 

6

8.2 Yedekliliğin Faydaları  

> •

Otomatik veri yedekleme  

> •

Her yerden erişim  

> •

SLA ile garanti edilen çalışma süresi  

> •

Felaket kurtarma (Disaster Recovery)