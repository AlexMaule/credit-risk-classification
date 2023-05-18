# Credit Risk Classification

### Overview
The purpose of this exercise is to create a model to evaluate, predict, if an individual is a considered a `healthy loan` or `high risk loan` based on several pieces of information collected. To build a model capable of predicting which individuals will pay back their loan, it will be used Supervised Machine Learning tools from Scikit-Learn library among others, and a dataset with already labeled results.

The dataset contains these columns:
* loan_size
* nterest_rate
* borrower_income
* debt_to_income
* num_of_accounts
* derogatory_marks
* total_debt
* loan_status

### The Results
There were two models created to observe how some modification of the data could help with creating a model that have better performance.
Both models were created using the Logistic Regression Model. The first used the original dataset, obtaining good result:

![credit-original](https://github.com/AlexMaule/credit-risk-classification/assets/108903118/d2e91358-4481-42a0-85c0-5095e4eb3308)

![class-report-original](https://github.com/AlexMaule/credit-risk-classification/assets/108903118/05a76cef-2de0-4501-a706-c173255f0dfc)

From these we can see that the model worked outstanding for `healthy loans` with 100% Precision and Recall, but not so good for `risky loans` with 87% Precision and 91% Recal. The `risky loans` predictions are actually good, but compared with its counterpart, it lacks behind.

For the second model built, the dataset was resampled with Random Over Sampler which helped to improve the model predictions for `risky loans`.

![credit-resample](https://github.com/AlexMaule/credit-risk-classification/assets/108903118/847d9d11-8214-4f90-bcd6-de5cf58827d4)

![class-report-resample](https://github.com/AlexMaule/credit-risk-classification/assets/108903118/4a6dfc6f-d943-4a5b-b8a6-757d17e122fc)

The difference from the previous model is the 1% drop in Recall of `healthy loans` and Precision in `risky loans` in exchange of an increase of 8%, from 91% to 99%, in Recall of `risky loans`.

### Summary
Looking at the point of view of an individual or loaning group, which prefers to security, would be to use the the first model with the original data since it give 100% in Precision, meaning that all prediction of healthy loans were `healthy loans`, and the 100% in Recall, meaning that all the loans that are healthy were predicted as such.
