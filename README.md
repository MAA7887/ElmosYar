
# Yar-e Elmos 🎓
**Professor Analytics & Recommendation System for Students**

Yar-e Elmos is a data mining and NLP-based system that transforms scattered student opinions about university professors into an analytical dashboard and an explainable recommendation engine. The goal is to help students make informed course-selection decisions based on teaching quality, grading style, and collective student sentiment.

---

## ✨ Features

- 📊 **Exploratory Data Analysis (EDA)** of student feedback
- 🧹 **Robust data parsing & cleaning** for noisy Persian text
- 🧠 **NLP-based sentiment analysis** on student comments
- 🔍 **Keyword extraction & topic exploration**
- 📈 **Supervised models** for score/sentiment prediction
- 🧩 **Unsupervised clustering** of professors (KMeans + PCA)
- 🤝 **Explainable recommender system** (Content-Based + Rule-Based)
- 🖥 **Interactive Streamlit dashboard**

---

## 🗂 Project Structure

```
project/
│── data/
│   ├── raw/              # Raw JSON data
│   ├── cleaned/          # Cleaned & processed datasets
│
│── notebooks/            # EDA & experimentation notebooks
│
│── src/
│   ├── parser.py         # Message parsing & field extraction
│   ├── preprocessing.py # Text cleaning & normalization
│   ├── nlp.py            # Sentiment & keyword extraction
│   ├── models.py         # ML models (supervised & unsupervised)
│   ├── recommender.py    # Recommendation logic
│
│── dashboard/            # Streamlit app
│── report/               # Final report & figures
│── README.md
```

---

## 📊 Data Description

**Source:** JSON files containing student messages

**Extracted Fields:**
- Professor name
- Course name
- Faculty
- 6 numerical scores
- Student comment (optional)
- Grading style (easy / fair / hard)
- Attendance policy
- Term / date (if available)

---

## 🧹 Data Preprocessing

- Persian/Arabic character normalization (ی/ي، ک/ك)
- Emoji and noise removal
- Course name standardization
- Professor name unification using **RapidFuzz** (fuzzy matching)
- Invalid or unparseable messages flagged as `parse_error`

---

## 🧠 NLP Pipeline

- Tokenization & stopword removal (Persian)
- Sentiment analysis (Positive / Neutral / Negative)
- TF-IDF keyword extraction
- WordCloud generation per professor

---

## 🤖 Modeling

### Supervised Learning
- Logistic Regression
- Random Forest
- Tasks:
  - Sentiment classification
  - Overall score prediction

### Unsupervised Learning
- Feature engineering from scores + sentiment
- PCA for dimensionality reduction
- KMeans for professor clustering

---

## 🤝 Recommendation System

**Approach:**
- Content-Based Scoring
- Cosine Similarity
- Rule-Based filtering

**Student Preferences:**
- Teaching quality
- Grading strictness
- Project-oriented courses
- Overall sentiment

**Output:**
- Ranked list of recommended professors with short explanations

---

## 🖥 Dashboard (Streamlit)

### Pages
1. **Overview**
   - Total reviews
   - Covered professors
   - Score distributions

2. **Professor Profile**
   - Radar chart of scores
   - Sentiment distribution
   - WordCloud
   - Trend over semesters

3. **Recommender**
   - Preference inputs
   - Recommended professors + reasons

---

## 🚀 Getting Started

```bash
pip install -r requirements.txt
streamlit run dashboard/app.py
```

---

## ⏱ Project Timeline

- EDA & Parsing
- Data Cleaning & Standardization
- NLP & Modeling
- Recommender System
- Dashboard & Final Report

---

## ⚠ Limitations

- Noisy and informal student text
- Limited labeled data for supervised learning
- Lightweight NLP models due to hardware constraints

---

## 👥 Team

- **Amirhossein Oliya**
- **Mohammadamin Abbasi**

---

## 📌 Academic Context

This project was developed as a **final data mining course project**, focusing on interpretability, practical decision support, and real-world Persian text processing.

---

## 📜 License

This project is for academic use only.

