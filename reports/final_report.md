# Final Report and Code Submission

# Understanding Obesity Through Economic and Environmental Factors

---

## 1. Motivation

Obesity is one of the most widespread global health challenges today, affecting millions of people worldwide and creating major public health concerns. Although obesity is commonly associated with individual lifestyle choices, broader economic and environmental conditions may also influence obesity levels across countries.

In particular, inflation may affect food affordability, consumption behavior, and access to healthier food options. Similarly, fast food availability may shape dietary patterns and eating habits. Countries with easier access to fast food and changing economic conditions may exhibit different obesity patterns.

In this project, I aimed to explore the relationship between inflation rates, fast food availability, and obesity rates across countries by combining multiple global datasets. I investigated whether countries with higher inflation rates and higher fast food density also demonstrate higher obesity rates, and whether these variables can meaningfully explain obesity differences between countries.

By examining these relationships, this project aims to better understand the economic and environmental dimensions of obesity and highlight the complexity of global health inequalities.

---

## 2. Research Questions and Sub-Questions

### Main Question

How do inflation rates and fast food availability affect obesity rates across countries?

### Sub-Questions

- Does higher inflation relate to higher obesity rates?
- Does fast food density increase obesity levels?
- Do countries with higher fast food density exhibit higher obesity rates?
- Can inflation and fast food density together predict obesity rates?
- Are these relationships statistically significant?

---

## 3. Hypotheses

### H1

Countries with higher inflation rates and higher fast food density will tend to have higher obesity rates.

### H2

Higher fast food density per million people is associated with higher obesity rates.

### H3

Higher inflation rates are associated with changes in obesity rates due to changing food affordability and consumption patterns.

### H4

Inflation and fast food density together can partially explain obesity differences across countries through machine learning and regression models.

### H0 (Null Hypothesis)

Inflation rates and fast food density have no statistically significant relationship with obesity rates.

---

## 4. Data Description

| Dataset | Variable(s) | Why Used |
|---|---|---|
| World Bank – Inflation Data | Consumer price inflation (%) | Main economic indicator |
| Our World in Data / WHO – Obesity Data | Adult obesity prevalence (%) | Main dependent variable |
| World Bank – Population Data | Total population | Used for normalization |
| Kaggle – McDonald’s Global Store Dataset | Number of McDonald’s locations by country | Indicator of fast food availability |

### Final Variables Used

- inflation_rate
- obesity_rate
- population
- fast_food_count
- fast_food_per_million

A new variable called `fast_food_per_million` was generated to normalize fast food availability across countries.

---

## 5. Data Source and Collection

All datasets used in this project are publicly available and were collected from reliable international sources.

The datasets were downloaded from:

- World Bank
- Our World in Data
- WHO-based obesity datasets
- Kaggle

The data preparation process included:

- cleaning missing values
- reshaping World Bank datasets
- standardizing country names
- filtering for the year 2022
- merging datasets into a unified dataframe

Additionally, fast food density per million people was calculated to standardize fast food availability across countries.

All data used in this project are aggregated public datasets and do not contain personal information.

---

## 6. Methodology – How the Analysis Was Conducted

The project follows a structured data science workflow combining statistical analysis and machine learning methods.

### Exploratory Data Analysis (EDA)

First, descriptive statistics and visualizations were used to observe relationships between variables.

The following visualizations were created:

- histograms
- scatter plots
- correlation matrix
- boxplots

These visualizations helped identify:

- weak correlations
- distribution patterns
- outliers
- variable dispersion

---

### Hypothesis Testing

Several statistical tests were applied to evaluate whether the observed relationships were statistically significant.

#### Pearson Correlation Tests

Used to test:

- inflation vs obesity
- fast food density vs obesity

#### Independent T-Test

Used to compare obesity rates between:

- countries with high fast food density
- countries with low fast food density

#### Linear Regression Analysis

Used to evaluate the combined explanatory effect of inflation and fast food density.

---

### Machine Learning Methods

The following machine learning models were implemented:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

The models were evaluated using:

- RMSE
- MAE
- R² score

The purpose of the ML models was to investigate whether inflation and fast food density could predict obesity rates across countries.

---

## 7. Findings and Results

The analysis produced several important findings.

- Inflation and obesity showed a very weak relationship.
- Fast food density did not demonstrate a statistically significant relationship with obesity.
- Countries with high fast food density did not significantly differ from countries with low fast food density in terms of obesity rates.
- Machine learning models demonstrated limited predictive performance.

Among the ML models, Random Forest achieved the highest R² score, but the predictive power remained weak overall.

These results suggest that obesity is influenced by more complex economic, social, cultural, and behavioral factors beyond inflation and fast food availability alone.

---

## 8. Expected Results

Initially, it was expected that:

- higher fast food density might correspond to higher obesity rates
- economic pressure and inflation could influence dietary behavior
- machine learning models could partially explain obesity differences across countries

However, the analysis showed that these variables alone are not sufficient to strongly explain obesity differences.

This highlights the complexity of obesity as a global issue and demonstrates the importance of considering additional variables such as:

- income levels
- healthcare systems
- physical activity
- cultural dietary habits
- social inequalities

---

## 9. Limitations and Future Work

This project has several limitations.

- limited number of explanatory variables
- use of country-level aggregated data
- use of a single fast food chain as a proxy
- single-year analysis
- possible socioeconomic confounding factors

Future studies could improve the analysis by including:

- GDP and income variables
- healthcare indicators
- physical activity data
- food consumption patterns
- urbanization indicators
- multi-year time series analysis

These additions may improve both statistical and machine learning performance.

---

## 10. Conclusion

This project explored whether inflation rates and fast food availability are associated with obesity rates across countries.

The results suggest that these variables alone are not sufficient to strongly explain obesity differences. Both the statistical tests and machine learning models demonstrated weak relationships and limited predictive power.

Overall, the project highlights the complexity of obesity as a global issue and demonstrates the importance of combining statistical analysis and machine learning methods when investigating real-world social and health problems.

---

## 11. Code Submission

The GitHub repository includes:

- raw datasets
- processed dataset
- data collection notebook
- EDA notebook
- hypothesis testing notebook
- machine learning notebook
- README.md
- requirements.txt

### Repository Structure

```text
data/
  raw/
  processed/

notebooks/
  01_data_collection.ipynb
  02_eda.ipynb
  03_hypothesis_testing.ipynb
  04_ml_methods.ipynb

README.md
requirements.txt
