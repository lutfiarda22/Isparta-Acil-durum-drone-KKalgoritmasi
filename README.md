# Isparta Acil Durum Drone Rota Optimizasyonu (ACO)

Bu projede, **Isparta il merkezinde** bulunan afet ve acil durum toplanma alanları arasında,
**en kısa drone rotasını** bulmak amacıyla **Karınca Kolonisi Optimizasyonu (ACO)** algoritması kullanılmıştır.

Uygulama, **Streamlit** tabanlı bir arayüz üzerinden çalışmakta ve **Google Maps API** ile elde edilen gerçek mesafe verileriyle optimizasyon gerçekleştirmektedir.

---

## Proje Amacı

* Acil durumlarda bir dronun, belirlenen toplanma alanlarını **en kısa mesafe ile** dolaşmasını sağlamak
* Karınca Kolonisi Optimizasyonu (ACO) algoritmasının **gerçek verilerle** uygulanmasını göstermek
* Sonuçları **harita**, **grafik** ve **tablo** şeklinde görselleştirmek

---

## Kullanılan Yöntem

### Karınca Kolonisi Optimizasyonu (ACO)

ACO, karıncaların doğadaki feromon bırakma davranışından esinlenmiş bir sezgisel optimizasyon algoritmasıdır.

Bu projede:

* Her karınca bir rota üretir
* Kısa rotalar daha fazla feromon bırakır
* Feromonlar zamanla buharlaşır
* İterasyonlar ilerledikçe en kısa rota yakınsaması sağlanır

---

## 🛠️ Kullanılan Teknolojiler

* **Python**
* **Streamlit** (arayüz)
* **Google Maps Distance Matrix API**
* **Folium** (harita görselleştirme)
* **Pandas**
* **Matplotlib**

---

## 📂 Proje Yapısı

```text
.
├── main.py
├── data
│   └── coordinates.py
├── core
│   ├── ant_algorithm.py
│   ├── matrix_utils.py
│   └── visual
│       ├── map_plotting.py
│       └── plotting.py
├── requirements.txt
└── README.md
```

---

## ⚙️ Kurulum ve Çalıştırma
---
Anaconda prompt kullanarak yapınız.
---
### 1️⃣ Gerekli kütüphaneleri yükleyin

```bash
pip install -r requirements.txt
```

### 2️⃣ Google Maps API Key ayarlayın

`.streamlit/secrets.toml` dosyası oluşturup aşağıdaki formatta ekleyin:

```toml
GOOGLE_MAPS_API_KEY = "API_KEYİNİZ"
```

### 3️⃣ Uygulamayı çalıştırın

```bash
streamlit run main.py
```

---

## 🖥️ Uygulama Özellikleri

* Parametre ayarlanabilir ACO algoritması
* En iyi rota mesafesi ve iyileşme oranı
* Yakınsama (convergence) grafiği
* Detaylı rota tablosu
* Harita üzerinde kuş uçuşu drone rotası
* Temalı (lacivert–sarı) kullanıcı arayüzü

---

## 📊 Çıktılar

* **En kısa rota**
* **Toplam mesafe (km)**
* **İyileşme oranı (%)**
* **Harita üzerinde rota**
* **Adım adım mesafe tablosu**

## Öğrenci Bilgileri

**Lütfi Arda Karaoğlu**
**2212721038**
Bilgisayar Mühendisliği Öğrencisi
Isparta Uygulamalı Bilimler Üniversitesi
