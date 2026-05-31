# Heart Disease Prediction: Binary Classification

**Dataset:** UCI Cleveland Heart Disease — 303 patients, 13 clinical features (age, sex, chest pain type, resting BP, cholesterol, max heart rate, ST depression, exercise-induced angina, vessels coloured, thalassemia).

**Target:** Binary — presence (1) or absence (0) of heart disease.

---

## Approach

| Step | Description |
|---|---|
| Data cleaning | Replace `?` missing values in `ca` and `thal`; impute with mode |
| Target encoding | Multi-class target (0–4) → binary (0 = healthy, 1 = disease) |
| EDA | 6 charts: age distribution, cholesterol boxplot, sex breakdown, chest pain type, correlation heatmap, max heart rate by class |
| Pipeline | sklearn `ColumnTransformer` — StandardScaler (numeric) + OneHotEncoder (categorical) |
| Models | Logistic Regression and Random Forest, each evaluated with confusion matrix and ROC curve |
| Tuning | GridSearchCV on Random Forest (n_estimators, max_depth, min_samples_split) |

---

## Key Findings

- Max heart rate (`thalach`) and chest pain type (`cp`) are the strongest predictors
- Random Forest outperforms Logistic Regression on AUC after tuning
- StandardScaler is critical for Logistic Regression convergence on this mixed-type dataset

---

## Files

```
MIE1628/
├── heart_disease_classification.ipynb
└── data/
    └── heart_disease.csv
```

---

## Stack

Python · pandas · NumPy · scikit-learn · seaborn · matplotlib
