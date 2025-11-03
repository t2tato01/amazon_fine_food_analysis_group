# 🧠 Amazon Fine Food Reviews – NLP Helpfulness Analysis

This project explores what makes an Amazon food review **helpful** using Natural Language Processing (NLP).  
We analyze over **500,000 reviews** to study how linguistic and structural features (sentiment, readability, coherence, and summarization quality) relate to user-perceived helpfulness.

---

## 📘 Project Overview

| Section | Description |
|:--------|:-------------|
| **Task 1–2** | Data preprocessing and grouping (L1–L3 subsets by helpfulness metrics) |
| **Task 3** | Sentiment scoring (SentiStrength or lexicon-based) and time trend visualization |
| **Task 4** | Correlation analysis between text features and ratings |
| **Task 5** | Incomplete sentence detection using POS tagging |
| **Task 6** | Readability estimation (Gunning Fog, ForeCast) |
| **Task 7–9** | Summary extractiveness and auto-summary comparison (Gensim TF–IDF & frequency-based) |

---

## 🧩 Data

**Dataset:** [Amazon Fine Food Reviews (Kaggle)](https://www.kaggle.com/snap/amazon-fine-food-reviews)  
**Source:** McAuley, J., & Leskovec, J. (2013). *From Amateurs to Connoisseurs: Modeling the Evolution of User Expertise through Online Reviews.*

Each review includes:
- `Text`, `Summary`, `Score`, `HelpfulnessNumerator`, `HelpfulnessDenominator`, `Time`

---

## ⚙️ Implementation Pipeline

1. **Data Cleaning & Tokenization**
   - Remove missing values and normalize text
   - Tokenize with NLTK; remove stopwords

2. **Feature Extraction**
   - Sentiment score (SentiStrength / lexicon fallback)
   - Readability: Gunning Fog & ForeCast
   - POS-based incomplete sentence check

3. **Analysis**
   - Correlation of linguistic features with helpfulness & ratings
   - Sentiment trend over time
   - Summary overlap with extractive and generated summaries

4. **Visualization**
   - Bar and line charts via `matplotlib` & `seaborn`

---

## 📊 Example Results

| Insight | Observation |
|:--------|:-------------|
| **Text Length** | Helpful reviews are longer and richer in non-stopwords. |
| **Sentiment** | Positive sentiment dominates; negativity decreases over time. |
| **Readability** | Helpful reviews are moderately complex (Fog ≈ 12–14). |
| **Summary Overlap** | ~50% of summaries are extractive; L3 subset shows highest overlap. |

Example visualizations (see `/figures/`):
- `tokens_characters.png`
- `sentiment_trend_L1.png`, `sentiment_trend_L2.png`, `sentiment_trend_L3.png`
- `correlation_plot.png`
- `summary_overlap_comparison.png`

---

## 🧪 How to Run

### Requirements
```bash
pip install kagglehub sentistrength fuzzywuzzy python-Levenshtein nltk gensim matplotlib seaborn scipy pandas
