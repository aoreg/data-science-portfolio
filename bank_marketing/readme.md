# Bank Marketing: Term Deposit Subscription Prediction

## Business Problem

A bank runs outbound phone campaigns to sell term deposits. With 100,000 customer records and a 30% subscription rate, calling every customer indiscriminately is expensive — the goal is to identify which customers are most likely to subscribe so the campaign team can prioritize outreach and reduce cost-per-acquisition.

This project builds and compares three classification models to rank customers by conversion likelihood.

---

## Key Findings

- **XGBoost achieves the best recall (61.7%)** — meaning it correctly identifies nearly two-thirds of all eventual subscribers, while Logistic Regression is close behind (60.2%)
- **Random Forest is precision-optimized (55.7% precision)** but misses 86% of actual subscribers — a poor tradeoff when the cost of a missed sale outweighs the cost of an extra call
- **Call duration is the single strongest predictor** of subscription, but it is only observable *after* the call ends — including it would cause data leakage in any real-time deployment. It was retained here for benchmarking purposes but should be removed in production
- **ROC AUC of ~68% across all models** indicates moderate ranking ability — models reliably distinguish likely subscribers from non-subscribers, and threshold tuning against a precision-recall curve would improve business outcomes over the default 0.5 cutoff

---

## Results

| Model | Accuracy | Precision | Recall | F1 | ROC AUC |
|---|---|---|---|---|---|
| Logistic Regression | 64.7% | 43.6% | 60.2% | 50.6% | 68.2% |
| Random Forest | 70.8% | 55.7% | 14.0% | 22.4% | 67.4% |
| XGBoost | 63.4% | 42.5% | 61.7% | 50.3% | 67.9% |

**Primary metric: Recall** — missing a likely subscriber costs more than making an unnecessary call.

---

## Approach

Three classifiers trained on an 80/20 stratified split, each with explicit imbalance handling:

| Model | Imbalance Strategy |
|---|---|
| Logistic Regression | `class_weight="balanced"` |
| Random Forest | `class_weight="balanced_subsample"` |
| XGBoost | `scale_pos_weight` tuned to class ratio |

All models share a unified sklearn `Pipeline` with `StandardScaler` for numeric features and `OneHotEncoder` for categorical features, ensuring no preprocessing leakage between train and test sets.

---

## Dataset

**UCI Bank Marketing Dataset** — 100,000 customer records, 44 features, 30% positive rate (term deposit subscribed).

Features include customer demographics, account history, campaign contact details, and economic indicators.

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


---

## Next Steps

- Remove `LastContactDuration` and re-evaluate — it leaks post-call information and cannot be used for real-time scoring
- Tune the classification threshold using a precision-recall curve calibrated to the bank's cost function (cost of missed sale vs. cost of unnecessary call)
- Apply SHAP values for per-customer explanations to support frontline decision-making

---

## Stack

Python · pandas · NumPy · scikit-learn · XGBoost · matplotlib · seaborn
