# Rossmann-Retail_Sales_prediction
This repository contains the code and documentation for the Rossman Sales Prediction project. The goal of this project is to forecast the daily sales of Rossmann stores for up to six weeks in advance. By accurately predicting sales, store managers can make informed decisions regarding promotions, competition, holidays, and other factors that influence sales performance.

# Problem Statement and Project Description

Retail Sales Prediction is a regression machine learning project. Rossmann operates over 3,000 drug stores in 7 European countries. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance. Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied. You are provided with historical sales data for 1,115 Rossmann stores. The task is to forecast the "Sales" column for the test set. Note that some stores in the dataset were temporarily closed for refurbishment.

#Project Files Description

This project contains two executable file, a technical document and a presentation as follows:

## Executable Files:

- Regression Problem - Rossmann Retail Sales Prediction_Final_1.ipynb - Collab notebook containing data summary, exploration, visualisations and modeling.
-Regression Problem - Rossmann Retail Sales Prediction_Part2.ipynb - Collab notebook containg model hyperparameter tuning, Cross-validation, model performance, evaluation and conclusion.

# Project Summary

The Rossman Sales Prediction project involved extensive data analysis, feature engineering, and model selection to accurately forecast sales. Here is a brief overview of the project steps and key findings:

## Data Gathering and Cleaning:

Collected historical sales data for Rossmann stores, including competitor details, holidays, customer count, and daily sales.
Performed data cleaning to handle missing values and ensure data consistency.

## Exploratory Data Analysis (EDA):

- Conducted in-depth EDA by exploring univariate, bivariate, and multivariate relationships.
- Generated insightful visualizations to uncover patterns and trends in the data.
- Extracted meaningful insights to inform future decision-making in the machine learning pipeline.

## Feature Engineering and Preprocessing:
- Split the preprocessed data into two parts namely 'unseen_data' and 'new_data'. 
- unseen_data - This dataset consists of last six weeks data.
- new_data - This dataset consists of all other data except last six weeks data.
- Created additional features such as PromoDuration and CompetitionDurationMonths,Average_Customer_Week, Average_Customer_Month in both datasets to capture relevant information.
- Addressed multicollinearity among independent variables.
- Bussiness filters based on categorical and numerical features are made by applying IQR technique on new_data, then the same filters are applied on the unseen_data.
- Encoded categorical variables using One-Hot Encoding for compatibility with machine learning algorithms.
- Applied various transformation techniques to achieve normal distribution of data.

## Model Selection and Training:
- unseen_data was splitted into 80:20 ratio to create X_train and X_loc_test.
- The X_loc_test is again splitted into 50:50 ratio to create val_data and test_data.
- Created several base models based on algoriths such as Decission tree regressor, XGboost regressor, LGB regressor and Random forest regressor.
- Random forest regressor is selected as final model based on the performance metrics such as MSE, RMSPE, R^2 values.
- Hyper parameter tunning was performed on the selected model(random forest regressor) which helped in improving the model performance further.
- Inorder to generalise the performance of the tunned model Cross-validation is also performed.
Following result is achived in the unseen_data using tunned model:

|   Algorithm                     | MSE_Score | RMSPE_Score | R2_Score |
|---------------------------------|-----------|-------------|----------|
| RandomForestRegressor(BaseModel)| 3.576360  | 0.042206    | 0.945452 |
| RandomForestRegressor1          | 3.567391  | 0.042098    | 0.945725 |
| RandomForestRegressor2          | 3.564572  | 0.042056    | 0.945811 |






 
