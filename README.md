# Automated Purchase Order Classification 🚀

This project implements an **automated classification system for purchase orders (POs)** using Natural Language Processing (NLP) and Machine Learning techniques. The goal is to automatically assign POs to the correct account category based on textual description and additional engineered features. 📝

---

## Dataset 📂

The dataset consists of real purchase orders from multiple periods:

- Apr-Jun 2019
- Jan-Mar 2020
- Apr-Jun 2020
- Jul-Sep 2020

Key columns used:

- `po_description_clean`: textual description of the PO.
- `account_name_clean`: cleaned account label.
- Additional engineered features: `amount`, `keyword_rent`, `keyword_salary`.

![dataset-gif](https://media.giphy.com/media/3o6ZsZDQhox1aZg10I/giphy.gif)

---

## Methodology 🛠️

1. **Data Preprocessing**
   - Missing values filled and cleaned.
   - Textual description concatenated from multiple columns.
   - Labels encoded for machine learning.

2. **Feature Engineering**
   - TF-IDF vectorization of PO descriptions.
   - Engineered numerical features combined with TF-IDF for XGBoost.
   - Text tokenization for DistilBERT.

3. **Models**
   - Logistic Regression with TF-IDF features.
   - XGBoost Classifier with TF-IDF + engineered features.
   - DistilBERT Transformer for sequence classification.

![workflow-gif](https://media.giphy.com/media/l0MYt5jPR6QX5pnqM/giphy.gif)

---

## Model Performance 📊

### Logistic Regression

- Accuracy: ~91.8%
- Weighted F1-score: ~0.89

### XGBoost Classifier

- Accuracy: ~98.4%
- Weighted F1-score: ~0.98

### DistilBERT

- Accuracy: ~99% (depending on training epochs)
- Handles text natively without manual feature engineering.

**Classification reports** were generated for all models, showing precision, recall, and F1-score per account category.

![performance-gif](https://media.giphy.com/media/26xBukhFZyn1v3Cuk/giphy.gif)

---

## Visualization 📈

- Confusion matrices: interactive heatmaps to analyze model performance per category.
- Performance comparison: bar plots comparing accuracy, macro F1, and weighted F1 of Logistic Regression, XGBoost, and DistilBERT.

---

## Project Highlights 🌟

- Demonstrates the use of **NLP for supply chain automation**.
- Combines **traditional ML** (Logistic Regression, XGBoost) and **deep learning NLP** (DistilBERT).
- Can be extended for **real-time PO classification** in enterprise systems.
- Interactive visualizations help explain model performance to business stakeholders.

---

## Next Steps / Improvements 🔧

- Handle **rare categories** more effectively using class balancing.
- Experiment with **hyperparameter tuning** for XGBoost and DistilBERT.
- Incorporate **additional PO metadata** (e.g., supplier region, date features).
- Deploy as a **web app** for live prediction using Streamlit or FastAPI.

---

## How to Run ▶️

1. Clone the repository and install dependencies.
2. Run the notebook or script to reproduce the results.

---

### Author 👨‍💻

Hossein Zandinejad

---

**License:** MIT License
