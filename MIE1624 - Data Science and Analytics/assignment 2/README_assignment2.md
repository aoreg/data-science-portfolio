# Developer Salary Prediction: Multi-Class Ordinal Classification

**Dataset:** Kaggle Machine Learning & Data Science Survey 2022 — global respondents, salary encoded into ordinal compensation buckets.

**Goal:** Predict a survey respondent's annual compensation bucket from survey responses about tools, experience, and background.

---

## Pipeline

| Step | Description |
|---|---|
| Data cleaning | Drop irrelevant columns, impute missing values (median/unknown), label + one-hot encode |
| Feature engineering | Combine experience and education into composite features |
| Feature selection | Chi-square filter + LassoCV (selected ~15 from 72 features) |
| Modelling | Custom `OrdinalLogisticRegression` class (sklearn base) |
| Validation | K-fold cross-validation, bias-variance decomposition |
| Tuning | GridSearchCV over C, solver, max_iter |
| Evaluation | Confusion matrix, classification report on held-out test set |

---

## Key Findings

- Strongest predictors: Q4 (education), Q2 (age), Q27 (experience)
- High bias (~20) reflects the difficulty of predicting salary from noisy survey responses; errors are predominantly in adjacent salary buckets
- Dataset skews heavily toward low-compensation respondents — precision on higher salary classes is limited by class imbalance

---

## Files

```
MIE1624/
├── salary_prediction_classification.ipynb
└── data/
    └── clean_kaggle_data_2022.csv
```

---

## Stack

Python · pandas · NumPy · scikit-learn · seaborn · matplotlib
