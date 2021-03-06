# Telco Project

### In this project, I try to understand the customer churn rate of a fictional telco company that provides home phone and Internet services to 7,043 customers in California in Q3 based on 33 features. This project is based on a Kaggle challenge (https://www.kaggle.com/blastchar/telco-customer-churn). This project was conducted independently during June 2021.

## Problem Description
I try to answer the following questions:
1. How to predict a customer's churn rate? What are the most important features that predict the churn rate?

## Data Description
The cross-sectional dataset contains 7,043 observations and 33 features. It contains whether the customer has left the company in the past month, the services that the customer signed up for, payment method, and demographics. Please refer to **Data Description.txt** for detailed data description.

## Business Insights:
1. Month-to-Month Contract is bad for retaining customers.
2. The Telco company needs to improve its Fiber Optic Internet services.
3. Make technical support an default option can help retain customers.

## Exploratory Data Analysis
I calculate the customer's churn rate from the dataset, and graph the churn rate against different features. Please refer to **Exploratory Data Analysis.ipynb** for full data visualization. Here I discuss some highlights:

Senior Customers have higher churn rates
<p align="center">
<img src="senior.png" alt="Senior Citizen" width="700">
  </p>

Customers under Month-to-Month Contracts have higher churn rates
<p align="center">
<img src="contract.png" alt="Contract" width="700">
  </p>
  
Customers who signed up for Fiber Optic Internet services have higher churn rates
<p align="center">
<img src="fiber.png" alt="Types of Internet Services" width="700">
  </p>

## Predictive Model
I use various supervised learning models to predict whether the customer will left the Telco comapany or not. The models include: K-Nearest Neighbors, Support Vector Classification, Logistic Regression, Random Forest, AdaBoost, and XGBoost. When evaluating the models, I focus on the Recall metrics. It is very important to identify the customers who actualy leave the company, and Recall exactly captures this focus. The XGBoost model has a recall of 53% and the model AUC is 0.84. 

I use the Shapley Value (https://en.wikipedia.org/wiki/Shapley_value) to find the most important features of the model. I find that Contract type, Internet service type, and technical services are the most important features. I provide the business insights as a result of this analysis.

<p align="center">
<img src="shapley_value.png" alt="Shapley Value" width="700">
  </p>

