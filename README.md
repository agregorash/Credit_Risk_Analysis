# Credit Risk Analysis using Supervised Machine Learning

## Overview

The purpose of this analysis is to create a machine learning model that will best predict results for an unbalanced classification problem, credit card risk.  Good loans typically outnumber risky loans.  This is mirrored in the dataset we are using from LendingClub.  In order to find the model that best predicts loan outcomes based on the given factors, we must first prepare the data and apply statistical reasoning for each of our six machine learning models using a few different approaches or combination of approaches. 

**-Naive Random Oversampling**

**-SMOTE Oversampling**

**-Undersampling using ClusterCenteroids**

**-SMOTEENN Under and Oversampling**

**-Balanced Random Forest Classifier**

**-Easy Ensemble AdaBoost Classifier**
 
## Results 

- The dataset was first prepared by converting string values into numerical values 

- The dataset was then split into training(75%) and testing(25%) variables 

- The dataset was then passed through the following 6 machine learning models

### Naive Random Oversampling

- In order to balance the dataset we oversampled high risk applicants using RandomOverSampler before training the Logistic Regression model using this resampled data.

![randOver.PNG](https://github.com/agregorash/Credit_Risk_Analysis/blob/main/images/randOver.PNG)

**-Balanced Accuracy Score: 0.6347**

### SMOTE Oversampling

- The dataset was also oversampled in this model, but using SMOTE as opposed to RandomOverSampler

![SMOTEover.PNG](https://github.com/agregorash/Credit_Risk_Analysis/blob/main/images/SMOTEover.PNG)

**-Balanced Accuracy Score: 0.6473*


### Undersampling 

- The low-risk values in the dataset were undersamplered using ClusterCentroids in this model

![cc.PNG](https://github.com/agregorash/Credit_Risk_Analysis/blob/main/images/cc.PNG)

**-Balanced Accuracy Score: 0.6473**


### SMOTEENN

- This model used a combination of under and oversampling of the data, using the SMOTEENN technique

![SMOTEENN.PNG](https://github.com/agregorash/Credit_Risk_Analysis/blob/main/images/SMOTEENN.PNG)

**-Balanced Accuracy Score: 0.5111**

### Balanced Random Forest Classifier

- The ensemble algorithm BalancedRandomForestClassifier was used to reduced bias in this model

![BalRandForest](https://github.com/agregorash/Credit_Risk_Analysis/blob/main/images/BalRandForest.PNG)

**-Balanced Accuracy Score: 0.7878**

### Easy Ensemble AdaBoost Classifier

- The ensemble algorithm EasyEnsembleClassifier was used to reduced bias in this model

![EasyEnsemble.PNG](https://github.com/agregorash/Credit_Risk_Analysis/blob/main/images/EasyEnsemble.PNG)

**-Balanced Accuracy Score: 0.9254**

## Summary

In order to determine which model best predicts loan outcomes, we must analyze a combination of variables from our analysis.  F1 score, found in the classification report indicates which percent of positive predictions were correct on a scale of 0.0- 1.0.  Balanced Accuracy score is the average of sensitivity and specificity of the model, also on a scale of 0.0- 1.0.

The model that returns the highest average F1 score and balanced accuracy score is the Easy Ensemble AdaBoost Classifier, therefore I can recommend that this model best predicts loan outcomes.
