# 🚀 GenAI Projects Collection

This repository contains a set of **Generative AI and NLP mini-projects** built using Hugging Face, LangChain, FAISS, Gradio, and PyTorch.  
The goal is to explore **LLMs, RAG (Retrieval-Augmented Generation), and sentiment analysis** through hands-on implementations.

---

## 📂 Projects Overview

### 1. Conversational Assistant (in Colab Notebook)
- **Description:**  
  A simple conversational assistant built using **FLAN-T5** (`flan-t5-large`) with improved prompt handling.  
- **Tech stack:** Hugging Face Transformers, PyTorch.  
- **Features:**  
  - Maintains chat history context.  
  - Deterministic beam search (no hallucinated randomness).  
  - Truncates long prompts to prevent token overflow.  
  - Answers concisely; falls back to "I don’t know" when unsure.  

---

### 2. RAG (Retrieval-Augmented Generation) with FAISS
- **Description:**  
  A minimal pipeline that lets you **upload documents** (PDF, DOCX, TXT), split them into chunks, embed with **SentenceTransformers**, index with **FAISS**, and then query them using FLAN-T5 with **LangChain RetrievalQA**.  
- **Tech stack:** LangChain, FAISS, SentenceTransformers, Hugging Face Transformers.  
- **Features:**
  - Handles text, PDF, and Word files.  
  - Chunking with `RecursiveCharacterTextSplitter`.  
  - Embedding model: `all-MiniLM-L6-v2`.  
  - LLM: `flan-t5-large` wrapped with truncation-safe generation.  
  - Interactive Q&A loop in terminal.  
  - Shows **retrieved source filenames** for transparency.  

---

### 3. Startup Idea + Pitch Generator (Gradio App)
- **Description:**  
  A Gradio-powered web app that generates startup ideas and structured pitch decks based on a given domain (e.g., Agritech, Fintech, Edtech).  
- **Tech stack:** Hugging Face (`LaMini-flan-T5`), Gradio, Transformers.
- **Features:**
  - Generates sections: *Business Idea, Problem Statement, Solution, Revenue Model, Go-to-Market, Risks, Tagline*.  
  - User-adjustable parameters: temperature, max tokens, sampling mode.  
  - Dropdown + examples for quick testing.  
  - UI built with Gradio Blocks.  

---

### 4. Twitter Sentiment & Emotion Analysis
- **Description:**  
  Analyzes tweets to detect both **sentiment** (positive / neutral / negative) and **emotions** (27 categories from GoEmotions).  

- **Tech stack:**  
  Hugging Face Transformers, PyTorch, Pandas, Matplotlib, WordCloud.  

- **Features:**  
  - Cleans tweets (removes links, mentions, hashtags)  
  - Sentiment model: [`cardiffnlp/twitter-roberta-base-sentiment`](https://huggingface.co/cardiffnlp/twitter-roberta-base-sentiment)  
  - Emotion model: [`bhadresh-savani/bert-base-go-emotion`](https://huggingface.co/bhadresh-savani/bert-base-go-emotion)  
  - Visualizations: sentiment distribution, top emotions, positive/negative word clouds  
  - CSV export of results with sentiment, emotion, and scores  


---

## ⚙️ Setup & Installation

Clone the repo and install dependencies:

```bash
git clone https://github.com/your-username/genai-projects.git
cd genai-projects
```
For Colab users, you can skip cloning and just open the notebooks directly.

## 🙌 Acknowledgements
- Hugging Face Transformers & Datasets  
- LangChain & FAISS  
- CardiffNLP, Bhadresh Savani for pretrained models  
- Gradio team for easy UIs  
- Thanks to **GetSkilled** for conducting the GenAI workshop that guided these projects.
