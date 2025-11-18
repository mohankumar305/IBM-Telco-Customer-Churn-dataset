Telco Customer Churn Prediction
Project Overview
This project aims to predict customer churn for a telecommunications company using an interpretable machine learning model. The goal is to accurately identify which customers are likely to leave, allowing for targeted retention efforts. The model is built on the IBM Telco Customer Churn dataset (OpenML data_id=42178), which includes demographic, service usage, and billing information.

Key Features
Data preprocessing including missing value imputation and categorical encoding.

Handling class imbalance with SMOTE for improved minority class prediction.

Use of XGBoost classifier with hyperparameter tuning via GridSearchCV.

Model evaluation using ROC AUC, F1-score, classification report, and confusion matrix.

Comprehensive explainability with SHAP, including global feature importance and local individual prediction explanations.

Technologies Used
Python 3

XGBoost for machine learning modeling

SHAP for model interpretability and feature attribution

Scikit-learn for preprocessing, metrics, and model tuning

Imbalanced-learn for SMOTE oversampling

Matplotlib for visualization

Getting Started
Installation
Clone the repository:

text
git clone <repository-url>
cd telco-customer-churn
Install dependencies:

text
pip install -r requirements.txt
Running the Model
Run the main Jupyter notebook customer_churn_prediction.ipynb which includes:

Data loading and cleaning

Feature engineering and encoding

Model training and hyperparameter tuning

Model evaluation on test data

SHAP-based interpretation for global and local explanations

Outputs
AUC and F1-score metrics reflecting model performance

Classification report and confusion matrix

Global SHAP summary plots (dot and bar)

Plain text top 10 feature importance list with SHAP impact values

Local SHAP explanations with quantitative interpretation for example customers

Results
The best model achieved an AUC score of approximately 0.84 on the test set.

F1-score optimized at a chosen classification threshold of 0.3 was approximately 0.59.

Top predictors of churn include contract type (Month-to-month), tenure, and monthly charges.

Local explanations clarify how individual features push predictions up or down for specific customers.

