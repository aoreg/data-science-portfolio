# Electrical Grid Stability: Linear Regression & Gradient Descent Optimisation

**Dataset:** [Electrical Grid Stability](https://archive.ics.uci.edu/dataset/471/electrical+grid+stability+simulated+data) — 10,000 simulated instances, 12 features describing power grid behaviour (UCI).

**Goal:** Predict continuous grid stability (`stab`) and systematically compare three optimisation approaches for fitting a linear model.

---

## Approach

| Method | Description |
|---|---|
| Direct solution | Closed-form matrix inversion: $w = (X^TX)^{-1}X^Ty$ |
| Full-batch gradient descent | Single weight update per epoch; fixed α = 0.01 |
| Mini-batch gradient descent | Generalised function; batch size sweep from 1 (SGD) to 128 |

Features are standardised before training. A bias column is appended after standardisation to avoid division by zero.

---

## Results

| Method | Val RMSE | Notes |
|---|---|---|
| Direct solution | 0.0219 | Accuracy ceiling; instantaneous |
| Full-batch GD | ~0.0219 | Converges to same RMSE |
| Mini-batch GD (best) | ~0.0218 | Batch 32, α = 0.05, < 2 s |

---

## Key Findings

- The closed-form solution sets the accuracy ceiling — all GD variants converge to the same RMSE
- **Larger batches converge faster in wall-clock time**: batch 32 finishes in ~0.007 s vs. ~265 s for batch 2
- SGD (batch = 1) is unstable at α = 0.01 and diverged at all tested learning rates — noisy gradients prevent stable convergence on this dataset
- Optimal learning rate (α = 0.05) is 5× faster than the conservative default (α = 0.01) with identical final accuracy

---

## Files

```
APS1070/
├── linear_regression_grid_stability.ipynb     # Full notebook
└── data/
    └── electrical_grid_stability_simulated_data.csv
```

---

## Stack

Python · NumPy · pandas · SciPy · scikit-learn · matplotlib
