# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
  The goal of this analysis was to determine if the Logistic Regression machine learning model would more accurately predict the values for healthy loans versus high-risk loans using the original dataset or with a dataset that has been resampled to increase the size of the class. 
* Explain what financial information the data was on, and what you needed to predict.
  The dataset used for the analysis consists of information on 77,536 loans. It includes columns for loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, total debt, and loan status. the label we are trying to predict is loan_status. The data in the rest of the columns was used as features to train the data.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
  1. Prepare the Data - Import the file, create a DataFrame and evaluate the columns and features.
  2. Separate the data into feautres and labels(X,y) - The labels are what the model is trying to predict. The features are all of the remaining data that is used to train and test the model.
  3. Use the train_test_split function to separate the features and labels data into training and testing datasets.
  4. Import the machine learning model from the library, in this case the LogisticRegression model.
  5. Instantiate the model.
  6. Fit the model using the training data.
  7. Use the model to make predictions useing the features test data.
  8. Evaluate the precitions by calculating and comparing metrics like accuracy score, a confusion matrix, and a classification report.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).
  I used the LogisticRegression model, train_test_split, confusion_matrix and classifcation_report from SKLearn.
* 

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Accuracy score: 0.99
    * Precision: Class[0]: 1.00 , Class[1]: 0.84
    * Recall: Class[0]: 0.99 , Class[1]: 0.94

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
  The Logistic Regression model performed best for Class[0]. Both the precision and the recall were near perfect and had higher values than that of Class[1].
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
  Yes, as seen in Class[1] the model's precision and recall indicates that the model more often gives false positives than false negatives.

If you do not recommend any of the models, please justify your reasoning.
    I would say the logistic regression model seems to be a good model to use for predicting. We would need to see how accurate it can predict using a different data set to confirm that it can be used for predicting in this specific case. 
