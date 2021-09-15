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
I created a baseline using automl to assess the feasibility of the data. I use the f1 score as a metric considering there are imbalance case. I use class weight to fix it. 

![label_distribution](https://github.com/AfrizalSeptiansyah/Customers_Churn_Prediction/blob/main/asset/label.png?raw=true)


## Exploratory Data Analysis 
I do exploratory data analysis of all numeric and categorical features to gain insight of data. 


## Build Model 
I use XGBoost as a predictive model with the following steps:
* Preprocessing data such as handle missing value and one hot encoding. 
* I did hyperparameter tuning on XGBoost using RandomSearchCV with 5 cross validation.
* After training the model, I visualized the important features and selected the 8 most important features. After that, I retrained the model and added polynomials to improve accuracy.

![features_important](https://github.com/AfrizalSeptiansyah/Customers_Churn_Prediction/blob/main/asset/features_important.png?raw=true)


## Evaluation 

### Classification Report 
![classification_report](https://github.com/AfrizalSeptiansyah/Customers_Churn_Prediction/blob/main/asset/classification_report.PNG?raw=true)

### Roc Auc 
![roc_auc](https://github.com/AfrizalSeptiansyah/Customers_Churn_Prediction/blob/main/asset/roc_auc.png?raw=true)

### Confusion Matrix 
![confusion_matrix](https://github.com/AfrizalSeptiansyah/Customers_Churn_Prediction/blob/main/asset/confusion_,matrix.png?raw=true)


## Deployment 

I use flask framework and deploy using heroku service. <br>
Template Link : https://colorlib.com/wp/template/contact-form-v4/  <br>

Demo Application : https://customers-churn-prediction-xgb.herokuapp.com/?

![app](https://github.com/AfrizalSeptiansyah/Customers_Churn_Prediction/blob/main/asset/app.PNG?raw=true)

# Conclusion
From all the steps that have been done I get an f1 score of 0.88. Managed to get 8 important features used to increase f1 score. At the last stage I deploy so that it can be used by users. So that we can carry out marketing strategies if there are customers who are predicted to leave our services.

Thank you for reading :)
