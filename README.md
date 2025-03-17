# Credit Risk Report

## Overview of the Analysis

* **Purpose of the analysis** - The goal of this analysis is to determine if the Logistic Regression machine learning model can more accurately predict healthy loans versus high-risk loans using the original dataset or a dataset that is resampled to increase the size of the minority class.

* **The Dataset** - The dataset used to perform the analysis consists of information on 77,536 loans. The data includes columns for loan_size, interest_rate, borrower_income, debt_to_income ratio, number_of_accounts, derogatory_marks, total_debt, and loan_status. The category that we are attempting to predict with our analysis is **loan_status**. The data provided in the remaining columns will be used as features to train the model and inform the predictions.

* **Stages of the Machine Learning Process** - The stages of the machine learning process are very scripted. If followed in order, they provide an accurate assessment of the model's ability to make predictions. The stages of the machine learning process are as follows:

    - Prepare the data - Import the file, establish the DataFrame, and evaluate the columns and features.
   
    - Separate the data into features and labels - The labels represent what you are attempting to predict: whether the loan is healthy (0) or high-risk (1). The features comprise all of the remaining data used to train and test the model.
   
    - Use the train_test_split function to separate the features and labels data into training and testing datasets.
   
    - Import the machine learning model from the library - In this instance, we will be importing LogisticRegression from SKLearn.
   
    - Instantiate the model.
   
    - Fit the model using the training data.
   
    - Use the model to make predictions using the features from the test data.
   
    - Evaluate the predictions - Evaluations are performed by calculating and comparing metrics like accuracy score, a confusion matrix, and a classification report.
   
* **Machine Learning Methods Utilized** -

    The primary model used in this analysis is:
   
    - LogisticRegression model from SKLearn
   
    Supporting functions used in this analysis are:
   
    - train_test_split from SKLearn
   
    Models are evaluated using the following functions:
   
    - confusion_matrix from SKLearn
    - classification_report from SKLearn

## Results

* Machine Learning Model 1 - Logistic Regression:
 
  - Accuracy score: 0.99
  - Precision:
    - Class 0: 1.00
    - Class 1: 0.84
  - Recall:
    - Class 0: 0.99
    - Class 1: 0.94

## Summary

Overall, the Logistic Regression model performed well, especially in predicting outcomes for Class 0 (healthy loans), where both precision and recall were extremely close to perfect.

For Class 1 (high-risk loans), the model's precision is reported as 0.84 while the recall is 0.94. This suggests that the model may produce more false positives than false negatives for high-risk loans.

Given this information, the Logistic Regression model appears to do a great job at predicting both healthy and high-risk loans based on the features used for training. However, it is recommended that the model be further evaluated against different datasets before being implemented in production.
