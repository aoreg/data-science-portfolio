# Global GDP & US Electricity: Dimensionality Reduction with PCA and SVD

**Dataset 1:** World GDP — 179 countries × 52 years (1970–2021)
**Dataset 2:** US Electricity Sales — 62 states × 24 years (2001–2024)

**Goal:** Reduce high-dimensional time-series data using PCA and SVD, compare the two methods, and reconstruct individual series from a compressed representation.

---

## Approach

Both datasets are treated as matrices where rows are entities (countries or states) and columns are time steps. Dimensionality reduction is applied to find the directions of maximum variance across entities over time.

| Step | Description |
|---|---|
| Centering | Subtract column means to remove time-level trends |
| PCA | Eigen-decomposition of the covariance matrix |
| SVD | Direct factorisation of the data matrix |
| Scree plot | Cumulative variance explained vs. number of components |
| Reconstruction | Incrementally rebuild individual series using 1–N components |

---

## Key Findings

- **4 principal components** capture 99.9% of variance in the GDP dataset — global economic output is highly correlated across countries
- PCA and SVD produce identical principal components; SVD is faster because it skips explicit covariance matrix computation
- Reconstruction with 8–16 PCs closely recovers individual country and state series with low RMSE
- The first PC in both datasets captures the dominant global/national trend; subsequent PCs capture regional or sector-specific deviations

---

## Files

```
APS1070/
├── pca_svd_gdp_electricity.ipynb     # Full notebook
└── data/
    ├── domestic_product.csv          # World GDP dataset
    └── electricity_prices.csv        # US electricity sales dataset
```

---

## Stack

Python · NumPy · pandas · matplotlib
