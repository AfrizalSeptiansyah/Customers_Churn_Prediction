# Project Title

Customers Churn Prediction 

## Description

In this project I use the XGBoost algorithm to predict whether customers will churn : yes or no (imbalanced case). Successfully found important features that managed to increase prediction accuracy.

Dataset Link : https://www.kaggle.com/c/customer-churn-prediction-2020

## Getting Started

### Installing

* Miniconda 
```
conda install -c conda-forge xgboost
```

### Executing program

* Run program sequentially

# Step By Step Solve Problem 

## Baseline 
I created a baseline using automl to assess the feasibility of the data. I use the f1 score as a metric considering there are imbalance case.

![label distribution](https://github.com/AfrizalSeptiansyah/Costumers_Churn_Prediction/blob/main/asset/result_prophet.png?raw=true)


## Exploratory Data Analysis 
I do exploratory data analysis of all numeric and categorical features to gain insight of data. 


## Build Model 
I use XGBoost as a predictive model with the following steps:
* Preprocessing data such as handle missing value and one hot encoding. 
* I did hyperparameter tuning on XGBoost using RandomSearchCV with 5 cross validation.
* After training the model, I visualized the important features and selected the 8 most important features. After that, I retrained the model and added polynomials to improve accuracy.

Gambar 

## Evaluation 

Classification report 

Confusion matrix 

Roc Auc 


## Deployment 

I use flask framework and deploy using heroku service. <br>
Template Link : https://colorlib.com/wp/template/contact-form-v4/  <br>

Demo Application : https://customers-churn-prediction-xgb.herokuapp.com/?

gambar 

# Conclusion
sampaikan kesimpulan-kesimpulan penting dan jangan lupa tambahkan strategi bisnis 

