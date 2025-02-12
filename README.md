# Vehicles - What drives the price of a car?

Code - https://github.com/meenamurali2m/Vehicles/blob/main/prompt_II_MM.ipynb

Dataset - vehicles.csv

## Overview
In this application, you will explore a dataset from Kaggle. The original dataset contained information on 3 million used cars. The provided dataset contains information on 426K cars to ensure speed of processing. Your goal is to understand what factors make a car more or less expensive. As a result of your analysis, you should provide clear recommendations to your client -- a used car dealership -- as to what consumers value in a used car.

## CRISP-DM Framework
To frame the task, throughout our practical applications, we will refer back to a standard process in industry for data projects called CRISP-DM. This process provides a framework for working through a data problem. Your first step in this application will be to read through a brief overview of CRISP-DM here. After reading the overview, answer the questions below.

<img width="374" alt="Image" src="https://github.com/user-attachments/assets/c3c24617-5f6e-4fc7-a9d7-0a7569beec56" />

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

![Image](https://github.com/user-attachments/assets/5ef864a8-c9ce-4862-9485-7ba34a61b3ca)
![Image](https://github.com/user-attachments/assets/b35ac072-cb88-45ad-9810-5a0133d8c30e)
![Image](https://github.com/user-attachments/assets/6f39c388-a66c-4d03-828f-5c4cb41d34f4)
![Image](https://github.com/user-attachments/assets/cf22deab-a304-45f6-9c4f-790d1e02cd07)
![Image](https://github.com/user-attachments/assets/5ce05d71-6f58-4555-b4ff-9d284b77fe21)
![Image](https://github.com/user-attachments/assets/7cd37784-6f43-4eba-ad78-b703b71bb46d)
![Image](https://github.com/user-attachments/assets/83163000-0763-4ea8-bb11-368d185dc35f)



## Modeling
1. Apply PolynomialFeatures for feature expansion.
2. Baseline prediction
3. SequentialFeatureSelector to select the important features
4. Setup regression using pipeline and Make predictions on the test set with the best features selected
5. Calculate the Mean Squared Error (MSE) between the training and test datasets.

## Evaluation
Using the polynomial features and Sequential Feature Selector to select the important features, the MSE is slightly lower on the test set but the RMSE values based on the predictions are off by about 0.92-0.94 units. Used RandomForestRegressor that produced a better outcome of R2 Score: 0.9364 for Log scale and R2 Score: 0.9679 for the original scale. The actual results and the predicted results look pretty close making the accuracy of the model pretty good. 

## Deployment
### 1. Executive Summary
In this report, we provide data-driven insights that can help used car dealers optimize their inventory selection and pricing strategies. By analyzing key variables such as car make, model, odometer, condition, and price, we uncover trends that will allow you to make informed decisions to meet customer expectation and maximize profitability.

### 2. Objective
The primary goal of this analysis is to help your business:

  a. Set competitive prices that attract buyers 
  b. Leverage key data patterns to make informed business decisions

### 3. Methodology
To derive actionable insights, we analyzed historical data from used car sales, including variables like:

  a. Car Make and Model
  b. Odometer
  c. Year of Manufacture
  c. Price
  d. Condition
  e. Make

Our approach involved several data analysis techniques, including:

  a. Exploratory Data Analysis (EDA): To identify trends, correlations, and outliers.
  b. Price Analysis: To establish pricing patterns based on car attributes.
  c. Price Forecasting: To predict the price for most in-demand makes and models

### 4. Key Findings
Several key factor influence the price of the car. Our findings indicate that from a customer's point of view typically they value the odometer reading, year, model, and condition of the car to agree to a price point for buying a car.

### 6. Conclusion
By utilizing the insights gained from this analysis, used car dealers can strategically adjust the inventory, set optimal prices, and better meet customer demand. The key is to stay agile and monitor trends to fine-tune your offerings continuously

