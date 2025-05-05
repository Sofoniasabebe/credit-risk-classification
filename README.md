# credit-risk-classification

## Overview of the Analysis

The purpose of this analysis was to develop and assess a machine learning model for predicting loan risk satus based on applicant information. Specifically, the goal was to differentiate between high-risk loans (label `1`) and healthy loans (label `0`). 

The dataset included various financial metrics, such as:
* Loan size
* Interest rate
* Borrower income
* Debt-to-income ratio
* Number of credit accounts
* Number of derogatory marks
* Total existing debt
* Loan status 

The goal was to predict the loan_status column, which indicates whether a loan is high risk (`1`) or healthy (`0`). The distribution of the loan_status variable showed a class imbalance, with far more healthy loans than high-risk ones. A `value_counts` on the y data showed that there are 75036 healthy predictions and 2500 high-risk pridictions. 

The machine learning process involved the following steps:

* Importing and reviewing the data

* Splitting the data into features (X) and labels (y)

* Splitting into training and testing sets

* Fitting a logistic regression model using LogisticRegression

* Making predictions and evaluating performance using a confusion matrix and classification report

## Results

* Machine Learning Model 1: Logestic Regression
    * Accuracy: 99% of all predictions were correct 

    * Precision (Class 0): 1.00 - Of all the loans predicted to be healthy (0), 100% were actually healthy.

    * Recall (Class 0): 0.99 - Of all the actual healthy loans, 99% were correctly identified as healthy.

    * Precision (Class 1): 0.84 - Of all the loans the model flagged as high-risk, 84% were actually high-risk.

    * Recall (Class 1): 0.94 - Of all the actual high-risk loans, 94% were correctly identified.

    * F1-score (Class 1): 0.89 - A score of 0.89 indicates a strong model performance on the minority/high-risk class. 

## Summary 

The logestic regression model performed very well predicting both labels. For `0` (healthy loan), the precision is 1.00 meaning every loan predicted as healthy was correct. The recall is 0.99 - which indicates that 99% of all the actual healthy loans were identified. The f1-score is 1.00 - perfect balance between precision and recall. This means the model is extreamly confident and accurate when identifying healthy loans. 

For the `1` high-risk loan, the precision is 0.84 indicating that 84% of predicted high-risk loans were actually high-risk. The model correctly flagged 94% of all the high-risk loans. The f1-score is 0.89 indicating a solid performance given the small number of high-risk cases. 

Overall, although healty loans outnumber high-risk by ~30:1, the model still captures the majority of high-risk loans, whic is critical for credit risk assessment.

The logistic regression model performed exceptionally well overall, especially considering the class imbalance. It predicted healthy loans (0) with near-perfect accuracy.More importantly, it successfully identified 94% of high-risk loans (1) with strong precision (84%) and F1-score (0.89), which is critical in a financial risk context.

I recommend using the logistic regression model as a baseline solution since it performs very well on both classes, especially the minority class (1), which is more important for minimizing loan defaults. It is also interpretable, fast, and easy to deploy. 



