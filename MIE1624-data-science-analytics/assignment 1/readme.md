# Developer Salary Analysis: Job Mode & Education Level

**Dataset:** Stack Overflow Annual Developer Survey 2024 — 65,000+ respondents, cleaned subset with non-null salaries (~8,700 records).

**Goal:** Determine whether remote/in-person work mode and education level have statistically significant effects on developer compensation.

---

## Approach

| Analysis | Method |
|---|---|
| Descriptive statistics | Mean, median, std dev; IQR outlier removal |
| Remote vs in-person comparison | Two-sample t-test (manual + scipy) |
| Assumption validation | Shapiro-Wilk normality test, Levene's variance test |
| Robust comparison | Bootstrap resampling (10,000 samples) |
| Education effect | One-way ANOVA + bootstrap validation |

---

## Key Findings

- Remote workers earn ~92% more than in-person workers on average ($83k vs $43k); the gap is statistically significant (p < 0.001) and robust across bootstrap resamples
- Standard parametric assumptions (normality, equal variance) are violated — bootstrap results confirm the gap is real despite this
- Education level has a significant effect on salary (ANOVA p < 0.05); professional degrees show the widest range, Bachelor's and Master's have similar medians

---

## Files

```
MIE1624/
├── salary_stats_analysis.ipynb
└── data/
    └── clean_kaggle_data_2024.csv
```

---

## Stack

Python · NumPy · pandas · SciPy · seaborn · matplotlib
