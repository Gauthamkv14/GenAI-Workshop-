# 🐦 Twitter Sentiment & Emotion Analysis (MVP)

This project analyzes **Twitter text data** to detect both **sentiment** (positive / neutral / negative) and **emotions** (27 fine-grained categories).  
It combines state-of-the-art NLP models with clean visualizations to give **insight into how people feel online**.

---

## 🚀 Features
- 📂 Input Options: Upload your own CSV file of tweets, or use the built-in demo dataset.  
- 🧹 Preprocessing: Cleans tweets (removes links, mentions, hashtags).  
- 🔎 Sentiment Analysis: Uses [`cardiffnlp/twitter-roberta-base-sentiment`](https://huggingface.co/cardiffnlp/twitter-roberta-base-sentiment) for robust Twitter sentiment classification.  
- 🎭 Emotion Detection: Uses [`bhadresh-savani/bert-base-go-emotion`](https://huggingface.co/bhadresh-savani/bert-base-go-emotion) trained on Google’s **GoEmotions** dataset.  
- 📊 Visualizations:
  - Sentiment distribution (pie & bar chart)
  - Top 10 emotions
  - Word clouds (positive & negative tweets)  
- 💾 Export: Save results (`text`, `sentiment`, `emotion`, scores) as CSV.  
- 📈 Summary: Prints overall statistics (counts, averages).  

---

## ⚙️ Tech Stack
- Python 3.12 (Google Colab)
- Hugging Face Transformers
- PyTorch
- Pandas, NumPy
- Matplotlib, Seaborn
- WordCloud

---

## 📂 Project Structure
📁 twitter-sentiment-emotion
├── twitter_sentiment_analysis.ipynb # Main notebook (Google Colab ready)
├── sampled_30k.csv 
├──training.1600000.processed.noemoticon.csv
├── README.md 

## 🔧 How to Run
1. Clone the repo:
   ```bash
   git clone https://github.com/<your-username>/twitter-sentiment-analysis.git
   cd twitter-sentiment-analysis

2. Open the notebook in Google Colab (recommended).
-Upload twitter_sentiment_emotion_mvp_full.ipynb to your Google Drive and run step by step.

3.Data Input Options:

-Upload your own CSV of tweets (text column required).
-Or use the built-in demo dataset inside the notebook.
-Or use a sampled subset of Sentiment140.

🙌 Acknowledgements

-Sentiment140 Dataset
-GoEmotions
-Hugging Face Transformers team
