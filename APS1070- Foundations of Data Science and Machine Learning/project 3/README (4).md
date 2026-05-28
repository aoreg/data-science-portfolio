# APS1070 – Foundations of Data Analytics and Machine Learning

> **Fall 2024** · University of Toronto · Python · Jupyter Notebooks

---

## Projects

### Thyroid Disease Detection — Anomaly Detection with Gaussian Mixture Models
**Notebook:** `thyroid_anomaly_detection.ipynb`

Binary classification on a severely imbalanced medical dataset (97.5% / 2.5%). Four progressively complex GMM approaches:

| Model | Description |
|---|---|
| Univariate GMM | Single Gaussian per feature; rank by validation AUC |
| Bivariate GMM | Two-component mixture on feature pairs |
| Class-conditional GMM | Separate Gaussians per class; tune likelihood ratio threshold |
| Multivariate mixture | Unrestricted features + components; full model search |

Best model: Attribute1 + Attribute3, 2 components per class. Key takeaway: standard accuracy is meaningless under this level of imbalance — F1 and AUC are the only reliable signals.

---

### Global GDP & US Electricity: Dimensionality Reduction with PCA and SVD
**Notebook:** `pca_svd_gdp_electricity.ipynb`

Applied to two datasets:
- **World GDP** — 179 countries × 52 years (1970–2021)
- **US Electricity Sales** — 62 states × 24 years (2001–2024)

Key findings:
- Only **4 principal components** capture 99.9% of variance in the GDP dataset — global economic trends are highly correlated
- PCA and SVD produce identical components; SVD is faster as it skips covariance computation
- Incremental reconstruction with 8–16 PCs closely recovers individual country series with low RMSE

---

## Stack

Python · NumPy · pandas · scikit-learn · matplotlib
