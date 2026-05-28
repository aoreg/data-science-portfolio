# APS1070 – Foundations of Data Analytics and Machine Learning

> Fall 2024 · University of Toronto · Python · Jupyter Notebooks

Three projects covering core ML methods from scratch: anomaly detection, dimensionality reduction, and regression with gradient descent.

---

### Thyroid Disease Detection
**`thyroid_anomaly_detection.ipynb`** · Gaussian Mixture Models · Imbalanced Classification

Anomaly detection on a medical dataset with 97.5% / 2.5% class split. Implements four GMM variants (univariate → multivariate mixture) and evaluates on AUC and F1. Best model achieves strong separation using two features and two components per class.

---

### Dimensionality Reduction with PCA and SVD
**`pca_svd_gdp_electricity.ipynb`** · PCA · SVD · Time Series

Applied to World GDP (179 countries × 52 years) and US Electricity Sales (62 states × 24 years). 4 components capture 99.9% of variance in the GDP dataset. PCA and SVD produce identical results; SVD is faster. Incremental reconstruction quantified with RMSE.

---

### Linear Regression & Gradient Descent
**`linear_regression_grid_stability.ipynb`** · Linear Regression · Optimisation

Predicts grid stability on 10,000 simulated power-grid instances. Compares closed-form solution, full-batch GD, and mini-batch GD across a batch size sweep (1–128) and learning rate sweep (0.001–0.2). Optimal config: batch 32, α = 0.05 — 5× faster than the default with identical RMSE.

---

## Stack

Python · NumPy · pandas · scikit-learn · SciPy · matplotlib
