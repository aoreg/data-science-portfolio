# Bank Marketing: Term Deposit Subscription Prediction

**Dataset:** UCI Bank Marketing Dataset — 41,188 records from a Portuguese bank's direct marketing campaign (phone calls).

**Goal:** Predict whether a client will subscribe to a term deposit — a binary classification problem with ~11% positive rate (class imbalance).

---

## Approach

Three classifiers trained and compared, each with explicit imbalance handling:

| Model | Imbalance Strategy |
|---|---|
| Logistic Regression | `class_weight="balanced"` |
| Random Forest | `class_weight="balanced_subsample"` |
| XGBoost | `scale_pos_weight` tuned to class ratio |

All models use a shared sklearn `Pipeline` with `StandardScaler` for numeric features and `OneHotEncoder` for categorical features.

---

## Results

Models are evaluated on Accuracy, Precision, Recall, F1, and ROC AUC. Given the imbalance, **Recall and ROC AUC are the primary metrics** — the cost of missing a likely subscriber outweighs the cost of a wasted call.

---

## Files

```
bank-marketing/
├── bank_marketing_classification.ipynb   # Full notebook
└── data/
    ├── bank-additional-full.csv          # Dataset (41,188 rows, 21 features)
    └── bank-additional-names.txt         # Feature descriptions and citation
```

---

## Key Findings

- **Call duration** is the strongest predictor but is only known after the call — it should be dropped for any real-time deployment
- ROC AUC of ~94% across models indicates strong ranking ability despite the class imbalance
- All three models achieve high recall at the cost of precision; threshold tuning would be the next step for a production system

---

## Stack

Python · pandas · NumPy · scikit-learn · XGBoost · matplotlib
