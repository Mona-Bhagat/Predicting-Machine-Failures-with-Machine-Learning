# Predicting-Machine-Failures-with-Machine-Learning



## Overview
Predicting machine failures using predictive models is a key objective in the realm of Industry 4.0, enabling timely warnings about potential equipment failures, enabling them to proactively schedule maintenance activities and reduce unexpected downtime.

This project explores the application of machine learning and deep learning techniques using **MLP (Artifical Neural Network)**, **XGBoost** and **Random Forest** models to detect potential equipment failures before they occur.

## Dataset 

Dataset is publicly available on UCI Machine Learning Repository. Also couple of versions on Kaggle. Please make sure to use the 10000 rows 14 columns one 

## Approach

Based on literature reading available on predictive maintenance, it was concluded that Artificial Neural Network, XG Boost and Random Forest are known to give the better results amongst machine learning models hence these models weere shortlisted

## Steps

* Importing dependencies, saving into a dataframe and checking of nulls
* Cleaning column names for model readability 
* Splitting the dataset into features and target
* Checking high correlation and dropping one of those sets
* Since Air temperature had high positive corelation with Process temp, Air temp was dropped. Similarly, rotational speed and torque were strongly related (negative), Torque was dropped
* Splitting the data into Train-test
* Deploying under sampling only on the training (as the dataset was highly imbalanced)

* The three models (MLP, XG Boost and Random Forest) were trained with the balanced dataset 
* Since Random Forest had the highest accuracy score (0.85), decent recall (0.77) and highest f-1 score (0.24) across the board it was chosen for further performance improvement by simple hyperparameter tuning ( GridSearchCV )and SMOTE (generate synthetic samples of the minority class - Failures)

## Final Results 

While MLP had the highest recall on failures (0.85) but it suffered from massive false positives (634)

XG Boost also performed well on all parameters but was slightly superseded by Random Forest with final accuracy scores of 83%and 85% respectively 

![image](https://github.com/user-attachments/assets/5ab562c1-59af-4e63-8820-e9aef3261015)


## Acknowledgement

This dataset was originally a part of below publication

S. Matzka, "Explainable Artificial Intelligence for Predictive Maintenance Applications," 2020 Third International Conference on Artificial Intelligence for Industries (AI4I), 2020, pp. 69-74, doi: 10.1109/AI4I49448.2020.00023.





