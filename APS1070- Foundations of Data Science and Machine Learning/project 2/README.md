# APS1070 – Foundations of Data Analytics and Machine Learning

> **Fall 2024** · University of Toronto · Jupyter Notebooks · Python

---

## Projects

### Thyroid Disease Detection — Anomaly Detection with Gaussian Mixture Models

**Notebook:** `thyroid_anomaly_detection.ipynb`

**Dataset:** Thyroid Disease — 3,772 patient records, 6 anonymised clinical features, binary label (hypothyroid yes/no).

**Problem:** Extreme class imbalance (97.5% healthy / 2.5% hypothyroid) makes this an anomaly-detection task. Standard classifiers biased toward the majority class fail here — the goal is to reliably surface the rare positive cases using density-based modelling.

**Approach — four progressively complex GMM variants:**

| Model | Description |
|---|---|
| Univariate GMM | Single Gaussian per feature; rank features by validation AUC |
| Bivariate GMM | Two-component mixture on feature pairs; visualise outliers |
| Class-conditional GMM | Separate Gaussians for each class; tune likelihood ratio threshold c |
| Multivariate mixture | Unrestricted features + components; full model search across 10+ configs |

**Key findings:**
- Best model: Attribute1 + Attribute3 with 2 components per class
- F1 and ROC AUC are the only meaningful metrics under this level of imbalance — accuracy is misleading
- Class-conditional modelling outperformed unsupervised anomaly scoring by tuning the decision boundary between class likelihoods

---

## Stack

Python · pandas · NumPy · scikit-learn · matplotlib · seaborn
