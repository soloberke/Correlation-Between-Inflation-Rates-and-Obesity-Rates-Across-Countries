Understanding Obesity Through Economic and Environmental Factors
Project Overview

Obesity is one of the most widespread global health challenges today, affecting millions of people worldwide and creating major public health concerns. Although obesity is commonly associated with individual lifestyle choices, broader economic and environmental conditions may also influence obesity levels across countries.

This project investigates whether macroeconomic factors such as inflation and environmental factors such as fast food availability are associated with obesity rates across countries.

By combining multiple global datasets and applying statistical analysis together with machine learning methods, the project aims to explore whether these variables can explain or predict obesity levels at a country scale.

Motivation

The motivation behind this project comes from the idea that economic pressure and food accessibility may influence dietary behavior.

Rising inflation can affect:

food affordability
purchasing behavior
consumption habits
access to healthier food options

At the same time, fast food availability may shape eating patterns and nutritional choices.

Although these relationships are frequently discussed in public discourse, their actual statistical relationship across countries is not always clear.

Therefore, this project aims to explore whether inflation rates and fast food density have measurable relationships with obesity rates.

Research Questions

This project focuses on the following research questions:

Is there a relationship between inflation rates and obesity?
Does fast food availability influence obesity rates?
Do countries with higher fast food density exhibit higher obesity levels?
Can inflation and fast food density together predict obesity rates using machine learning models?
Hypotheses
Inflation and Obesity
H0 (Null Hypothesis): There is no relationship between inflation and obesity.
H1 (Alternative Hypothesis): There is a relationship between inflation and obesity.
Fast Food Density and Obesity
H0: There is no relationship between fast food density and obesity.
H1: There is a relationship between fast food density and obesity.
Group Comparison
H0: There is no difference in obesity rates between countries with high and low fast food density.
H1: There is a difference.
Dataset Description

The final dataset contains country-level observations for the year 2022.

The following variables were used in the analysis:

Variable	Description
country	Country name
inflation_rate	Consumer price inflation (%)
obesity_rate	Adult obesity prevalence (%)
population	Total population
fast_food_count	Number of McDonald’s locations
fast_food_per_million	Fast food density normalized by population

A new variable called fast_food_per_million was generated to standardize fast food availability across countries.

Data Sources

The project combines multiple publicly available datasets.

Dataset	Source	Purpose
Inflation Data	World Bank	Inflation analysis
Population Data	World Bank	Population normalization
Obesity Data	Our World in Data / WHO	Obesity prevalence
Fast Food Data	Kaggle	McDonald’s store counts
Data Collection and Preparation

The data collection process involved combining multiple datasets into a unified dataframe.

The preprocessing stage included:

downloading datasets from public sources
cleaning missing values
reshaping World Bank datasets
standardizing country names
filtering for the year 2022
merging datasets
generating derived variables

The final processed dataset was stored as:

merged_dataset.csv
Methodology

The project follows a complete data science workflow.

1. Data Collection and Cleaning

The raw datasets were cleaned and transformed into a consistent format before analysis.

Key preprocessing steps:

handling missing values
reshaping datasets
country-level standardization
merging multiple datasets
creating normalized variables
2. Exploratory Data Analysis (EDA)

EDA techniques were used to visually inspect distributions and relationships between variables.

The following visualizations were created:

histograms
scatter plots
correlation matrix
boxplots

EDA helped identify:

weak correlations
distribution patterns
outliers
variable relationships
3. Hypothesis Testing

Several statistical methods were applied to evaluate whether the observed relationships were statistically significant.

Pearson Correlation Tests

Used to test relationships between:

inflation and obesity
fast food density and obesity
Independent T-Test

Used to compare obesity rates between:

countries with high fast food density
countries with low fast food density
Regression Analysis

Used to evaluate the combined explanatory effect of inflation and fast food density.

4. Machine Learning Methods

Machine learning models were applied to investigate whether inflation and fast food density could predict obesity rates.

The following models were implemented:

Linear Regression
Decision Tree Regressor
Random Forest Regressor

The models were evaluated using:

RMSE
MAE
R² score
Exploratory Data Analysis Findings

The EDA stage suggested that:

inflation and obesity show very weak relationships
fast food density does not visually correlate strongly with obesity
the variables exhibit substantial dispersion across countries

The correlation matrix also indicated weak linear relationships between the variables.

Hypothesis Testing Results

The statistical tests produced weak and statistically insignificant results.

Main findings:

inflation and obesity are not significantly related
fast food density and obesity are not significantly related
countries with high fast food density do not significantly differ from countries with low fast food density

These results suggest that the observed relationships are weak and may not be statistically meaningful.

Machine Learning Results

The machine learning models demonstrated limited predictive performance.

Model Performance Summary
Model	General Performance
Linear Regression	Very weak
Decision Tree	Weak
Random Forest	Best among models, but still limited

Although Random Forest achieved the highest R² score, the overall predictive power remained low.

This indicates that:

inflation and fast food density alone are not sufficient predictors of obesity
obesity is likely influenced by more complex social, cultural, and behavioral factors
Expected Results vs Actual Results

Initially, it was expected that:

higher fast food density might be associated with higher obesity rates
economic pressure could influence dietary behavior and obesity

However, the analysis showed that:

these variables alone do not strongly explain obesity differences across countries
the predictive power of the models remained weak

This highlights the complexity of obesity as a global issue.

Limitations

This project has several limitations:

limited number of explanatory variables
country-level aggregated data
use of a single fast food chain as a proxy
analysis limited to one year
possible cultural and socioeconomic confounding factors
Future Work

Future studies could improve the analysis by including:

GDP and income variables
healthcare indicators
physical activity metrics
food consumption data
urbanization variables
multi-year time series analysis

Additional variables may improve both statistical analysis and machine learning performance.

Project Structure
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
Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
SciPy
Statsmodels
Scikit-learn
Google Colab
Important Note

Correlation does not imply causation.

The relationships observed in this project are exploratory and do not represent causal effects.
