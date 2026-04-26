<div align="center">

# 🎬 Sentiment Analysis on IMDB Movie Reviews

> **Classify movie reviews as Positive or Negative using Natural Language Processing & Machine Learning**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/harshchill/Sentiment-Analysis/blob/main/sentimentAnalysis.ipynb)
![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange?logo=scikit-learn&logoColor=white)
![NLTK](https://img.shields.io/badge/NLTK-NLP-green)
![Pandas](https://img.shields.io/badge/Pandas-Data-150458?logo=pandas&logoColor=white)
![Accuracy](https://img.shields.io/badge/Accuracy-85.11%25-brightgreen)

</div>

---

## 📖 Overview

This project builds a **binary text classifier** that determines whether an IMDB movie review expresses a **positive** or **negative** sentiment. It walks through a complete end-to-end NLP pipeline — from raw, messy HTML-laden text all the way to a trained Naive Bayes model — achieving **85.11% accuracy** on 10,000 held-out reviews.

---

## ✨ Features

- 🧹 **Text Preprocessing** — HTML tag removal, punctuation stripping, lowercasing, stopword removal, and Porter Stemming
- 📊 **TF-IDF Vectorization** — Converts cleaned text into a numerical feature matrix (top 5,000 terms)
- 🤖 **Multinomial Naive Bayes Classifier** — Fast, interpretable, and effective for text classification
- 📈 **Performance Evaluation** — Accuracy score + full classification report (precision, recall, F1)

---

## 🗂️ Project Structure

```
Sentiment-Analysis/
│
├── sentimentAnalysis.ipynb   # Main Jupyter / Colab notebook
├── IMDB Dataset.csv          # Dataset (50,000 labeled movie reviews)
└── README.md
```

---

## 🔄 Pipeline

```
Raw Reviews (CSV)
      │
      ▼
┌─────────────────────────────────────┐
│  Text Cleaning  (clean_text)        │
│  • Strip HTML tags  <br/>           │
│  • Remove punctuation & numbers     │
│  • Lowercase                        │
│  • Tokenize                         │
│  • Remove English stopwords         │
│  • Porter Stemming                  │
└─────────────────────────────────────┘
      │
      ▼
 Label Encoding   positive → 1  |  negative → 0
      │
      ▼
 Train / Test Split   80% / 20%
      │
      ▼
 TF-IDF Vectorizer   (max_features = 5,000)
      │
      ▼
 Multinomial Naive Bayes  →  Predictions  →  Evaluation
```

---

## 📊 Results

| Metric    | Negative (0) | Positive (1) | Overall |
|-----------|:------------:|:------------:|:-------:|
| Precision | 0.85         | 0.85         | —       |
| Recall    | 0.84         | 0.86         | —       |
| F1-Score  | 0.85         | 0.85         | —       |
| **Accuracy** | — | — | **85.11 %** |

> Evaluated on **10,000 test reviews** (4,961 negative · 5,039 positive)

---

## 🚀 Getting Started

### 1 — Run in the Cloud (Recommended)

Click the badge below — no local setup needed:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/harshchill/Sentiment-Analysis/blob/main/sentimentAnalysis.ipynb)

### 2 — Run Locally

```bash
# Clone the repository
git clone https://github.com/harshchill/Sentiment-Analysis.git
cd Sentiment-Analysis

# Install dependencies
pip install pandas nltk scikit-learn

# Launch the notebook
jupyter notebook sentimentAnalysis.ipynb
```

> **Note:** Place `IMDB Dataset.csv` in the project root before running. The dataset is available on [Kaggle](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews).

---

## 🛠️ Tech Stack

| Library | Purpose |
|---------|---------|
| `pandas` | Data loading & manipulation |
| `nltk` | Stopwords corpus & Porter Stemmer |
| `scikit-learn` | TF-IDF, train/test split, Naive Bayes, metrics |
| `re` | Regex-based HTML & punctuation cleaning |

---

## 📚 Dataset

**IMDB Movie Reviews** — 50,000 polar (positive / negative) movie reviews sourced from the Internet Movie Database.

| Property | Value |
|----------|-------|
| Total samples | 50,000 |
| Classes | Positive, Negative |
| Balance | 50 % / 50 % |
| Source | [Kaggle IMDB Dataset](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews) |

---

## 🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/improve-model`)
3. Commit your changes (`git commit -m 'Add logistic regression model'`)
4. Push to the branch (`git push origin feature/improve-model`)
5. Open a Pull Request

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

<div align="center">

Made with ❤️ by [harshchill](https://github.com/harshchill)

</div>
