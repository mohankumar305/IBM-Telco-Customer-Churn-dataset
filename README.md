# IBM-Telco-Customer-Churn-dataset
This project explores how machine learning can be used to predict customer churn for a telecom company and explain why the model makes each prediction. Instead of treating the model as a black box, the goal is to understand the key factors that influence customer decisions, both at the overall (global) level and for individual customers (local level).

The dataset used for this project is the IBM Telco Customer Churn Dataset, which is downloaded automatically from Google using a direct link.

## 1. Project Objective

The main aim of the project is to:

Build a strong churn prediction model using XGBoost

Handle class imbalance properly

Use SHAP (SHapley Additive exPlanations) to interpret the model

Identify the top features that cause churn

Explain the predictions for three specific customers:

One high-risk customer

One low-risk customer

One borderline customer

The final output should help a telecom business understand why customers leave and what actions could reduce churn.

## 2. Dataset

The dataset is directly loaded from this public Google URL:

"https://raw.githubusercontent.com/IBM/telco-customer-churn-on-icp4d/master/data/Telco-Customer-Churn.csv"

It contains information about:

Customer demographics

Contract types

Billing and payment patterns

Services they use

Whether they churned or not

A few columns (TotalCharges, customerID) require cleaning before training the model.

## 3. Approach

### a. Preprocessing

* Missing values in TotalCharges were fixed

* Categorical features were label-encoded

* The dataset was split into train and test sets

* Imbalance in the target variable was handled using scale_pos_weight

### b. Model

* The XGBoost classifier was chosen because:

* It handles tabular data well

* It naturally works with SHAP

* It performs strongly on churn datasets

* The model was trained with tuned parameters.

### c. Evaluation

* The following metrics were calculated:

* Accuracy

* F1-Score

* AUC

* Classification Report

These help judge how well the model performs overall.

## 4. SHAP Explainability

SHAP was used for two main purposes:

### 1. Global Interpretation

To understand which features the model finds most important.
The following visualizations were produced:

* SHAP Summary Plot

* SHAP Bar Plot

* Top 10 Feature Ranking

Examples of important features include:

* Contract Type

* Monthly Charges

* Tenure

* Payment Method

*Internet Service Type

These show what drives churn across the entire customer base.

### 2. Local Interpretation

Three specific customers were selected:

* Highest churn probability

* Lowest churn probability

* Middle (borderline) churn probability

For each of them:

* SHAP force plots were created

* Dependence plots were reviewed

* A written explanation was provided describing why that customer did or did not churn


## 5. Deliverables

The project includes:

### 1.Complete Python code for:

* Data loading

* Preprocessing

* Model training

* SHAP global and local explanations

### 2.Technical Summary

* Model architecture

* Evaluation metrics

* Interpretation of top SHAP features

### 3.Local Explanation Summary

* A plain-English explanation of the three selected customers

### 4.Top 10 Feature Importance List

* With SHAP impact descriptions
