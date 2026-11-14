# 🏦 Credit Scoring Model — CodeAlpha Internship Task 1

**Intern:** Hammad Ahmed
**Organisation:** CodeAlpha
**Domain:** Machine Learning
**Dataset:** German Credit Risk Dataset (Kaggle)

---

## 📌 Objective

Predict whether a loan applicant is a **Good** or **Bad** credit risk using past financial data, applying classification algorithms and proper ML evaluation techniques.

---

## 📂 Project Structure

```
CodeAlpha_Credit_Scoring_Model/
│
├── credit_scoring_model_FIXED.ipynb   # Main notebook (full pipeline)
├── german_credit_data.csv             # Dataset (with Risk column)
├── requirements.txt
├── outputs/                           # Auto-generated charts
│   ├── eda_overview.png
│   ├── eda_categorical.png
│   ├── eda_correlation.png
│   ├── engineered_features.png
│   ├── cm_logistic_regression.png
│   ├── cm_decision_tree.png
│   ├── cm_random_forest.png
│   ├── model_comparison.png
│   └── feature_importance.png
└── README.md
```

---

## 🔁 Pipeline Overview

| Step | Description |
|------|-------------|
| 1 | Install & Import Libraries |
| 2 | Load Dataset |
| 3 | Exploratory Data Analysis (EDA) |
| 4 | Preprocessing & Encoding |
| 5 | Feature Engineering |
| 6 | Train-Test Split & Scaling |
| 7 | Model Training |
| 8 | Model Evaluation |
| 9 | Model Comparison Charts |
| 10 | Feature Importance |
| 11 | Final Summary |

---

## ⚙️ Models Used

| Model | Description |
|-------|-------------|
| **Logistic Regression** | Linear baseline; interpretable |
| **Decision Tree** | Non-linear rule-based splits |
| **Random Forest** | Ensemble method; best ROC-AUC |

All models use `class_weight='balanced'` to handle the 70/30 class imbalance.

---

## 🛠️ Feature Engineering

| Feature | Formula | Rationale |
|---------|---------|-----------|
| `Debt_to_Duration` | Credit Amount ÷ Duration | Monthly repayment burden |
| `Credit_to_Age` | Credit Amount ÷ Age | Loan size vs life-stage capacity |

---

## 📊 Evaluation Metrics

- Accuracy
- Precision, Recall, F1-Score (focus on Bad Credit class)
- ROC-AUC Score
- Confusion Matrix

---

## 🏆 Results

Held-out test set of 200 applicants (140 good, 60 bad), numbers taken from the notebook output:

| Model | Accuracy | F1 (Bad) | Recall (Bad) | ROC-AUC |
|-------|----------|----------|--------------|---------|
| Logistic Regression | 0.71 | 0.61 | 0.73 | 0.745 |
| Decision Tree | 0.61 | 0.53 | 0.72 | 0.687 |
| **Random Forest** | **0.715** | 0.60 | 0.70 | **0.787** |

> ✅ **Random Forest** ranks best by ROC-AUC. Logistic Regression is about equal on accuracy and slightly ahead on F1 for the Bad class, so the models are close; with only 200 test rows the differences are small. Treat this as a learning exercise, not a production credit model.

## 🚀 How to Run

1. Clone the repository:
```bash
git clone https://github.com/Hammad-Ahmed-hk/CodeAlpha_Credit_Scoring_Model.git
cd CodeAlpha_Credit_Scoring_Model
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Open the notebook:
```bash
jupyter notebook credit_scoring_model_FIXED.ipynb
```

4. Run all cells top to bottom.

---

## 📦 Dependencies

- Python 3.8+
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

---

## 🙏 Acknowledgements

- **CodeAlpha** for the internship opportunity
- **UCI ML Repository / Kaggle** for the German Credit Risk dataset

---

*Made with ❤️ by Hammad Ahmed | CodeAlpha ML Internship*
