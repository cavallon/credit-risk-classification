# credit-risk-classification 

## Overview of the Analysis

This section describes the analysis that was completed for the machine learning models used in this project.  

* Purpose of the analysis:
The purpose of this analysis is to determine how well the machine can predict the results of the data by comparing the machine predictions to the actual data results. 

* Explain what financial information the data was on, and what you needed to predict: 
The data I used is based on bank loans and includes whether the loan is in default (person is not paying), or if it is a healthy loan (person is paying on time). I needed the actual default status of the loan in order to compare it with the predictions made by the algorithm.  

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`):
We are trying to use the data from each loan to predict whether the loan will turn out to be a healthy loan or an unhealthy loan (default). The data is found in the column titled loan_status.

* Describe the stages of the machine learning process you went through as part of this analysis:
The first stage I went through, was to separate the data that I wanted to predict from the rest of the data in the data frame. I did this by making a new data frame for just the loan_status column, and set it equal to y. The rest of the data from the original data frame was set as equal to X. I then took the y and the X data frames and further split them into training and testing variables. So, y now has training and testing variables, and the same for X. After doing this, I created a logistical regression model, and used the model to create predictions. I then used a confusion matrix to compare the results, and printed a classification report to show how accurate the model was compared to the actual (test) data.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms): 
Logistic regression requires a data set that has labeled examples. Each example usually has one or more features and a binary outcome of either 0 or 1. Logistic regression models determine the probability that a particular instance belongs to a certain class. In our case, whether the loan will become a healthy loan or an unhealthy loan. In order to get the results the model must be trained. After it is trained, it can create predictions, and then classify how accurate those predictions are using metrics such as accuracy, precision, f-1 score, and support. Logistic regression has limitations when the data is non-linear and contains more complex relationships.  

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of the machine learning model.

* Description of Model Accuracy, Precision, and Recall scores.

    * Accuracy - this is calculated as the ration of the number of correct predictions to the total number of predictions made by the model. It measures the overall correctness of the models predictions across all classes. In this case the accuracy was 99%. 
    * Precision - this measures the proportion of correctly predicted positive cases out of all instances predicted as positive by the model. In this case, it correctly predicted 99% of all healthy loans (0), and 91% of all unhealthy loans (1). 
    * Recall - this measures the percentage of relevant data points that were correctly identified by the model. In this case, 100% of all data points were correctly identified for healthy loans (0), and 88% of all relevant data points were correctly identified for the unhealthy loans (1). 

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. 

The logistic regression model predicts the '0' (healthy loan) labels with 99% of predictions made by the model being correct (precision), and with 100% of the relevant data points being correctly identified by the model (recall). This is a very good result in terms of predicting healthy loans. For '1' (high risk loans), 91% of the predictions made by the model were correct, and 85% of the relevant data points were correctly identified by the model. This model seems to correctly predict whether a loan will be healthy at a higher rate than when it predicts whether a loan will be unhealthy. In either case, I would still recommend that the company use this. Overall, the model scored a 99% in accuracy. If there is any concern over the lower scores regarding the unhealthy loans, the model can be used to focus on predicting healthy loans (being that it scored 99% in precision and 100% in recall for healthy loans). 

# File Information

The file labeled credit_risk_classification.ipynb has all solution code. 
