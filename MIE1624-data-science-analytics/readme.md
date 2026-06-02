# MIE1624 – Introduction to Data Science and Analytics

> Fall 2024 · University of Toronto · Python · Jupyter Notebooks

Three assignments covering the full data science workflow: statistical inference, supervised ML classification, and unsupervised clustering.

---

### Developer Salary Analysis: Job Mode & Education Level
**`salary_stats_analysis.ipynb`** · Hypothesis Testing · Bootstrap

Statistical analysis of 65,000+ Stack Overflow survey respondents. Tests whether remote work and education level significantly affect developer salaries using t-tests, ANOVA, and 10,000-sample bootstrap resampling. Remote workers earn ~92% more than in-person ($83k vs $43k); the gap holds under bootstrap even when parametric assumptions are violated.

---

### Developer Salary Prediction: Ordinal Classification
**`salary_prediction_classification.ipynb`** · scikit-learn · Feature Selection

End-to-end ML pipeline predicting compensation buckets from Kaggle survey responses. Chi-square + LassoCV reduce 72 features to ~15; a custom ordinal logistic regression is tuned with GridSearchCV and evaluated with k-fold CV and a confusion matrix.

---

### Data Science Skill Clustering for Curriculum Design
**`skill_clustering_analysis.ipynb`** · Clustering · NLP · OpenAI API

Clusters 14 data science skills from Indeed job postings using 9 engineered features (frequency, salary, demand growth, difficulty, relevance, diversity metrics). Hierarchical and K-Means clustering produce 4 curriculum modules; OpenAI GPT generates course descriptions per cluster.

---

## Stack

Python · NumPy · pandas · scikit-learn · SciPy · NLTK · seaborn · matplotlib · OpenAI API
