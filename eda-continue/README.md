# 📊 Keşifçi Veri Analizi - Bölüm 2 (EDA Deep Dive)

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge)](https://seaborn.pydata.org/)

Kırmızı şarap kalitesi ve mobil uygulama pazarı veri setleri üzerinde çok değişkenli istatistiksel analizler, veri temizliği, korelasyon çalışmaları ve sınıf dengeleme.

---

## 📚 Notebook Serisi

| Notebook | Veri Seti | Temel Yöntem ve Çıkarımlar |
| :--- | :--- | :--- |
| **[`wine_quality.ipynb`](wine_quality.ipynb)** | **Kırmızı Şarap Kalitesi (`winequality-red.csv`)** | Mükerrer gözlem temizliği (`drop_duplicates`), Korelasyon matrisi ve ısı haritası, Alkol ve Sitrik Asit'in kalite puanına etkisi, **SMOTE** ile nadir kalite sınıflarını dengeleme |
| **[`google_playstore.ipynb`](google_playstore.ipynb)** | **Google Play Store (`google_playstore_cleaned.csv`)** | Uygulama puanları, yorum sayıları, indirme hacimleri ve kategori dağılımlarının analizi |

---

## 🛠️ Kurulum

```bash
pip install pandas numpy matplotlib seaborn imbalanced-learn
jupyter notebook
```
