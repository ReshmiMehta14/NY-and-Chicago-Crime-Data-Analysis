# NY-and-Chicago-Crime-Data-Analysis
## Introduction
This project focuses on analyzing crime data from two major US cities: Chicago and New York. The aim is to predict crime occurrences and understand the factors influencing arrest rates using various machine learning techniques.

## Problem Statement
1. How can we predict crimes in cities using data from New York and Chicago?
2. To what extent do factors such as district and crime type contribute to the variability in arrest numbers?
3. How does the incidence of specific crime types (Homicide, Assault, Robbery, Arson, etc.) vary across different time periods?
Methodology

## Theoretical Explanation
We used supervised learning (regression) to analyze the correlation between crime rates and indicators like law code, jurisdiction code, and geographical locators (e.g., district code, latitude, longitude). Random Forest and XGBoost were employed to capture complex relationships, while ARIMA models were used for time series analysis.

## Importance of This Topic
This analysis can be used in:

- Public Safety and Policy Making
- Business Operations
- Urban Planning
- Healthcare and Emergency Services
- Resource Allocation
- Social Impact
- Insurance and Risk Management
- Technology and Innovation

## Data Preparation

### Dataset Source Information
**Chicago**

Dataset Name: Crimes - 2001 to Present

Source: The City of Chicago's open data portal (https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-present/ijzp-q8t2)

Date Range: 01/01/2001 to 12/31/2023

Shape: 8,009,594 rows, 22 columns


# 
**New York**

Dataset Name: NYPD Arrest Data (Year to Date)

Source: NYC Open Data (https://data.cityofnewyork.us/Public-Safety/Police-Precincts/78dh-3ptz)

Date Range: 01/01/2023 to 12/31/2023

Shape: 226,855 rows, 19 columns

Notes: The Chicago dataset includes crime incidents with an indication of whether an arrest occurred. For comparison with the New York dataset, which only includes arrest data, we filtered out incidents in Chicago where no arrest was made.


## Machine Learning Models and Analysis
**Regressions:**
Helps answer the question "How do factors like "District" and "Crime Type" influence the likelihood of an arrest?
To what extent do factors contribute to the variability in arrest numbers?"

**Random Forest:**
Helps answer the question " How does the incidence of specific crime types vary across different time periods?"

**ARIMA Model:**
Helps answer the Temporal analysis of crime data.


## Key Findings
### Comparative Analysis
- The district and primary crime type in Chicago data are closely correlated with the likelihood of an arrest occurring, achieving a model accuracy over 86% using logistic regression.
- Narcotics-related crimes have the highest number of arrests in the Chicago dataset.
- Assault-related crimes have the highest number of arrests in the New York dataset.
- Robbery is the most frequent crime type in New York, while Assault is the most common in Chicago.

### Temporal Analysis
- Overall crime counts in Chicago have been decreasing from 2004 to 2024, but homicides have been increasing.
- Narcotics crimes in Chicago have experienced the most significant decrease, followed by Battery and Theft.
- July has the highest monthly crime counts in Chicago.

### Spatial Analysis
- Dangerous drug offenses in New York have shown the most significant increase and intensification among the top five crime categories.


1. **Logistic Regression**:
   - **Accuracy**: 86.66%
     - The model correctly predicts whether an arrest will occur in about 86.66% of cases.
   - **Mean Squared Error**: 18,813,783.28
   - **R-squared**: 66.08%
     - This indicates that approximately 66% of the variability in the crime data can be explained by the model.

2. **Random Forest**:
   - **Mean Squared Error**: 18,813,783.28 after 3 rounds
   - **R-squared**: 66.08%
     - The Random Forest model also shows that around 66% of the variability in the crime data is explained by the model.

3. **ARIMA**:
   - The ARIMA models showed varied AIC and BIC values across different crime types, indicating significant differences in model fit and complexity among the crime categories.

#### New York

1. **Linear Regression**:
   - **Mean**: 18,139.37
   - **Mean Squared Error**: 1,404,165,829.68
     - This high MSE indicates poor model performance.
   - **R-squared**: -0.27
     - The negative R-squared value suggests that the model does not explain the variability in the data well.

2. **Random Forest**:
   - **Mean Squared Error**: 27,125,372.48 after 3 rounds
   - **R-squared**: -0.27
     - The negative R-squared value indicates poor performance for the New York dataset in this context.
