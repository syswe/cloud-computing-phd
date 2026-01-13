# Şebeke ve Bulut Bilişim - Doktora Ders Notları

[![Kocaeli Üniversitesi](https://img.shields.io/badge/Kocaeli%20Üniversitesi-Grid%20%26%20Cloud%20Computing-blue)](https://www.kocaeli.edu.tr/)
[![Lisans](https://img.shields.io/badge/License-Educational-green.svg)](LICENSE)
 
> **Şebeke ve Bulut Hesaplama (Grid and Cloud Computing)**

---

## 📋 İçindekiler

- [Hakkında](#-hakkında)
- [Ders İçeriği](#-ders-içeriği)
- [Dosya Yapısı](#-dosya-yapısı)
- [Konu Başlıkları](#-konu-başlıkları)
- [Nasıl Kullanılır](#-nasıl-kullanılır)
- [Kaynaklar](#-kaynaklar)
- [Katkıda Bulunma](#-katkıda-bulunma)

---

## 🎯 Hakkında

Bu repo, **Şebeke ve Bulut Hesaplama** doktora dersi için hazırlanmış kapsamlı ders notları ve çoktan seçmeli sınav sorularını içermektedir. 

### Amaç
- Grid Computing (Şebeke Hesaplama) temellerini anlamak
- Bulut Bilişim kavramlarını ve mimarisini öğrenmek
- NIST standartlarını ve referans mimarisini kavramak
- Doktora final sınavına hazırlanmak

---

## 📖 Ders İçeriği

### Haftalık Program

| Hafta | Konu |
|-------|------|
| 1 | Şebekeye (Grid) Giriş |
| 2 | Grid Hesaplama Altyapıları |
| 3 | Hizmet Odaklı Mimari (SOA) |
| 4 | Grid Mimarisi, Standartlar ve Elemanlar |
| 5 | OGSA'ya Giriş, İşlevsellik ve Grid Servis Modelleri |
| 6 | Açık Kaynaklı Grid Ara Yazılım Paketleri |
| 7 | Grid Konfigürasyonu ve Model Kullanımı |
| 8 | Grid Güvenlik Ortamı için Güven Modelleri |
| 9 | Kimlik Doğrulama ve Yetkilendirme Yöntemleri |
| 10 | Grid Güvenlik Altyapısı (GSI) |
| 11 | Bulut Bilişim Genel Bakış |
| 12 | Bulut İçgörüleri |
| 13 | Bulut Mimarisi:  Katmanlar ve Modeller |
| 14 | Bulutta Kimlik Doğrulama ve Yetkilendirme |
| 15 | Grid ve Bulut Bilişim Karşılaştırması |

---

## 📁 Dosya Yapısı

```
cloud-computing-phd/
│
├── 📄 README.md                    # Bu dosya
│
├── 📂 ders-notlari/                # Ders Notları
│   ├── 1-notes.md                  # Grid Computing
│   ├── 2-notes.md                  # Şebeke Hesaplamaya Giriş
│   ├── 3-notes.md                  # OGSA ve WSRF
│   ├── 4-notes.md                  # Bilgi Hizmetleri (MDS)
│   ├── 5-notes.md                  # Veri Yönetimi
│   ├── 6-notes.md                  # Grid Çizelgeleme ve Bilgi Hizmetleri
│   ├── 7-notes.md                  # Grid Çizelgeleme ve Kaynak Yönetimi
│   ├── 8-notes.md                  # Grid Hesaplamada Güvenlik
│   ├── 9-notes.md                  # Şebeke Ara Katman Yazılımı
│   ├── 10-notes.md                 # Bulut Bilişimin NIST Tanımı
│   ├── 11-notes.md                 # Bulut Bilişim Referans Mimarisi
│   ├── 12-notes.md                 # Uygulama Alanları ve Ölçeklenebilirlik
│   └── 13-notes.md                 # Grid vs Cloud Karşılaştırması
│
├── 📂 sinav-sorulari/              # Çoktan Seçmeli Sorular
│   ├── 1-exam.md                   # Grid Computing Soruları
│   ├── 2-exam.md                   # Şebeke Hesaplamaya Giriş Soruları
│   ├── 3-exam.md                   # OGSA ve WSRF Soruları
│   ├── 4-exam.md                   # Bilgi Hizmetleri Soruları
│   ├── 5-exam.md                   # Veri Yönetimi Soruları
│   ├── 6-exam.md                   # Çizelgeleme ve Bilgi Hizmetleri Soruları
│   ├── 7-exam.md                   # Çizelgeleme ve Kaynak Yönetimi Soruları
│   ├── 8-exam.md                   # Güvenlik Soruları
│   ├── 9-exam.md                   # Ara Katman Yazılımı Soruları
│   ├── 10-exam.md                  # NIST Tanımı Soruları
│   ├── 11-exam.md                  # Referans Mimarisi Soruları
│   ├── 12-exam.md                  # Ölçeklenebilirlik Soruları
│   ├── 13-exam.md                  # Karşılaştırma Soruları
│   └── genel-tekrar-exam.md        # Kapsamlı Final Sınavı (30 Soru)
│
└── 📂 kaynaklar/                   # Orijinal Ders Materyalleri
    ├── 1-Grid Computing. md
    ├── 2-Introduction to Grid Computing.md
    ├── 3-OGSA and WSRF.md
    └── ... 
```

---

## 📚 Konu Başlıkları

### 🔷 Bölüm 1: Grid Computing (Şebeke Hesaplama)

| Konu | Açıklama |
|------|----------|
| **Grid Tanımı** | Dağıtılmış bilgi işlem mimarisi |
| **Çalışma Prensibi** | Kontrol düğümü, sağlayıcı, kullanıcı |
| **Ara Yazılım** | Middleware kavramı ve görevleri |
| **Grid Mimarisi** | Fabric, Connectivity, Resource, Collective, Application katmanları |
| **Grid Türleri** | Hesaplama, Veri, Uygulama, Servis şebekeleri |

### 🔷 Bölüm 2: Standartlar ve Mimariler

| Konu | Açıklama |
|------|----------|
| **GGF** | Global Grid Forum standartları |
| **OGSA** | Open Grid Services Architecture |
| **WSRF** | Web Services Resource Framework |
| **Web Servisleri** | SOAP, WSDL, UDDI |

### 🔷 Bölüm 3: Bilgi Hizmetleri ve Veri Yönetimi

| Konu | Açıklama |
|------|----------|
| **MDS** | Monitoring and Discovery Services |
| **GRIS/GIIS** | Grid Resource/Index Information Service |
| **Meta Veri** | Veri hakkında veri yönetimi |
| **Replikasyon** | Veri çoğaltma ve senkronizasyon |

### 🔷 Bölüm 4: Çizelgeleme ve Kaynak Yönetimi

| Konu | Açıklama |
|------|----------|
| **Çizelgeleme Paradigmaları** | Merkezi, Dağıtılmış, Hiyerarşik |
| **ETC Matrisi** | Expected Time to Compute |
| **Algoritmalar** | Min-Min, Max-Min, Genetik Algoritma |
| **Hata Toleransı** | Fault tolerance mekanizmaları |

### 🔷 Bölüm 5: Güvenlik

| Konu | Açıklama |
|------|----------|
| **Kimlik Doğrulama** | Authentication mekanizmaları |
| **Yetkilendirme** | Authorization ve VOMS |
| **PKI** | Public Key Infrastructure |
| **Kerberos** | Ağ kimlik doğrulama protokolü |
| **GSI** | Grid Security Infrastructure |

### 🔷 Bölüm 6: Bulut Bilişim

| Konu | Açıklama |
|------|----------|
| **NIST Tanımı** | 5 temel özellik |
| **Hizmet Modelleri** | SaaS, PaaS, IaaS |
| **Dağıtım Modelleri** | Özel, Genel, Topluluk, Hibrit |
| **Referans Mimarisi** | 5 temel aktör |
| **Ölçeklenebilirlik** | Dikey, Yatay, Çapraz |

---

## 🚀 Nasıl Kullanılır

### Ders Notlarını Okuma

1. `ders-notlari/` klasöründeki markdown dosyalarını sırayla okuyun
2. Her konunun sonundaki özet tablolarına dikkat edin
3. Önemli terimleri ve tanımları not alın

### Sınava Hazırlanma

1. `sinav-sorulari/` klasöründeki soruları çözün
2. Yanlış yaptığınız soruları işaretleyin
3. İlgili ders notuna geri dönüp tekrar edin
4. `genel-tekrar-exam. md` ile kendinizi test edin

### Önerilen Çalışma Planı

```
📅 1. Hafta: Konuları oku (1-notes.md → 5-notes.md)
📅 2. Hafta: Konuları oku (6-notes.md → 10-notes.md)
📅 3. Hafta: Konuları oku (11-notes.md → 13-notes. md)
📅 4. Hafta: Tüm sınav sorularını çöz
📅 5. Hafta: Genel tekrar ve zayıf noktaları güçlendir
```

---

## 📊 Önemli Kavramlar Özeti

### Grid Computing Temel Kavramları

| Kavram | Tanım |
|--------|-------|
| **Grid Fabric** | Tüm kaynakların bütünü |
| **Middleware** | Ara katman yazılımı |
| **VO (Virtual Organization)** | Sanal Organizasyon |
| **Makespan** | Tüm görevlerin tamamlanma süresi |
| **GSI** | Grid Security Infrastructure |

### Bulut Bilişim Temel Kavramları

| Kavram | Tanım |
|--------|-------|
| **On-Demand Self-Service** | İsteğe bağlı self-servis |
| **Resource Pooling** | Kaynak havuzu |
| **Rapid Elasticity** | Hızlı esneklik |
| **Measured Service** | Ölçülen hizmet |
| **Multi-Tenant** | Çok kiracılı mimari |

### Grid vs Cloud

| Özellik | Grid | Cloud |
|---------|------|-------|
| **Yönetim** | Merkeziyetsiz | Merkezi |
| **Ödeme** | Ücretsiz | Pay-as-you-go |
| **Mimari** | Dağıtılmış | İstemci-sunucu |
| **Ölçeklenebilirlik** | Normal | Yüksek |

---

## 📖 Kaynaklar

### Ana Kaynak
- **Kitap:** Kai Hwang, Geoffrey C. Fox, Jack J. Dongarra - *"Distributed and Cloud Computing:  Clusters, Grids, Clouds and the Future of Internet"*, Morgan Kaufman Publisher

### Ek Kaynaklar
- NIST Cloud Computing Reference Architecture (SP 500-292)
- Globus Toolkit Documentation
- Open Grid Services Architecture (OGSA) Specification

### Faydalı Linkler
- [NIST Cloud Computing](https://www.nist.gov/programs-projects/nist-cloud-computing-program-nccp)
- [Globus Project](https://www.globus.org/)
- [Open Grid Forum](https://www.ogf.org/)