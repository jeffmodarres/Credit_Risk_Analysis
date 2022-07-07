# Module 17: Credit_Risk_Analysis

## Overview
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Goal is to employ different techniques to train and evaluate models with unbalanced classes.
Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once done, we’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

# Result
Here are the results of testing different techniques for this imbalanced dataset

**RandomOverSampler:**
- balanced accuracy score: 0.64
- Precision: 0.01
- Recall: 0.69

**SMOTE:** (Oversampling)
- balanced accuracy score: 0.66
- Precision: 0.01
- Recall: 0.63

**ClusterCentroids:** (undersampling)
- balanced accuracy score: 0.54
- Precision: 0.01
- Recall: 0.69

**SMOTEENN:** (Over and under Sampling)
- balanced accuracy score: 0.675
- Precision: 0.01
- Recall: 0.76

**BalancedRandomForestClassifier:**
- balanced accuracy score: 0.79
- Precision: 0.03
- Recall: 0.70

**EasyEnsembleClassifier:**
- balanced accuracy score: 0.998
- Precision: 0.96
- Recall: 1

# Summary
The problem of predicting high risk loans is very imbalanced in nature. Most loans are paid in time with no issues and there are few bad loans. 
RandomOverSampler, SMOTE, ClusterCentroids and SMOTEENN were used in combination with logistic regression to predict bad loans. None of them works as expected. 

Two decision tree based classifiers (BalancedRandomForestClassifier,EasyEnsembleClassifier) were tested as well. and EasyEnsembleClassifier(Adaboost based) perform really well and it has very high precision and Recall.

its recommended to use EasyEnsembleClassifier for this type of predictions.
