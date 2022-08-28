# Module 12 Report Template

## Overview of the Analysis

**Purpose:** 
The purpose of the analysis is to present evaluations of a historical dataset of lending activity from a peer-to-peer lending services company.  Linear regression models will
be generated to identify the creditworthiness of borrowers.

**Data:** 
Financial information for all lenders included the following variables: 
    1. Loan Size
    2. Interest Rate
    3. Borrower Income
    4. Debt To Income (DTI)
    6. Number of Accounts
    7. Derogatory Remarks
    8. Total Debt
    9. Loan Status
    
The loan status was the important variable of interest. So, the 'y' variable was separated and set as a label. Healthy loans were denoted by '0' and high risk loans were denoted by '1'. 

**Analysis:**
First, the number of health loans and high risk loans were counted by using the value_count function. Initial data indicate that there were 75,076 'Healthy Loans' and 2,500 'High-Risk Loans'.  This unbalanced dataset allowed for a training model to be created. The data was split by using the train_test_split function. An initial logistic regression model was created based on this data.  This model would serve as the training data. Predictions and accuracies were calculated based on this data. A confusion matrix was then created to evaluate the predictions.

Secondly, another logistic regression model was created using the resampled data.  This was done by using the random oversampling model to refit the training to a balanced dataset of 56,277 'Healthy Loans' and 56,277 'High-Risk Loans'. Again predictions were made. 


## Results

By conducting a second logistics regression on training data, the overall accuracy increased from 99.2% to 99.4%.  And the ability to determine 'High-Risk Loans' went from 87% to 97%.

**Machine Learning Model 1:**

                 precision    recall  f1-score   support

           0       1.00      1.00      1.00     18759
           1       0.87      0.89      0.88       625

    accuracy                           0.99     19384
   macro avg       0.94      0.94      0.94     19384
weighted avg       0.99      0.99      0.99     19384



**Machine Learning Model 2:**
                 precision    recall  f1-score   support

           0       0.99      0.99      0.99     56277
           1       0.99      0.99      0.99     56277

    accuracy                           0.99    112554
   macro avg       0.99      0.99      0.99    112554
weighted avg       0.99      0.99      0.99    112554


## Summary

Model #2 is the better model for this analysis.  Both the overall accuracy and ability to detect 'High Risk Loans' increased. It is more important to predict the 'High Risk Loans', however, I believe that more information should be used in addition to the algorithm. Sometimes lenders disqualify successful loan candidates without other considerations or unforeseen circumstances.