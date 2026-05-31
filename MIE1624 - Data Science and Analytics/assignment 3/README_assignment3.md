# Data Science Skill Clustering for Curriculum Design

**Dataset:** Web-scraped job postings from Indeed.com — Canadian, US, and remote data science roles.

**Goal:** Cluster 14 data science skills based on features derived from job postings to recommend a structured university course curriculum.

---

## Approach

| Step | Description |
|---|---|
| Skill extraction | Keyword matching across 14 skills in 4 categories |
| Feature engineering | 9 features per skill: frequency, salary, demand growth, difficulty, relevance, job role/industry/location diversity, longevity |
| Hierarchical clustering | Dendrogram with manual cluster refinement |
| K-Means clustering | Elbow method for optimal k; PCA scatterplot for visualisation |
| Curriculum generation | OpenAI GPT API to produce course descriptions per cluster |

**Skill categories:** Programming (Python, MATLAB, Excel, SQL) · Technical (Data Management, Big Data, ML, Modelling) · Business (Project Management, Consulting, Negotiation) · Interpersonal (Teamwork, Creativity, Communication)

---

## Key Findings

- Python and Communication are the highest-frequency, highest-salary skills — any curriculum should prioritise both
- Hierarchical clustering separates programming languages, soft skills, and emerging technical skills into natural groups
- K-Means produced 4 curriculum modules: Core Programming · Technical Depth · Professional Skills · Communication & Collaboration

---

## Files

```
MIE1624/
├── skill_clustering_analysis.ipynb
└── data/
    └── Data_Scientist_Canada_US_Remote.csv
```

> Note: set `OPENAI_API_KEY` environment variable to run the curriculum generation section.

---

## Stack

Python · pandas · NumPy · scikit-learn · SciPy · NLTK · OpenAI API · seaborn · matplotlib
