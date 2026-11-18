# 🦜🔗 LangChain ile LLM ve Agent Geliştirme

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)](https://www.langchain.com/)
[![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)](https://openai.com/)
[![Google Gemini](https://img.shields.io/badge/Google--Gemini-8E75C2?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev/)
[![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=for-the-badge&logo=pydantic&logoColor=white)](https://docs.pydantic.dev/)

Büyük Dil Modelleri (LLM) ile üretim kalitesinde uygulamalar, araç çağıran ajanlar (Tool Use / Function Calling) ve yapılandırılmış veri işleme boru hatları geliştirme deposu.

---

## 🧭 LCEL (LangChain Expression Language) Mimarisi

```mermaid
flowchart LR
    A["Girdi Parametreleri"] --> B["ChatPromptTemplate"]
    B --> C["ChatModel (Gemini / GPT / Llama)"]
    C --> D["OutputParser (Pydantic / JSON)"]
    D --> E["İş Mantığı & Yanıt"]
```

---

## 📚 Notebook Serisi ve İçerik

| Notebook | Konu & Başlık | Temel Yetkinlikler |
| :--- | :--- | :--- |
| **[`langchain.ipynb`](langchain.ipynb)** | **Temel LCEL & Model Entegrasyonu** | Google Gemini (`gemini-2.0-flash`) & OpenAI entegrasyonu, `ChatPromptTemplate`, boru hattı (`\|`) operatörü |
| **[`ToolUse.ipynb`](ToolUse.ipynb)** | **Araç Kullanımı (Function Calling / Tool Use)** | OpenAI JSON Schema ile fonksiyon tanımlama, harici API çağrısı (`wttr.in` hava durumu), modelin aracı tetiklemesi |
| **[`notebook-output-parse.ipynb`](notebook-output-parse.ipynb)** | **Yapılandırılmış Çıktı Ayrıştırıcıları** | `StrOutputParser`, `JsonOutputParser`, `PydanticOutputParser` ile şema doğrulama ve tip güvenliği |
| **[`Llmverisleme.ipynb`](Llmverisleme.ipynb)** | **Toplu Veri İşleme (Batch Processing)** | Müşteri yorumlarını Pandas ile okuma, Pydantic şemasıyla duygu/kategori etiketleme, iş değeri üretimi |
| **[`langchain-grog.ipynb`](langchain-grog.ipynb)** | **Groq & Meta Llama Entegrasyonu** | Ultra hızlı çıkarım (inference) için Groq / Meta Llama 3 API kullanımı ve prompt zincirleme |
| **[`Calısma1.ipynb`](Calısma1.ipynb)** | **Pratik LangChain Laboratuvarı** | Çok adımlı zincirler ve parametrik soru-cevap denemeleri |

---

## ⚙️ Kurulum ve Ortam Değişkenleri

1. Gerekli kütüphaneleri yükleyin:
```bash
pip install -r requirements.txt
```

2. `.env` dosyasını oluşturun ve API anahtarlarınızı girin:
```bash
cp .env.example .env
```

```env
OPENAI_API_KEY=your_openai_api_key_here
GOOGLE_API_KEY=your_gemini_api_key_here
GROQ_API_KEY=your_groq_api_key_here
```
