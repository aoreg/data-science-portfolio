# APS1070 – Foundations of Data Analytics and Machine Learning

> **Fall 2024** · University of Toronto · Jupyter Notebooks · Python

This course covers core ML fundamentals — from EDA and statistical testing to feature engineering and model evaluation.

---

## Projects

### Project 1 – Exploratory Data Analysis
**File:** `F24_APS1070_Project_1_Alton_1004909307.ipynb`
**[Open in Colab](https://colab.research.google.com/drive/1moUwZKV2_MBMBNMzpxdsrtyzeqQ8Z7k4)**

Introductory EDA project covering data cleaning, visualization, and descriptive statistics on a real-world dataset.

---

### Project 2 – Statistical Inference & Hypothesis Testing
**File:** `F24_APS1070_Project_2_Alton_1004909307.ipynb`
**[Open in Colab](https://colab.research.google.com/drive/13kXJMMzDNWWfH1cEstPRF-YfhiKgFrXg)**

Applied statistical tests (t-tests, ANOVA, bootstrapping) to compare salary distributions across job modes and education levels using Stack Overflow survey data.

Key findings:
- Remote workers earn ~$35,000 more on average than in-person workers (p < 0.001)
- Professional degree holders have significantly higher and more variable salaries
- Bootstrapping (10,000 resamples) validated both parametric and non-parametric results

---

### Project 3 – Classification & Feature Engineering
**File:** `F24_APS1070_Project_3.ipynb`
**[Open in Colab](https://colab.research.google.com/drive/14zOJqj-Mr0FDwiqeY39mxJy1MD8HHWzK)**

Built and tuned multi-class ordinal classification models to predict Kaggle survey respondents' annual compensation bucket.

Steps included:
- Data cleaning: dropped irrelevant columns, imputed missing values, label + one-hot encoded features
- Feature selection using Chi-square tests and Lasso regression (10-fold CV)
- Feature engineering: created Experience_Education interaction term and Total_Skills aggregate
- Ordinal logistic regression with bias-variance analysis and hyperparameter tuning
- Evaluation with Precision, Recall, F1-score (macro and weighted) due to class imbalance

---

### Project 4 – Advanced Modelling
**File:** `F24_APS1070_Project_4.ipynb`
**[Open in Colab](https://colab.research.google.com/drive/12zW_cM_KajsEfN7yZo7u-PCduo-b27-g)**

Extended modelling work applying more advanced techniques to improve on Project 3's ordinal classification baseline.

---

## Additional Resources

| Resource | Link |
|----------|------|
| Midterm Prep Notebook | [Open in Colab](https://colab.research.google.com/drive/1FW14jUmcXjtqhZH-pRC1yHYKrvbTsReV) |
| Week 1 Lecture Code | [Open in Colab](https://colab.research.google.com/drive/1lIY_vGGHrNZYXfpkWzfCMIF-N36VE9mz) |
| Week 2 Lecture Code | [Open in Colab](https://colab.research.google.com/drive/1TaJYVIr7SQIsEyYJveknsQlRw5rzHXVS) |
| Tutorial – Python Basics | [Open in Colab](https://colab.research.google.com/drive/18ri62N1DHQm8OxYvxK_VOV13Lp9QEKSV) |
| Tutorial – Basic Data Science | [Open in Colab](https://colab.research.google.com/drive/1WPhig-EQoPXaCNYoLXzYMJYf2DjAX4Ud) |

---

## Skills Developed
- Exploratory data analysis and visualization
- Hypothesis testing (t-test, ANOVA, bootstrapping)
- Feature engineering and selection (Chi-square, Lasso)
- Ordinal logistic regression and multi-class classification
- Bias-variance tradeoff, cross-validation, hyperparameter tuning
