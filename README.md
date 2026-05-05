# Understanding Obesity Through Economic and Environmental Factors

---

## Motivation

Obesity is a growing global health problem that affects millions of people worldwide. While individual lifestyle choices play an important role, obesity is also influenced by broader economic and environmental conditions.

In particular, rising inflation may affect food affordability and consumption patterns, while the availability of fast food may shape dietary habits. Understanding how these macro-level factors relate to obesity can provide insight into global health disparities.

This project aims to explore whether economic and environmental variables, such as inflation and fast food availability, are associated with obesity rates across countries.

---

## Research Questions and Sub-Questions

### Main Research Question

- Is there a relationship between inflation rates, fast food availability, and obesity rates across countries?

### Sub-Questions

- Is there a statistically significant relationship between inflation and obesity?
- Does fast food density correlate with obesity rates?
- Is there a difference in obesity levels between countries with high and low fast food availability?
- Can inflation and fast food availability together predict obesity rates?

---

## Hypotheses

The following hypotheses are tested:

### Inflation and Obesity

- **H0 (Null Hypothesis):** There is no relationship between inflation and obesity.
- **H1 (Alternative Hypothesis):** There is a relationship between inflation and obesity.

### Fast Food and Obesity

- **H0:** There is no relationship between fast food density and obesity.
- **H1:** There is a relationship between fast food density and obesity.

### Group Comparison

- **H0:** There is no difference in obesity rates between countries with high and low fast food density.
- **H1:** There is a difference.

---

## Data Description

The final dataset includes country-level observations for a selected year (2022). The variables used in the analysis are:

- country  
- inflation_rate  
- obesity_rate  
- population  
- fast_food_count  
- fast_food_per_million  

A new variable, **fast_food_per_million**, was created to standardize fast food availability across countries.

---

## Data Sources and Collection

The data was collected from multiple publicly available sources:

- **Inflation Data:** World Bank (consumer price inflation)
- **Obesity Data:** Our World in Data (WHO-based obesity estimates)
- **Population Data:** World Bank
- **Fast Food Data:** McDonald's global store dataset (Kaggle)

Data collection involved:

- downloading datasets from official sources  
- cleaning and standardizing formats  
- merging datasets based on country  
- filtering for a common year  
- computing derived variables  

---

## Methodology

The project follows a structured data science workflow:

### 1. Data Collection and Cleaning
- Raw datasets were cleaned and standardized
- Missing values were handled
- Data was merged into a unified dataset

### 2. Exploratory Data Analysis (EDA)
- Distribution analysis using histograms
- Scatter plots to explore relationships
- Correlation matrix
- Outlier detection

### 3. Hypothesis Testing
- Pearson correlation tests
- Independent t-test
- Linear regression analysis

### 4. Machine Learning Methods
- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

Model performance was evaluated using RMSE, MAE, and R².

---

## Expected Results

Based on initial exploration, it is expected that:

- The relationship between inflation and obesity will be weak or insignificant
- Fast food density alone will not strongly explain obesity rates
- Machine learning models will have limited predictive power
- Obesity will likely depend on additional factors not included in this dataset

---

## Conclusion

The results of this project suggest that inflation and fast food availability alone are not sufficient to explain differences in obesity rates across countries.

This highlights the complexity of obesity as a global issue and suggests that additional variables, such as income, lifestyle, and healthcare systems, should be considered in future analyses.

---

## Important Note

Correlation does not imply causation.  
The relationships observed in this study are exploratory and do not represent causal effects.


