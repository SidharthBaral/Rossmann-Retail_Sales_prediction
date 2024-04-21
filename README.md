# Rossmann-Retail_Sales_prediction
This repository contains the code and documentation for the Rossman Sales Prediction project. The goal of this project is to forecast the daily sales of Rossmann stores for up to six weeks in advance. By accurately predicting sales, store managers can make informed decisions regarding promotions, competition, holidays, and other factors that influence sales performance.

# Problem Statement and Project Description

Retail Sales Prediction is a regression machine learning project. Rossmann operates over 3,000 drug stores in 7 European countries. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance. Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied. You are provided with historical sales data for 1,115 Rossmann stores. The task is to forecast the "Sales" column for the test set. Note that some stores in the dataset were temporarily closed for refurbishment.

#Project Files Description

This project contains two executable file, a technical document and a presentation as follows:

## Executable Files:
Regression Problem - Rossmann Retail Sales Prediction_Final_1.ipynb - Collab notebook containing data summary, exploration, visualisations and modeling.
Regression Problem - Rossmann Retail Sales Prediction_Part2.ipynb - Collab notebook containg model hyperparameter tuning, Cross-validation, model performance, evaluation and conclusion.

# Project Summary

The Rossman Sales Prediction project involved extensive data analysis, feature engineering, and model selection to accurately forecast sales. Here is a brief overview of the project steps and key findings:

Data Gathering and Cleaning:

Collected historical sales data for Rossmann stores, including competitor details, holidays, customer count, and daily sales.
Performed data cleaning to handle missing values and ensure data consistency.

Exploratory Data Analysis (EDA):

Conducted in-depth EDA by exploring univariate, bivariate, and multivariate relationships.
Generated insightful visualizations to uncover patterns and trends in the data.
Extracted meaningful insights to inform future decision-making in the machine learning pipeline.
Feature Engineering and Preprocessing:

Created additional features such as PromoDuration and CompetitionDuration to capture relevant information.
Addressed multicollinearity among independent variables using variance inflation factor (VIF) analysis.
Detected and treated outliers using the Interquartile Range (IQR) technique.
Encoded categorical variables using One-Hot Encoding for compatibility with machine learning algorithms.
Applied various transformation techniques to achieve normal distribution of data.
Model Selection and Training:

Split the preprocessed data into training and testing sets.
Utilized a variety of machine learning algorithms, including linear regression, decision trees, random forests, LightGBM, and XGBoost.
Evaluated model performance using metrics such as R-squared score, accuracy, and mean absolute percentage error (MAPE).
Employed regularization techniques (e.g., Lasso, Ridge, Elastic Net) for improved model performance.
Identified XGBoost as the optimal model due to its high accuracy, with an MAPE of only 2% and an R-squared score of 0.94.

 
