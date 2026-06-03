# 🎧 Music Streaming User Analysis

## 📌 Proje Hakkında

Bu proje, bir müzik streaming platformuna ait kullanıcı verileri üzerinde veri analizi çalışmaları gerçekleştirmek amacıyla hazırlanmıştır.

Proje kapsamında Excel, SQL ve Python kullanılarak kullanıcı davranışları incelenmiş, kullanıcı segmentleri karşılaştırılmış, churn (müşteri kaybı) davranışı analiz edilmiş ve elde edilen bulgular iş içgörülerine dönüştürülmüştür.

Bu çalışma, veri analizi sürecinde kullanılan temel araçların gerçek bir senaryo üzerinde uygulanmasını göstermektedir.

---

## 🎯 Proje Amaçları

Bu proje kapsamında aşağıdaki sorulara cevap aranmıştır:

- Premium kullanıcılar platformu daha aktif kullanıyor mu?
- Churn eden kullanıcıların davranışları nasıl farklılaşıyor?
- Kullanıcıların dinleme alışkanlıkları ülkelere göre değişiyor mu?
- Cihaz tipi kullanıcı davranışlarını etkiliyor mu?
- Hangi müzik türlerinde skip rate daha yüksek?
- Veri setinde eksik veri veya aykırı değer bulunuyor mu?

---

## 🗂️ Veri Seti

Veri seti, bir müzik streaming platformundaki kullanıcı aktivitelerini temsil etmektedir.

### Veri Seti Kolonları

| Kolon | Açıklama |
|---------|---------|
| user_id | Kullanıcı kimliği |
| age | Kullanıcı yaşı |
| country | Kullanıcının ülkesi |
| subscription_type | Free veya Premium abonelik |
| device | Kullanılan cihaz |
| daily_minutes | Günlük dinleme süresi |
| favorite_genre | Favori müzik türü |
| skip_rate | Şarkı geçme oranı |
| ads_clicked | Reklam tıklama durumu |
| churned | Kullanıcının platformu bırakma durumu |

---

## 🛠️ Kullanılan Teknolojiler

- Excel
- SQL
- Python
- Pandas
- Matplotlib
- Google Colab
- GitHub

---

## 📌 Yapılan Analizler

### SQL Analizleri

- Veri keşfi (Data Exploration)
- Filtreleme ve sıralama işlemleri
- COUNT, SUM ve AVG analizleri
- GROUP BY analizleri
- Churn analizi
- Kullanıcı segmentasyonu
- Veri kalitesi kontrolleri

### Python Analizleri

- Veri temizleme
- Eksik veri analizi
- Aykırı değer (Outlier) analizi
- Keşifsel Veri Analizi (EDA)
- Veri görselleştirme

### Excel Analizleri

- Veri inceleme
- Veri doğrulama
- Temel KPI hesaplamaları

---

# 📈 Analiz Sonuçları

## 1. Premium Kullanıcılar Daha Aktif

Abonelik tipine göre yapılan analiz sonucunda Premium kullanıcıların platform üzerinde daha fazla zaman geçirdiği görülmüştür.

| Abonelik Tipi | Ortalama Günlük Dinleme Süresi |
|---------------|-------------------------------|
| Premium | 135.7 dakika |
| Free | 45.3 dakika |

Bu sonuç, Premium kullanıcıların platformla daha yüksek etkileşim kurduğunu göstermektedir.

---

## 2. Skip Rate ve Churn Arasında Güçlü Bir İlişki Bulundu

Churn eden kullanıcıların şarkı geçme oranlarının önemli ölçüde daha yüksek olduğu tespit edilmiştir.

| Churn Durumu | Ortalama Skip Rate |
|-------------|-------------------|
| Aktif Kullanıcı | %13.6 |
| Churn Eden Kullanıcı | %53.4 |

Bu bulgu, skip rate değerinin churn tahmini için kullanılabilecek önemli bir gösterge olduğunu göstermektedir.

---

## 3. Ülkelere Göre Kullanıcı Davranışları Farklılaşıyor

Ülkeler bazında yapılan analizde Almanya, Fransa ve İngiltere'deki kullanıcıların platformda daha uzun süre vakit geçirdiği görülmüştür.

| Ülke | Ortalama Günlük Dinleme Süresi |
|-------|------------------------------|
| Almanya | 131.9 dakika |
| Fransa | 129.5 dakika |
| İngiltere | 125.2 dakika |
| Türkiye | 49.8 dakika |

---

## 4. Müzik Türleri Arasında Davranış Farklılıkları Bulundu

Skip rate değerleri müzik türlerine göre incelendiğinde Hip-Hop ve Pop türlerinde daha yüksek oranlar gözlemlenmiştir.

| Tür | Ortalama Skip Rate |
|------|------------------|
| Hip-Hop | %56.9 |
| Pop | %47.2 |
| Rock | %16.8 |
| Jazz | %10.3 |
| Classical | %9.1 |

Bu durum kullanıcı tercihleri ve öneri sistemleri açısından değerlendirilebilir.

---

## 5. Veri Kalitesi Bulguları

Veri kalitesi kontrolleri sonucunda:

- 2 adet eksik değer tespit edilmiştir.
- 1 adet aykırı gözlem (outlier) bulunmuştur.
- Bir kullanıcının günlük dinleme süresi 400 dakika olarak kaydedilmiştir.

Analiz öncesinde bu tür kayıtların incelenmesi sağlıklı sonuçlar elde etmek açısından önemlidir.

---

# 💡 İş İçgörüleri ve Öneriler

Analiz sonuçlarına göre aşağıdaki öneriler geliştirilebilir:

- Yüksek skip rate gösteren kullanıcılar churn riski açısından yakından takip edilebilir.
- Free kullanıcıları Premium üyeliğe yönlendirecek kampanyalar oluşturulabilir.
- Hip-Hop ve Pop kategorilerinde öneri algoritmaları geliştirilebilir.
- Churn tahmini modellerinde skip rate önemli bir özellik olarak kullanılabilir.
- Kullanıcı etkileşimini artırmak için cihaz bazlı deneyim analizleri yapılabilir.

---

## 📁 Proje Dosya Yapısı

text music-streaming-analysis/ │ ├── dataset.csv ├── queries.sql ├── python_analysis.ipynb ├── analysis.md └── README.md 

---

## 🚀 Sonuç

Bu proje, Excel, SQL ve Python kullanılarak uçtan uca bir veri analizi sürecinin nasıl gerçekleştirilebileceğini göstermektedir.

Veri temizleme, sorgulama, analiz ve görselleştirme adımları tamamlanarak kullanıcı davranışlarına yönelik anlamlı iş içgörüleri elde edilmiştir.

Proje, veri analisti rolünde kullanılan temel tekniklerin uygulamalı bir örneğini sunmaktadır.

---

👩‍💻 Bu proje, Yıldız Kariyerim Data Analyst Bootcamp kapsamında hazırlanmışt
