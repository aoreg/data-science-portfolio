# PySpark Analytics & Movie Recommender System

**Stack:** Apache Spark · PySpark MLlib · Python

---

## Part A — Distributed Data Analysis

Three PySpark analysis tasks on text datasets:

| Task | Description |
|---|---|
| Integer parity | Count odd vs even integers using Spark transformations |
| Salary aggregation | Per-department total, mean, median, stddev from salary data; histogram and boxplot |
| Word frequency | Keyword count + top/bottom 10 word frequencies on Shakespeare corpus |

---

## Part B — Movie Recommender System (ALS)

Collaborative filtering on a MovieLens-style ratings dataset using PySpark's Alternating Least Squares algorithm.

| Step | Description |
|---|---|
| EDA | Rating distribution, top-10 movies by average rating, user activity |
| Baseline ALS | Train/test split evaluation across split ratios |
| Error metrics | RMSE, MAE, precision, recall (binary relevance threshold) |
| Hyperparameter tuning | CrossValidator with ParamGrid over rank, maxIter, regParam |
| Recommendations | Personalised top-N recommendations for target users |

---

## Files

```
MIE1628/
├── pyspark_analytics_recommender.ipynb
```

---

## Stack

Python · PySpark · PySpark MLlib (ALS) · pandas · matplotlib
