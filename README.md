# 📱 SMS Spam Detector

A machine learning project that classifies SMS messages as **Spam** or **Ham (Not Spam)** using Natural Language Processing (NLP) and Naive Bayes classification.

---

## 🎯 Problem Statement
With the rise of spam messages, automatically detecting and filtering them is a critical real-world problem. This project builds a classifier that identifies spam SMS messages with 97.2% accuracy.

---

## 📂 Dataset
- **Source:** [SMS Spam Collection Dataset - UCI / Kaggle](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)
- **Size:** 5,572 messages
- **Distribution:** 4,825 Ham | 747 Spam (imbalanced dataset)

---

## 🔧 Tech Stack
- Python 3
- Pandas, NumPy
- Scikit-learn
- NLTK
- Matplotlib, Seaborn

---

## 🧠 Approach

1. **EDA** — Explored class distribution and message length patterns
   - Spam messages are ~2x longer than ham (139 vs 71 chars avg)
2. **Preprocessing** — Removed special chars, lowercased, removed stopwords, applied stemming
3. **Feature Extraction** — TF-IDF Vectorization (top 3000 features)
4. **Model** — Multinomial Naive Bayes
5. **Evaluation** — Accuracy, Precision, Recall, F1-Score, Confusion Matrix

---

## 📊 Results

| Metric | Ham | Spam |
|--------|-----|------|
| Precision | 0.97 | 1.00 |
| Recall | 1.00 | 0.79 |
| F1-Score | 0.98 | 0.88 |

**Overall Accuracy: 97.2%**

Key insight: The model achieves **zero false positives** — it never marks a legitimate message as spam.

---

## 📈 Visualizations

- Spam vs Ham distribution
- Message length distribution by class
- Confusion matrix heatmap

---

## 🚀 How to Run

```bash
git clone https://github.com/koushik280227/sms-spam-detector.git
cd sms-spam-detector
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

Then open `spam_detector.ipynb` in VS Code or Jupyter.

---

## 🔍 Sample Predictions

"Congratulations! You've won a free iPhone. Click here!"  →  🚨 SPAM (87% confident)
"Hey, are we still meeting tomorrow for lunch?"           →  ✅ HAM (100% confident)

---

## 💡 Key Learnings
- Real-world datasets are imbalanced — accuracy alone is misleading
- Spam messages tend to be longer and use urgency/reward language
- TF-IDF effectively captures word importance across documents
- Naive Bayes works surprisingly well for text classification

---

## 🔮 Future Scope
- Try LSTM or BERT for improved recall on spam
- Build a simple web interface using Streamlit
- Handle multilingual spam messages

---