# Project: Hotel Management System & Stay Prediction

Bu proje, bir butik otelin hem operasyonel yönetimini hem de veri odaklı müşteri analizini kapsayan iki aşamalı bir çalışmadır. Nesne yönelimli programlama (OOP) prensipleriyle geliştirilen yönetim modülü, gerçek dünya verileriyle eğitilmiş makine öğrenmesi modelleriyle desteklenmiştir.

## Proje İçeriği ve Yetenekler

### 1. Operasyonel Yönetim Sistemi (OOP):

*Personel ve Oda Yönetimi:* Müdür, Resepsiyonist, Housekeeping gibi farklı roller için kalıtım (inheritance) yapısı kullanılarak personel takibi, maaş hesaplamaları ve çalışma gün sayısı takibi yapılmaktadır.

*Rezervasyon ve Check-in/out:* Misafirlerin konaklama türüne (Standart, Suit, Delux) ve aldıkları ek hizmetlere (WiFi, Özel Araç vb.) göre dinamik ücret hesaplama sistemi kurgulanmıştır.

*Gerçek Zamanlı Durum Takibi:* Oteldeki anlık boş oda sayısı ve personel maliyetleri gibi kritik veriler sistem üzerinden raporlanabilmektedir.

### 2. Veri Analizi ve Konaklama Tahmini (Prediction): Otel misafirlerinin demografik bilgilerini (gelir, eğitim, aile durumu vb.) kullanarak müşteri davranışlarını anlamlandırmayı hedefler:

*Oda Tipi Önerisi:* DecisionTreeClassifier kullanılarak, yeni bir misafirin profilinden (gelir, yaş, çocuk sayısı) yola çıkarak hangi oda tipini tercih edeceği tahmin edilir.

*Konaklama Süresi Analizi:* Misafirlerin gelir düzeyi ile kalacakları gün sayısı arasındaki ilişki Lineer, Polinomsal ve Random Forest regresyon modelleriyle analiz edilmiştir.

*Bulgu:* Gelir ile konaklama süresi arasında zayıf bir korelasyon (0.34) saptanmış, bu durum konaklama süresinin sadece bütçeye değil, diğer yaşam tarzı faktörlerine de bağlı olduğunu göstermiştir.

Kullanılan Teknolojiler

*Python (OOP):* Sınıf yapıları, kalıtım ve tarih-saat yönetimi (datetime).

*Veri Analizi:* Pandas, NumPy, Matplotlib.

*Makine Öğrenmesi:* Scikit-learn (Decision Tree, Linear/Polynomial/Random Forest Regression).

## İletişim

| Kanal | Link |
| :--- | :--- |
| **LinkedIn** | [Profilime Git](https://www.linkedin.com/in/burcuuluag/) |