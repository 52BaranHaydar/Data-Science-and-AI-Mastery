# 🔍 Keşifçi Veri Analizi (Exploratory Data Analysis - EDA)

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge)](https://seaborn.pydata.org/)

Veri biliminde modelleme öncesinde verinin yapısını, dağılımını, anomalilerini ve değişkenler arası ilişkilerini ortaya çıkarmak için uygulanan kapsamlı analitik çalışmalar.

---

## 📚 Projeler ve Vaka Analizleri

| Notebook | Veri Seti | Kapsam & Yöntemler |
| :--- | :--- | :--- |
| **[`flight_price.ipynb`](flight_price.ipynb)** | **Uçuş Fiyat Tahmini (`flight_price.xlsx`)** | Tarih ve saat mühendisliği (`Date_of_Journey`, `Dep_Time`), Uçuş süresi ayrıştırma, Aktarma sayısı (`Total_Stops`) ordinal kodlama, One-Hot & Target Mean Encoding |
| **[`../eda-continue/wine_quality.ipynb`](../eda-continue/wine_quality.ipynb)** | **Kırmızı Şarap Kalitesi (`winequality-red.csv`)** | Eksik/tekrar eden veri temizliği, Korelasyon ısı haritası (`sns.heatmap`), Alkol/pH/Sitrik asit ilişkileri, SMOTE ile sınıf dengeleme |
| **[`../eda-continue/google_playstore.ipynb`](../eda-continue/google_playstore.ipynb)** | **Google Play Store Analizi** | Mobil uygulama kategorileri, indirme ve puanlama metrikleri, temizlenmiş veri analizi |
| **[`questions.ipynb`](questions.ipynb)** | **Pratik Soru-Cevap Laboratuvarı** | Metin sütun uzunlukları, One-Hot dönüşümleri ve pratik mülakat alıştırmaları |

---

## 🛠️ Kurulum ve Çalıştırma

```bash
pip install -r requirements.txt
jupyter notebook
```
