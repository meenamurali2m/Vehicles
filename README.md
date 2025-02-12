# Vehicles - What drives the price of a car?

## Overview
In this application, you will explore a dataset from Kaggle. The original dataset contained information on 3 million used cars. The provided dataset contains information on 426K cars to ensure speed of processing. Your goal is to understand what factors make a car more or less expensive. As a result of your analysis, you should provide clear recommendations to your client -- a used car dealership -- as to what consumers value in a used car.

## CRISP-DM Framework
To frame the task, throughout our practical applications, we will refer back to a standard process in industry for data projects called CRISP-DM. This process provides a framework for working through a data problem. Your first step in this application will be to read through a brief overview of CRISP-DM here. After reading the overview, answer the questions below.

## Business Understanding
Develop a predictive model to estimate used car prices using a diverse set of independent variables (features) such as make, model, year, mileage, condition, and other relevant attributes. Perform feature selection and importance analysis to identify the most significant factors influencing price variations. Utilize techniques like correlation analysis, feature importance ranking, and possibly dimensionality reduction methods to determine the key drivers of used car prices. The model's performance will be evaluated using appropriate regression metrics, and the results will be interpreted to provide actionable insights for the business.

## Data Understanding
We use several initial EDA methods to understand the dataset and identify the several problems like missing values, null values, and all issues in the data.

## Data Preparation
We handle any integrity issues and cleaning by removing null values, missing values, outliers, change dat types,  the engineering of new features, transformations and general preparation for modeling with sklearn.
1. Delete redundant columns
2. Delete columns with more than 50% null values.
3. Delete rows with null price values, manufacturer, or model 
4. Cleanup outliers
5. Transform categorical columns into numerical columns using James-Stein encoding.
6. Split the dataset into training and testing datasets.

## Visualization
We use visualization on the data columns to understand and visualize the dataset and their correlation.
![Vehicles Price](images/vehicles_price.png)
 
## Modeling

1. Apply PolynomialFeatures for feature expansion.
2. Use SequentialFeatureSelector to select three important features.
3. Set up a linear regression model using a pipeline.
4. Calculate the Mean Squared Error (MSE) between the training and test datasets.
