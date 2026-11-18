# 🚀 Veri Bilimi, Doğal Dil İşleme ve Üretken Yapay Zeka Akademisi
### *End-to-End Data Science, NLP, LangChain & RAG Mastery*

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)](https://www.langchain.com/)
[![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6600?style=for-the-badge)](https://www.trychroma.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

Bu depo; ham verinin keşfinden istatistiksel hipotez testlerine, özellik mühendisliğinden doğal dil işlemeye, modern **LangChain** zincirlerinden kurumsal **RAG (Retrieval-Augmented Generation)** mimarilerine kadar uzanan kapsamlı, teorik ve pratik bir veri bilimi ve yapay zeka eğitim ve uygulama serisidir.

Tüm kodlar, matematiksel formüller ($LaTeX$), akış şemaları ve gerçek hayat projeleri **Baran Haydar** tarafından geliştirilmiştir.

---

## 🗺️ Öğrenim ve Uygulama Yol Haritası (Curriculum Roadmap)

```mermaid
flowchart TD
    subgraph MODÜL 1: VERİ KAŞİFLİĞİ & İSTATİSTİK
        A["1. Keşifçi Veri Analizi (EDA)"] --> B["2. Olasılık Dağılımları"]
        B --> C["3. Hipotez Testleri (Z, t, ANOVA, Ki-Kare)"]
    end

    subgraph MODÜL 2: ÖZNİTELİK & MODEL HAZIRLIĞI
        C --> D["4. Özellik Mühendisliği (Feature Engineering)"]
        D --> D1["Eksik Veri & Aykırı Değerler"]
        D --> D2["Kategorik Kodlama (OHE, Target Guided)"]
        D --> D3["Dengesiz Veri (SMOTE)"]
    end

    subgraph MODÜL 3: DOĞAL DİL İŞLEME (NLP)
        D3 --> E["5. NLP Temelleri (Tokenization, BoW, TF-IDF)"]
        E --> F["6. İleri NLP (Türkçe Morfoloji, SpaCy NER, BBC Sınıflandırma)"]
    end

    subgraph MODÜL 4: ÜRETKEN YAPAY ZEKA (GENAI & RAG)
        F --> G["7. LangChain (LCEL, Tool Calling, Pydantic Parsers)"]
        G --> H["8. RAG Sistemleri (Embeddings, ChromaDB, Ragas Değerlendirme)"]
    end

    style A fill:#e1f5fe,stroke:#0288d1,stroke-width:2px
    style D fill:#fff3e0,stroke:#f57c00,stroke-width:2px
    style E fill:#f3e5f5,stroke:#7b1fa2,stroke-width:2px
    style H fill:#e8f5e9,stroke:#388e3c,stroke-width:2px
```

---

## 📂 Modüller ve İçerik Fihristi

### 🔍 1. [Keşifçi Veri Analizi (EDA)](Explorative-data-analysis/README.md) & [Derinlemesine EDA](eda-continue/README.md)
* **Uçuş Fiyat Tahmini (`flight_price.ipynb`):** Tarih ve saat ayrıştırma, uçuş süresi hesaplama, aktarma sayısı ordinal haritalaması, One-Hot ve Target Guided Encoding.
* **Kırmızı Şarap Kalitesi (`wine_quality.ipynb`):** Korelasyon ısı haritası (`sns.heatmap`), fizikokimyasal özelliklerin kaliteye etkisi, SMOTE ile kalite sınıfı dengeleme.
* **Google Play Store Analizi (`google_playstore.ipynb`):** Mobil uygulama market metrikleri, indirme ve puan dağılımları.

### 📊 2. [İstatistik ve Olasılık Dağılımları](OlasılıkDağılımları/README.md)
* **Temel İstatistik:** Örnekleme yöntemleri, 5 Sayı Özeti, Çarpıklık (Skewness), Pearson Korelasyonu, PMF / PDF / CDF fonksiyonları.
* **Ayrık Dağılımlar:** Bernoulli, Binom, Poisson dağılımları ve simülasyonları.
* **Sürekli Dağılımlar:** Normal (Gauss), Standart Normal (Z-Skoru), Düzgün (Uniform), Log-Normal, Güç Yasası (Power Law) ve **Merkezi Limit Teoremi (CLT)**.

### 🧪 3. [Hipotez Testleri ve İstatistiksel Karar Alma](HipotezTestleri/README.md)
* **Parametrik Testler:** Tek Örneklem Z-Testi ($\sigma$ bilindiğinde), Student-t Testi (küçük ve pratik örneklemler).
* **Varyans Analizi (ANOVA):** Tek Yönlü ANOVA, $\alpha$-enflasyonu önleme, grup içi ve gruplar arası varyans, Post-Hoc **Tukey HSD** ikili karşılaştırmaları.
* **Non-Parametrik Testler:** Ki-Kare ($\chi^2$) Bağımsızlık Testi, Kontenjans Tabloları, beklenen frekanslar ve Cochran kuralları.

### ⚙️ 4. [Özellik Mühendisliği (Feature Engineering)](Feature-Engineering/README.md)
* **Eksik Veri (Missing Data):** MCAR, MAR, MNAR ayrımları; Ortalama, Medyan ve Mod ile doldurma (Imputation).
* **Aykırı Değerler (Outliers):** Çeyrekler Açıklığı ($IQR$), Alt ve Üst Çit sınırları, Boxplot görselleştirmeleri.
* **Kategorik Kodlama:** `LabelEncoder`, `OrdinalEncoder` (hiyerarşik sıra), `OneHotEncoder(drop='first')`, Target Guided Mean Encoding.
* **Dengesiz Sınıflar (Imbalanced Data):** Downsampling ve **SMOTE (Synthetic Minority Over-sampling Technique)** ile k-NN tabanlı sentetik veri üretimi.

### 🔤 5. [Doğal Dil İşleme Temelleri (NLP)](NLP/README.md)
* **Metin Ön İşleme:** Tokenization (Kelime, Cümle, Subword/BPE), Stopwords temizliği, Stemming (Porter, Snowball) vs Lemmatization (WordNet).
* **Türkçe Morfolojik Analiz:** Sondan eklemeli Türkçe için **Zeyrek** morfolojik analizörü.
* **Vektörleştirme Modelleri:** Kelime Çantası (Bag of Words / CountVectorizer), Terim-Belge Matrisi (DTM), TF-IDF matematiksel ağırlıklandırması.

### 🧠 6. [İleri NLP ve Metin Madenciliği](IleriNLP/README.md)
* **Varlık Tanıma (NER):** SpaCy `en_core_web_sm` boru hattı, `displaCy` varlık görselleştirme, `Matcher` ile özel kalıp tanıma.
* **Duygu Analizi (Sentiment Analysis):** Sözlük tabanlı (Lexicon/VADER) vs Makine Öğrenmesi (TF-IDF + Lojistik Regresyon) kıyaslaması.
* **Uçtan Uca Metin Sınıflandırma:** Gerçek **BBC Haberleri** veri seti üzerinde ön işleme, model eğitimi ve modelin `.pkl` olarak dışa aktarımı.

### 🦜🔗 7. [LangChain ile LLM ve Agent Geliştirme](LangChain/README.md)
* **LCEL (LangChain Expression Language):** `prompt | llm | parser` boru hattı mimarisi.
* **Model Entegrasyonları:** Google Gemini (`gemini-2.0-flash`), OpenAI (`gpt-4o / gpt-3.5`) ve Groq / Meta Llama 3.
* **Araç Kullanımı (Function Calling / Tool Use):** Modelin harici fonksiyonları ve API'leri (Hava durumu servisi vb.) çağırması.
* **Yapılandırılmış Çıktılar:** `StrOutputParser`, `JsonOutputParser` ve Pydantic şema doğrulaması (`PydanticOutputParser`).
* **Toplu Veri İşleme:** Müşteri yorumlarının Pydantic şeması ile otomatik analiz edilip etiketlenmesi.

### 🔍 8. [Retrieval-Augmented Generation (RAG) Mimarisi](RAG/README.md)
* **Vektör Temsilleri (Embeddings):** Yoğun vektörler (Dense Vectors), Kosinüs Benzerliği, Chunking stratejileri.
* **Vektör Deposu:** **ChromaDB** üzerinde doküman indeksleme ve metadata filtreleme.
* **İleri Geri Getirme Yöntemleri:** Standart Similarity, **MMR (Maximum Marginal Relevance)** ve Eşik Değeri (Threshold) filtreleme.
* **RAG Triad & Değerlendirme:** Context Precision, Context Recall, Faithfulness (halüsinasyon tespiti) ve Answer Relevance.
* **Uçtan Uca Projeler:** Sepetix E-Ticaret Destek Asistanı & Tüketici Hukuku Kanunu PDF RAG Sistemi.

---

## 🛠️ Kurulum ve Başlangıç

### 1. Depoyu Klonlayın
```bash
git clone https://github.com/52BaranHaydar/Data-Science-and-AI-Mastery.git
cd Data-Science-and-AI-Mastery
```

### 2. Sanal Ortam Oluşturun ve Bağımlılıkları Yükleyin
```bash
python3 -m venv venv
source venv/bin/activate  # Windows için: venv\Scripts\activate
pip install -r requirements.txt
```

### 3. API Anahtarlarını Yapılandırın
```bash
cp .env.example .env
```
`.env` dosyasını açarak OpenAI, Google Gemini veya Groq anahtarlarınızı girin.

### 4. Jupyter Notebook'u Başlatın
```bash
jupyter notebook
```

---

## 👤 Yazar & İletişim

**Baran Haydar**
- 🐙 **GitHub:** [@52BaranHaydar](https://github.com/52BaranHaydar)
- 💼 **Çalışma Alanları:** Veri Bilimi, Makine Öğrenmesi, NLP, LLM Mimarileri, RAG & Otonom Ajanlar

---

## 📜 Lisans
Bu proje [MIT Lisansı](LICENSE) altında lisanslanmıştır. Eğitim ve araştırma amaçlı serbestçe kullanılabilir, genişletilebilir ve paylaşılabilir.
