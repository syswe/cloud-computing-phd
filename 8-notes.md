# 8. Grid Hesaplamada Güvenlik - Ders Notları

## 8.1 Sanal Organizasyonlar (Virtual Organizations - VO)

**Tanım:** Kaynakları ve hizmetleri paylaşmak için oluşturulmuş, coğrafi olarak dağılmış grup. 

**Özellikler:**
- Kalıcı veya geçici olabilir
- Paylaşım kurallar ve politikalara tabidir
- Dinamik ve organizasyonlar arası yapı

**Zorluk:** Merkezi kontrol noktası olmaması → Her kaynak sağlayıcı risk değerlendirmesi yapmalı

## 8.2 Geleneksel Güvenlik Alanları

### 1. Kimlik Doğrulama (Authentication)

**Tanım:** Ağdaki bir varlığın kimliğini belirleme süreci

**Yöntemler:**
- Kullanıcı adı ve parola (basit)
- **Kerberos**:  Simetrik anahtar şifrelemesi
- **PKI (Public Key Infrastructure)**: Grid'de önemli teknoloji

**X.509 Sertifikaları:**
- Varlıkları tanımlayan güvenlik sistemi
- **CA (Certification Authority)** tarafından verilir
- Kullanıcılar farklı VO'larda farklı kimlik bilgileri kullanabilir

### 2. Yetkilendirme (Authorization)

**Tanım:** Bir varlığa atanan ayrıcalıkların doğrulanması

**Önemli:** Sadece kimlik doğrulama başarıyla gerçekleştirildikten sonra yapılır

**Yetkilendirme Teknikleri:**

| Teknik | Açıklama |
|--------|----------|
| **Globus Gridmap Dosyası** | Grid kullanıcıları ve yerel hesap adları listesi |
| **CAS (Community Authorization Service)** | Grid yetkilendirmesinin kolaylığını artırır |
| **VOMS (Virtual Organization Membership Service)** | VO'lar içinde yetkilendirme bilgilerinin yönetimi |

### 3. Gizlilik (Confidentiality)

**Tanım:** Hassas bilgilerin yetkisiz kişilerden saklanması

**Yaklaşım:** Veri şifreleme

**Hassas Veri Örnekleri:**
- Endüstriyel bilgiler
- Finansal bilgiler
- Tıbbi veriler

## 8.3 Mevcut Güvenlik Teknolojileri

### 1. PKI (Public Key Infrastructure)

**Amaç:** Genel/özel anahtar çifti ile güvenli iletişim

**Bileşenler:**
- **CA (Sertifika Yetkilisi)**: Güvenilir üçüncü taraf
- **Dijital Sertifika**:  Kullanıcıyı benzersiz şekilde tanımlar

**Güven Zinciri (Chain of Trust):**
- **En Alt**:  Son kullanıcılar (dijital sertifika)
- **Orta**: Bölgesel CA'lar
- **En Üst**: Kök CA'lar (Root CA)

### X.509 Dijital Sertifika Alanları:

| Alan | Açıklama |
|------|----------|
| **Sürüm** | X.509 versiyonu (1, 2, veya 3) |
| **Seri Numarası** | Benzersiz tanımlayıcı |
| **Algoritma Tanımlayıcı** | Kullanılan algoritmalar |
| **Sertifikayı Veren (Issuer)** | CA adı |
| **Geçerlilik (Validity)** | Geçerlilik süresi |
| **Konu (Subject)** | Sertifika sahibi |
| **Konu Açık Anahtar Bilgisi** | Açık anahtar |
| **Sertifika İmzası** | CA'nın imzası |

### 2. Kerberos

**Tanım:** MIT tarafından geliştirilen ağ kimlik doğrulama protokolü

**Özellik:** Simetrik anahtar şifrelemesi kullanır

**Temel Taraflar:**
1. **İstemci (Client)**
2. **Sunucu (Server)**
3. **KDC (Key Distribution Center)**:  Güvenilir aracı

**Kerberos Terimleri:**

| Terim | Açıklama |
|-------|----------|
| **Principal** | Kimliği doğrulanan varlık |
| **Verifier** | Kimliği doğrulayan varlık |
| **Kerberos Realm** | Yönetim alanı |
| **TGT (Ticket Granting Ticket)** | TGS'ye kimlik doğrulama için kullanılır |

**KDC Bileşenleri:**
- **AS (Authentication Server)**: TGT düzenler
- **TGS (Ticket Granting Server)**: Normal bilet sağlar

**Kerberos Özellikleri:**
- Tek Oturum Açma (Single Sign-On)
- Zaman damgaları ile mesaj sayısı azaltma
- Bölgeler arası kimlik doğrulama desteği

### 3. GSI (Grid Security Infrastructure)

**Tanım:** Grid'de güvenlik uygulaması için eksiksiz mimari

**Özel Güvenlik İhtiyaçları:**

| İhtiyaç | Açıklama |
|---------|----------|
| **Tek Oturum Açma** | Bir kez kimlik doğrulama, sonra erişim |
| **Ayrıcalıkların Devredilmesi** | Proxy sertifikası ile ayrıcalık devri |
| **Etki Alanları Arası Güvenlik** | Farklı organizasyonlar arası etkileşim |
| **Güvenli İletişim** | TLS ile mesaj alışverişi |
| **Kimlik Doğrulama ve Yetkilendirme** | Güvenli ve ölçeklenebilir |
| **Tek Tip Kimlik Bilgileri** | X.509 sertifika formatı |

## 8.4 Gelişen Güvenlik Teknolojileri

### 1. WS-Security

**Tanım:** SOAP mesajlarına güvenlik özellikleri sağlayan standart

**Amaç:** İleti düzeyinde güvenlik (taşıma düzeyinden farklı)

**Desteklenen Protokoller:** PKI, Kerberos, SSL

### 2. OGSA Güvenliği

**OGSA (Open Grid Services Architecture):** Web servislerine dayalı Grid mimarisi

**Temel Özellikler:**
- Globus Toolkit ve web hizmetleri üzerine kurulu
- Grid hizmetleri:  Durum yönetimi ve yaşam döngüsü desteği

**Grid Servisi Özellikleri:**
- **Durum (State)**: Web hizmetleri durumsuz, Grid hizmetleri durumlu
- **Hizmet Verileri**:  WSDL arayüzüne yapılandırılmış veri ekleme

**Kimlik Belirleyiciler:**

| Belirleyici | Özellik |
|-------------|---------|
| **GSH (Grid Service Handle)** | Değişmez, benzersiz tanımlayıcı |
| **GSR (Grid Service Reference)** | Değişebilir, protokol ve adres bilgisi |