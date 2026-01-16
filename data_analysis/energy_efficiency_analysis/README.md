# Energy Efficiency: Predictive Analysis of Building Heating Loads

Bu proje, UCI Machine Learning Repository'de bulunan "Energy Efficiency" veri setini kullanarak, binaların çeşitli mimari özelliklerine göre **Isıtma Yükünü (Heating Load)** tahmin etmeyi amaçlar. Çalışma kapsamında regresyon modelleri hiperparametre optimizasyonu ile eğitilmiş ve performansları karşılaştırılmıştır.


## Veri Seti Hakkında
Veri seti, binaların enerji performansını etkileyen 8 farklı mimari parametreyi (Nispi Kompaktlık, Yüzey Alanı, Duvar Alanı, Çatı Alanı, Genel Yükseklik, Yön, Camlama Alanı, Camlama Alanı Dağılımı) içermektedir.

**Hedef Değişken:** Heating Load (Isıtma Yükü - kWh/m²)

## Temel Bulgular ve Analiz Sonuçları (Findings)

Yapılan kapsamlı analizler ve modelleme süreçleri sonucunda elde edilen veriler şu kritik bulguları ortaya koymuştur:

### 1. Model Performans Karşılaştırması
Eğitilen modeller arasında **Polynomial Regression**, karmaşık ilişkileri yakalama konusunda en başarılı model olmuştur.

| Algoritma | MAE (Hata) | RMSE | R² (Başarı Skoru) |
| :--- | :--- | :--- | :--- |
| **Polynomial Regression (Degree 2)** | **0.5367** | **0.7341** | **%99.48** |
| **Decision Tree** | 0.6542 | 1.0520 | %98.92 |
| **Support Vector Machine (SVR)** | 0.7146 | 1.1651 | %98.69 |
| **Ridge Regression** | 1.3771 | 1.9458 | %96.36 |
| **Lasso Regression** | 1.5226 | 2.1079 | %95.73 |

### 2. Doğrusal Olmayan (Non-Linear) İlişkilerin Keşfi

* **Karmaşıklık Etkisi:** Basit doğrusal modeller (Lasso/Ridge) yaklaşık %96 başarıda kalırken, özniteliklerin karesel kombinasyonlarını içeren **Polynomial Regression** başarısı %99'un üzerine çıkmıştır. Bu, bina yüksekliği ile yüzey alanı gibi değişkenler arasında ısıtma yükünü etkileyen doğrusal olmayan etkileşimler olduğunu kanıtlamaktadır.

* **Hata Dağılımı:** Polynomial modelin RMSE değerinin Ridge regresyonuna göre %60 daha düşük olması, modelin uç değerlerdeki (outliers) tahmin başarısının çok daha stabil olduğunu göstermektedir.

### 3. Öznitelik Önem Derecesi ve Düzenlileştirme

* **Lasso Analizi:** Lasso regresyonu sırasında bazı katsayıların sıfıra yaklaşması, binanın yönü (Orientation) gibi bazı kategorik değişkenlerin ısıtma yükü üzerinde "Camlama Alanı" (Glazing Area) kadar baskın bir etkisi olmadığını ortaya koymuştur.

* **SVR Optimizasyonu:** RBF çekirdeği (kernel) kullanılan SVM modelinde en iyi sonucun yüksek bir `C` parametresinde (C=10) alınması, verideki gürültünün düşük olduğunu ve modelin sınır değerlere odaklanarak daha hassas tahminler yapabildiğini göstermiştir.

## Kullanılan Teknolojiler

* **Python 3.11**
* **Scikit-learn:** Hiperparametre optimizasyonu (GridSearchCV) ve modelleme.
* **Pandas & NumPy:** Veri manipülasyonu ve RMSE hesaplamaları.
* **Matplotlib & Seaborn:** Bulguların görselleştirilmesi.

## İletişim

| Kanal | Link |
| :--- | :--- |
| **LinkedIn** | [Profilime Git](https://www.linkedin.com/in/burcuuluag/) |