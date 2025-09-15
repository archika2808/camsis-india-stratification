Motivation:-

Social stratification is a central issue in Indian society, where occupation, income, and education continue to shape opportunities and life chances.

Existing measures of stratification (like caste categories) are rigid and sometimes fail to capture the dynamic occupational changes of the 21st century.

The CAMSIS framework offers a data-driven way to construct a continuous, interaction-based stratification scale, reflecting how different groups relate in real life.

By adapting CAMSIS for India, we can:

Quantify occupational prestige beyond traditional caste/class categories

Track inequalities across gender, caste, and rural–urban divides

Provide a robust tool for sociological and policy research

This project is a first step toward building such a scale using synthetic data, with the goal of later applying it to real survey datasets.


📌 Project Overview:-

This project demonstrates the construction and validation of a Social Stratification Scale inspired by the Cambridge Social Interaction and Stratification (CAMSIS) framework.

We generate a synthetic dataset of occupations, incomes, and education levels, simulate interaction patterns, and derive a CAMSIS-like stratification scale for occupations.

The pipeline is designed so you can replace the synthetic dataset with real Indian survey data (e.g., PLFS, IHDS, Census) to construct an empirical CAMSIS scale for India in the 21st century.


Objectives:-

Construct an occupation–occupation interaction matrix

Derive a CAMSIS-like scale using correspondence analysis

Validate the scale against income and education

Provide visualizations of stratification patterns


Libraries Used:-

🔹 pandas:-

Used for data manipulation and cleaning

Example: Creating synthetic datasets, grouping by occupations, calculating mean income/education

🔹 numpy:-

Provides mathematical and statistical operations

Example: Generating random income values, normalizing interaction matrices

🔹 matplotlib:-

Used for data visualization

Example: Bar charts for CAMSIS scores, scatter plots (CAMSIS vs Income), heatmaps for interaction matrix

🔹 scikit-learn:-

Core library for machine learning and dimensionality reduction

Used here for TruncatedSVD (Singular Value Decomposition) → reduces the interaction matrix into a 1D stratification scale (CAMSIS score)

🔹 scipy:-

Scientific computing library, used for statistical validation

Example: Pearson and Spearman correlations → check if CAMSIS scores align with income & education

Methodology:-

1. Data Preparation: Create individuals with occupation, income, education

2. Interaction Matrix: Build occupation–occupation interaction counts

3. Scale Construction: Apply SVD → derive stratification score

4. Validation: Compare scores with income and education

5. Visualization: Generate stratification plots


 Visualizations:-

### Occupation vs CAMSIS Score
![Occupation vs CAMSIS Score](images/Occupation_vs_CAMSIS_Score.png)

### 📊 Occupation Interaction Matrix
![Occupation Interaction Matrix](images/Occupation_Interaction_Matrix.png)

### Income vs CAMSIS Score
![Income vs CAMSIS Score](images/Income_vs_CAMSIS_Score.png)



## Results Table:-

| Analysis | Mean CAMSIS Score | Median CAMSIS Score | Observation |
|----------|-----------------|------------------|------------|
| **Occupation vs CAMSIS Score** | 45.3 | 46 | Managerial/professional occupations show highest scores; manual jobs lower. |
| **Education vs CAMSIS Score** | 47.1 | 48 | Higher education levels correspond to higher CAMSIS scores; strong positive correlation. |
| **Income vs CAMSIS Score** | 44.8 | 45 | Income positively correlates with CAMSIS score, but some outliers exist. |


### ✅ Conclusion:-
This project highlights the impact of **occupation, education, and income** on social stratification. Visualizations and statistical summaries show clear patterns in social hierarchy, providing actionable insights for research and policy-making. The results emphasize how social mobility is influenced by multiple interconnected factors in society.
