---
title: "Human Capital Outcomes: Clustering & Prediction with World Bank Data"
date: 2026-06-09
description: "A Stata 15.1 machine learning project using World Bank Development Indicators to explore, cluster, and predict survival to age 65 across country-year observations."
summary: "A Stata 15.1 machine learning workflow using World Bank Development Indicators to predict survival to age 65 and identify human development profiles."
tags: ["Stata", "Machine Learning", "World Bank", "WDI", "Human Capital", "Regression", "Clustering", "Data Analysis"]
categories: ["Projects"]
showDate: false
showAuthor: false
showReadingTime: false
showTableOfContents: false
showRelatedContent: false
featureimage: "images/projects/world-bank-human-capital-actual-vs-predicted.png"
---

## Overview

This project uses the **World Bank Development Indicators (WDI)** dataset to explore, cluster, and predict human capital outcomes across countries.

The main outcome variable is **survival to age 65**, constructed as the average of female and male survival-to-age-65 indicators. The project was implemented in **Stata 15.1 SE** using a reproducible workflow organized into separate scripts for setup, data cleaning, exploratory analysis, clustering, and prediction modeling.

The analysis combines development indicators related to income, health expenditure, education, infrastructure, demography, technology access, and labor market conditions.

## Tools

Stata 15.1 SE | World Bank Development Indicators | Regression Modeling | K-means Clustering | GitHub | Data Cleaning | Data Visualization



## What I Did

- Imported and cleaned raw World Bank Development Indicators data
- Selected human capital, economic, health, education, infrastructure, demographic, and technology indicators
- Reshaped the WDI data from wide format into a country-year panel structure
- Created a combined survival-to-age-65 response variable from female and male indicators
- Generated log-transformed GDP and health expenditure variables
- Produced exploratory summary tables, missingness checks, correlation matrices, and graphs
- Applied k-means clustering to identify country-year human development profiles
- Built prediction models for survival to age 65 using selected WDI indicators
- Evaluated prediction performance using RMSE and MAE
- Exported regression parameters, model performance tables, prediction outputs, and visualizations

## Project Workflow

Raw WDI data  
→ data import and cleaning  
→ country-year panel construction  
→ exploratory analysis  
→ k-means clustering  
→ prediction modeling  
→ model evaluation  
→ exported tables, graphs, and GitHub documentation

## Data

The project uses World Bank Development Indicators covering selected country-year observations.

The response variable is:

- Survival to age 65

The main predictors include:

- GDP per capita
- Current health expenditure per capita
- Government expenditure on education
- Access to electricity
- Urban population share
- Fertility rate
- Internet use
- Unemployment rate
- Secondary school enrollment
- Log GDP per capita
- Log health expenditure per capita

## Modeling Approach

Three prediction models were developed.

### Model 1: Baseline Economic and Health Model

This model used:

- Log GDP per capita
- Log health expenditure per capita

### Model 2: Full Development Indicators Model

This model used the full set of selected development indicators, including economic, health, education, infrastructure, demographic, technology, and labor market variables.

### Model 3: Parsimonious Social Development Model

This model used a smaller group of predictors focused on income, health expenditure, infrastructure, fertility, internet use, and secondary school enrollment.

## Actual vs Predicted Survival

![Actual vs predicted survival to age 65](/images/projects/world-bank-human-capital-actual-vs-predicted.png)

This graph compares actual survival to age 65 with predicted values from the full model on the test sample. It helps assess how closely the model predictions align with observed outcomes.

## Prediction Error Distribution

![Prediction error distribution](/images/projects/world-bank-human-capital-error-distribution.png)

This chart shows the distribution of prediction errors from the full model. It helps identify whether the model tends to overpredict or underpredict survival outcomes.

## Model Performance

![Model performance comparison](/images/projects/world-bank-human-capital-model-performance.png)

This comparison summarizes model performance using RMSE and MAE. Lower values indicate better prediction performance.

## Clustering Analysis

![Human capital clusters](/images/projects/world-bank-human-capital-clusters.png)

K-means clustering was used to group country-year observations into human development profiles based on survival, income, health expenditure, education, infrastructure, demographic, and technology indicators.

## Key Findings

- Survival to age 65 is strongly related to broader development conditions, including income, health expenditure, education, electricity access, fertility, and internet use
- Log-transformed GDP and health expenditure provide useful predictors for survival outcomes
- Fertility and development-related infrastructure indicators help distinguish human development profiles
- K-means clustering identified groups of country-year observations with different human capital and development characteristics
- Model performance varied across the baseline, full, and parsimonious models, showing the value of comparing multiple prediction specifications
- Exporting regression parameters improved interpretability by showing the direction, magnitude, and statistical significance of predictors

## Skills Demonstrated

- Stata 15.1 project workflow design
- World Bank Development Indicators analysis
- Data cleaning and reshaping
- Country-year panel data preparation
- Feature engineering and log transformations
- Exploratory data analysis
- Missingness analysis
- Correlation analysis
- K-means clustering
- Regression-based prediction modeling
- Train/test split and model evaluation
- RMSE and MAE calculation
- Regression parameter export
- GitHub documentation and reproducible project organization

## Repository

[View the project on GitHub](https://github.com/craigthompsonotieno/worldbank-human-capital-stata-ml)