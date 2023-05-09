# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis. 

The purpose of this challenge was to use modeling techniques to predict creditowrthiness of borrowers from an existing dataset. The challenge lies in evaulating how to modify the dataset using our own evaluations of the dataset to make the most accurate model. 

* Explain what financial information the data was on, and what you needed to predict.

The financial information used includes loan size, interest rate, borrower's income, debt to income ratio, number of accounts, derogatory marks, and total debt of the borrower to predict the loan status. The loan status is classified into one of two values: 0 (healthy loans) and 1 (risky loans)


* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).

The variable that was to be predicted was the number of healthy loans and risky loans using the value counts function. The independent variables used in the logistic regression model were loan size, interest rate, borrower's income, debt to income ratio, number of accounts, derogatory marks, and total debt.


* Describe the stages of the machine learning process you went through as part of this analysis.

First the original dataset was split between the train and test data using the train_test_split function. A Logistic Regression model was then created based on the original dataset. After calculating an accuracy score based on the given dataset, a confusion matrix was created to record the true positive, true negative, false positive, and false negative values, while its performance metrics were evaluated based on the precision, recall, and f1 scores. A second logistic regression model was resample to overrepresent the minority class data (risky loans) and followed the same process.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

Logistic Regression model was used for the existing dataset and the resampled data set.

To get a better representation of the data, I utilized the RandomOverSampler function to better represent the minority class that is the high risk loans in the training data in order for the model to better predict the high risk loans.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.

Precision score Healthy Loans: 1.00
Recall score Healthy Loans: .99
F1-score Healthy Loans: 1.00


Precision score Risky Loans: 0.85
Recall score Risky Loans: .91
F1-score: .88
  


![alt text](https://github.com/kashbasavaraju/Module_12/blob/main/Imbalanced_Classification_Report.jpg)


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  
Precision score Healthy Loans: 1.00
Recall score Healthy Loans: .99
F1-score Healthy Loans: 1.00

Precision score Risky Loans: 0.84
Recall score Risky Loans: .99
F1-score: .91
  
![alt text](https://github.com/kashbasavaraju/Module_12/blob/main/Oversampled_Classification_Report.jpg)

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?

I would recommend the Regression Model with the oversampled dataset.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

I believe it would be better to predict the unhealthy loans than a model that would better predict the healthy loans. For the purposes of trying to identify credit risk, it would better to be oversample risky loans in order to create a model that is less likely to predict false positives for creditworthiness and therefore lowers risk for lenders. In the original data set, the model is more likely to return false positives with the original data set which is indicated by the lower precision score for high risk loans. The F1 score captures the likelihood of returning false positives and false negatives - the original dataset has a lower f1 score for high risk loans than the oversampled data as well.
