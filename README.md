# Data Science Portfolio - Alton Rego

Hey, I'm Alton. This repo tracks my learning and projects in Data Science, spanning graduate coursework at the University of Toronto and independent study. Projects cover statistical analysis, machine learning, cloud analytics, and blockchain/fintech.

---

## Table of Contents

- [Courses](#courses)
- - [Projects](#projects)
  - - [Skills and Tools](#skills-and-tools)
   
    - ---

    ## Courses

    | Course | Title | Year |
    |--------|-------|------|
    | APS1070 | Foundations of Data Analytics and Machine Learning | Fall 2024 |
    | MIE1624 | Introduction to Data Science and Analytics | Fall 2024 |
    | MIE1628 | Cloud Analytics | Fall 2025 |
    | APS1050 | Blockchain and Bitcoin | Fall 2025 |

    ---

    ## Projects

    ---

    ### APS1070 - Foundations of Data Analytics and Machine Learning

    Fall 2024 - Jupyter Notebooks - Python

    Four projects building up core ML fundamentals, from EDA and statistical testing to feature engineering and model evaluation.

    #### Project 1 - Exploratory Data Analysis

    F24_APS1070_Project_1_Alton_1004909307.ipynb

    Introductory EDA project covering data cleaning, visualization, and descriptive statistics on a real-world dataset.

    #### Project 2 - Statistical Inference and Hypothesis Testing

    F24_APS1070_Project_2_Alton_1004909307.ipynb

    Applied statistical tests (t-tests, ANOVA, bootstrapping) to compare salary distributions across job modes (remote vs. in-person) and education levels using Stack Overflow survey data. Key findings:
    - Remote workers earn ~$35,000 more on average than in-person workers (p less than 0.001)
    - - Professional degree holders have significantly higher and more variable salaries than Bachelor's and Master's degree holders
      - - Bootstrapping with 10,000 resamples validated both parametric and non-parametric results
       
        - #### Project 3 - Classification and Feature Engineering
       
        - F24_APS1070_Project_3.ipynb
       
        - Built and tuned multi-class ordinal classification models to predict Kaggle survey respondents' annual compensation bucket. Steps included:
        - - Data cleaning: dropped irrelevant columns, imputed missing values, label and one-hot encoded categorical features
          - - Feature selection using Chi-square tests and Lasso regression with 10-fold CV
            - - Feature engineering: Experience_Education interaction term and Total_Skills aggregate
              - - Ordinal logistic regression with bias-variance analysis and hyperparameter tuning
                - - Evaluation with Precision, Recall, F1-score (macro and weighted) due to class imbalance
                 
                  - #### Project 4 - Advanced Modelling
                 
                  - F24_APS1070_Project_4.ipynb
                 
                  - Extended modelling work applying more advanced techniques to improve on Project 3's ordinal classification baseline.
                 
                  - ---

                  ### MIE1624 - Introduction to Data Science and Analytics

                  Fall 2024 - Jupyter Notebook and Reports - Python

                  #### Assignment 1 - Salary Analysis: Job Mode and Education Level

                  rego_1004909307_assignment1.ipynb

                  Statistical analysis of developer salaries from the Stack Overflow Annual Developer Survey, examining the impact of job mode (remote, hybrid, in-person) and education level (Bachelor's, Master's, Professional) on compensation. Techniques: descriptive statistics, t-tests, ANOVA, bootstrapping, outlier detection (IQR method), Shapiro-Wilk normality test, Levene's variance test.

                  #### Assignment 2 - Salary Prediction: Multi-Class Ordinal Classification

                  rego_1004909307_assignment2.ipynb

                  Trained, validated, and tuned multi-class ordinal classification models to predict a survey respondent's compensation bucket from Kaggle survey responses. Covered full ML pipeline: data cleaning, EDA, feature selection (Chi-square + Lasso), model training, bias-variance analysis, hyperparameter tuning, and evaluation.

                  ---

                  ### MIE1628 - Cloud Analytics

                  Fall 2025 - Jupyter Notebooks and Reports - Python - Cloud

                  Five assignments covering cloud-based analytics, distributed computing, and data pipeline concepts.

                  | Assignment | Description |
                  |------------|-------------|
                  | Assignment 1 | MIE1628-a1.ipynb - Foundational cloud analytics setup and data exploration |
                  | Assignment 2 | Cloud data processing pipeline |
                  | Assignment 3 | Distributed analytics and querying |
                  | Assignment 4 | Advanced cloud ML workflow |
                  | Assignment 5 | Assignment 5.ipynb - Culminating cloud analytics project |

                  ---

                  ### APS1050 - Blockchain and Bitcoin

                  Fall 2025 - Reports and Analysis - Python

                  Exploration of blockchain technology and decentralized finance through a series of assignments and a final project.

                  | Assignment | Description |
                  |------------|-------------|
                  | Assignment (Sept 19) | Introduction to blockchain concepts |
                  | Assignment (Sept 26) | Bitcoin fundamentals |
                  | Assignment (Oct 4) | Blockchain architecture deep dive |
                  | Assignment (Oct 9) | Cryptographic protocols |
                  | Assignment (Oct 10) | Blockchain implementation analysis |
                  | Assignment (Oct 17) | DeFi and smart contracts |
                  | Ethereum MetaMask Assignment | Hands-on wallet setup and transaction analysis |
                  | Final Project | Comprehensive blockchain and Bitcoin analysis |

                  ---

                  ### Bank Marketing - Independent Project

                  Fall 2025 - Jupyter Notebook - Python

                  Bank Marketing.ipynb

                  Independent data science project applying classification techniques to a bank marketing dataset to predict term deposit subscription. Part of a self-directed Data Science Mission learning track.

                  ---

                  ## Skills and Tools

                  **Languages:** Python, SQL
                  **Libraries:** pandas, NumPy, scikit-learn, matplotlib, seaborn, SciPy
                  **Methods:** EDA, hypothesis testing (t-test, ANOVA, bootstrapping), feature engineering, Lasso regression, ordinal logistic regression, cross-validation, hyperparameter tuning
                  **Cloud:** Cloud analytics platforms (MIE1628)
                  **Other:** Blockchain/DeFi fundamentals, Ethereum/MetaMask
                  **Tools:** Jupyter Notebook, Google Colab, Git

                  ---

                  *Updated May 2026*
