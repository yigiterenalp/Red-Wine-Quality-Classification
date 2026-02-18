\# 🍷 Red Wine Quality Prediction: A Machine Learning Approach



\[!\[Python Version](https://img.shields.io/badge/python-3.10-blue.svg)](https://www.python.org/)

\[!\[Scikit-Learn](https://img.shields.io/badge/scikit--learn-latest-orange.svg)](https://scikit-learn.org/)

\[!\[License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)



Bu proje, Portekiz'in "Vinho Verde" şaraplarının fizikokimyasal özelliklerini analiz ederek, şarap kalitesini sınıflandırmak amacıyla geliştirilmiştir. Veri bilimi yaşam döngüsünün tüm aşamalarını (EDA, Preprocessing, Hyperparameter Tuning) içermektedir.







\## 🎯 Proje Hedefi

Veri setindeki 1-10 arası kalite puanlarını, daha dengeli bir modelleme için \*\*Binary Classification\*\* (0: Standart, 1: İyi) problemine dönüştürdük. Amacımız, kimyasal bileşenlere bakarak bir şarabın "İyi" (6 ve üzeri puan) olup olmadığını tahmin etmektir.



\## 📊 Veri Analizi ve Bulgular (EDA)

Yapılan korelasyon analizleri sonucunda şunlar tespit edilmiştir:

\* \*\*Alkol:\*\* Kalite ile en güçlü pozitif korelasyona (+0.43) sahip değişim.

\* \*\*Volatile Acidity (Uçucu Asitlik):\*\* Sirkeleşmeyi temsil ettiği için kalite ile en güçlü negatif korelasyona (-0.32) sahiptir.

\* \*\*Outlier Yönetimi:\*\* IQR (Interquartile Range) yöntemi kullanılarak uç değerler temizlenmiş, modelin genel örüntüleri öğrenmesi sağlanmıştır.







\## 🛠️ Teknik İş Akışı

1\.  \*\*Exploratory Data Analysis (EDA):\*\* Seaborn ve Matplotlib ile veri görselleştirme.

2\.  \*\*Preprocessing:\*\* \* IQR Filtreleme ile gürültü azaltma (%25 veri temizliği).

&nbsp;   \* `StandardScaler` ile özellik ölçeklendirme.

3\.  \*\*Modeling:\*\* `RandomForestClassifier` algoritması seçildi.

4\.  \*\*Optimization:\*\* `GridSearchCV` kullanılarak en iyi parametreler belirlendi.



\## 📈 Model Performansı

Optimizasyon sonrası elde edilen sonuçlar:



| Metric | Score |

| :--- | :--- |

| \*\*Accuracy\*\* | \*\*%81.59\*\* |

| \*\*Precision (İyi Şarap)\*\* | \*\*%83\*\* |

| \*\*Recall (İyi Şarap)\*\* | \*\*%77\*\* |







\## 📂 Dosya Yapısı

```text

├── data/               # Ham veri seti (CSV)

├── models/             # Eğitilmiş model (.pkl) ve Scaler nesnesi

├── notebooks/          # Adım adım analiz içeren Jupyter Notebook

├── .gitignore          # Gereksiz dosyaların filtrelenmesi

├── README.md           # Proje dokümantasyonu

└── requirements.txt    # Gerekli kütüphanelerin listesi



Başlangıç

Projeyi yerel bilgisayarınızda çalıştırmak için:



Depoyu klonlayın:



Bash



git clone \[https://github.com/yigiterenalp/Red-Wine-Quality-Classification.git](https://github.com/yigiterenalp/Red-Wine-Quality-Classification.git)

Gerekli paketleri yükleyin:



Bash



pip install -r requirements.txt

Notebook'u çalıştırın:



Bash



jupyter notebook notebooks/Wine\_Quality\_Analysis.ipynb

