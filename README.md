# Loan-Default-Prediction
Introduction


Defaulter - customers who are not capable of paying the loan
Non-Defaulter – Customers who are capable of paying the Loan

Goal
The goal of this project is to come up with a loan defaulter prediction model that identify potential customers and predict likelihood of defaulter.

Business Needs
This will enable the loan servicing institution to make decisions on issuing loans, so that the risk can be lowered
The profit can be maximized and  help the marketing team to shift their focus  on those customers who show low risk of defaulting

Data and Population
307511 samples
122 features

Target Definition
         Loan Defaulter- predicts whether an applicant can repay the loan amount or not 
         
Preprocessing steps
Identifying outliers
AMT_ANNUITY, AMT_CREDIT, AMT_GOODS_PRICE,CNT_CHILDREN have some number of outliers.
DAYS_EMPLOYED has outlier values around 350000(days) which is around 958 years which is impossible and hence this has to be incorrect 
entry so we dropped it.
Identifying correlated features
Dropped the correlated Feature
 
Numerical Features
Imputing missing values with median
Scaling is performed using minmax scalar
Categorical Features
Imputing missing values with most frequent category
One hot encoding is performed to convert the categorical values to numerical
Train/Test split-70%/30%

Tested Models
Logistic Regression
Decision Tree
Random Forest Classifier
XGBoost Classifier

XGBoost Classifier is a good fit model with higher roc_auc score

Model Optimization steps

Hyperparameter tuning has been performed
Best model parameters are selected 
Fitted the selected parameters and selected features to the model
Final performance score is 0.749 roc_auc for the test dataset 








