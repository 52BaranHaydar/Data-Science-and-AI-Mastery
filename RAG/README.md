# 🔍 Retrieval-Augmented Generation (RAG) Mimarisi ve Uygulamaları

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)](https://www.langchain.com/)
[![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6600?style=for-the-badge)](https://www.trychroma.com/)
[![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)](https://openai.com/)

Büyük Dil Modellerinin (LLM) bilgi kesinti tarihi (knowledge cutoff) ve halüsinasyon (hallucination) sınırlarını aşmak için harici özel veri tabanları ve dokümanlarla beslenen **RAG (Retrieval-Augmented Generation)** sistemleri.

---

## 🧭 RAG Sistem Mimarisi

```mermaid
flowchart TD
    subgraph 1. İndeksleme ve Hazırlık (Offline Ingestion)
        A["Özel Belgeler (PDF, MD, Web)"] --> B["Document Loader (PyPDFLoader)"]
        B --> C["Metin Parçalama (RecursiveTextSplitter)"]
        C --> D["Embedding Modeli (Dense Vectors)"]
        D --> E[("Vektör Veritabanı (ChromaDB / FAISS)")]
    end
    
    subgraph 2. Çıkarım ve Yanıtlama (Online Inference)
        F["Kullanıcı Sorusu"] --> G["Soru Embedding'i"]
        G --> H{"Semantik Arama (Similarity / MMR)"}
        E -.-> H
        H --> I["Top-K İlgili Parçalar (Context)"]
        F --> J["Augmented Prompt"]
        I --> J
        J --> K["LLM (GPT / Llama / Gemini)"]
        K --> L["Doğrulanmış Yanıt"]
    end
```

---

## 📚 Notebook Serisi ve Yol Haritası

| Notebook | Başlık | Kapsam & Yetkinlikler |
| :--- | :--- | :--- |
| **[`Embeddings.ipynb`](Embeddings.ipynb)** | **Vektör Temsilleri (Embeddings)** | Semantik arama vs Kelime araması (Ctrl+F), Yoğun vektörler (Dense Vectors), Kosinüs Benzerliği ($\cos\theta$), Metin parçalama (Chunking) |
| **[`RAG.ipynb`](RAG.ipynb)** | **RAG Temelleri & Boru Hattı** | LLM'in sınırları ve halüsinasyon problemi, RAG Triad, Retrieval ve Generation ayrımı, Uçtan uca basit RAG zinciri |
| **[`RAGChatBot.ipynb`](RAGChatBot.ipynb)** | **İleri Geri Getirme Stratejileri** | 1. Similarity Search, 2. **MMR (Maximum Marginal Relevance)** ile çeşitlilik-alaka dengesi, 3. Similarity Score Threshold filtreleme |
| **[`RAGChatBotProje.ipynb`](RAGChatBotProje.ipynb)** | **Sepetix E-Ticaret Destek Asistanı** | Şirket içi yardım ve ürün dökümanlarını indeksleme, RAG'siz vs RAG'li model kıyaslaması, Destek asistanı zinciri |
| **[`RagDegerlendirme.ipynb`](RagDegerlendirme.ipynb)** | **RAG Değerlendirme & Metrikleri** | **Retrieval:** Precision@K, Recall@K, MRR, Hit Rate; **Generation:** Faithfulness (doğruluk), Answer Relevance (alaka düzeyi) |
| **[`ragprojesi.ipynb`](ragprojesi.ipynb)** | **Tüketici Kanunu PDF RAG Asistanı** | Gerçek PDF mevzuat yükleme (`PyPDFLoader`), 800 karakterlik örtüşmeli chunking, ChromaDB üzerinde kanun maddeleri soru-cevap |

---

## ⚖️ RAG Değerlendirme Çerçevesi (RAG Triad)

1. **Context Relevance (Bağlam Alakası):** Getirilen parçalar kullanıcının sorusuyla ne kadar doğrudan ilişkili?
2. **Groundedness / Faithfulness (Temellendirilmişlik):** Modelin ürettiği yanıt verilen bağlam tarafından destekleniyor mu (Halüsinasyon yok mu)?
3. **Answer Relevance (Yanıt Alakası):** Model kullanıcının sorduğu soruya eksiksiz ve doğrudan cevap veriyor mu?

---

## 🚀 Kurulum ve Çalıştırma

```bash
pip install -r requirements.txt
cp .env.example .env
jupyter notebook
```
