# Credit Risk Classification
- Module 20 Challenge

## Credit Risk Analysis Report
### Overview of the analysis
- The purpose of this analysis is to build a model which can identify the creditworthiness of borrowers. 
- A dataset of historical lending activity from a peer-to-peer lending serice company was utilized.
- The dependent variable (y value) of this analysis was represented by "loan status" which indicated if a loan was healthy (0) or high risk (1).
- The independent variables (x values) were the loan size, interest rate, borrower income, debt to income ratio, number of accounts and derogatory marks.
- Within this analysis, data was split to training and test sets. Dependent and independent variables were defined. A logistic regression model was then created and fit to the original data within the model. A trained model was used to make predictions. Following this, an evaluation of the model's performance was made. 
### Results
Below you will find snapshots of logistic regression models for both the original data and a randomly oversampled dataset. 

* Logistic Regression Model with Original Data

![original_classreport](https://github.com/emichellet/credit-risk-classification/assets/118394753/c9af6007-b9cc-4e40-b327-ae4832f25c1a)
![balancedaccuracy_original](https://github.com/emichellet/credit-risk-classification/assets/118394753/bc577acf-2aad-4c64-a99f-47b92d2078a0)

* Logistic Regression Model with Randomly Oversampled Data

![resampled_classreport](https://github.com/emichellet/credit-risk-classification/assets/118394753/a444aaa8-be8e-4459-8719-a230dff2623d)
![balancedaccuracy_resampled](https://github.com/emichellet/credit-risk-classification/assets/118394753/4aa9c01b-a852-40bd-9e4a-f2d98bc59919)

### Summary
Analysis dipslays that collected data can be effectively used to train and test the Machine Learning Classifcation Model. For better predictions, solving the imbalance sampling issue is required. Randomly oversampling the data helps to get higher balanced accuracy and recall scores. Incorrect predictions can raise some issues:
- False positives (users will be flagged as risky, but they are actually healthy)
- False negatives (users who are risky may not actually be flagged because they are improperly coded as healthy)

Much like medicine, having such issues rise can have its detriments. Thus, it is important to have the model predict both healthy and risky (0's and 1's). Additionally, the model must have great accuracy with identifying both. 

***
## Instructions
The instructions for this Challenge are divided into the following subsections:
    - Split the Data into Training and Testing Sets
    - Create a Logistic Regression Model with the Original Data
    - Predict a Logistic Regression Model with Resampled Training Data
    - Write a Credit Risk Analysis Report

## Split the Data into Training and Testing Sets
- Open the starter code notebook and use it to complete the following steps:
    - Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
    - Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
        *NOTE: A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
    - Split the data into training and testing datasets by using train_test_split.

## Create a Logistic Regression Model with the Original Data
- Use your knowledge of logistic regression to complete the following steps:
    - Fit a logistic regression model by using the training data (X_train and y_train).
    - Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
    - Evaluate the model’s performance by doing the following:
        - Calculate the accuracy score of the model.
        - Generate a confusion matrix.
        - Print the classification report.
    - Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

## Write a Credit Risk Analysis Report
- Write a brief report that includes a summary and analysis of the performance of the machine learning models that you used in this homework. You should write this report as the README.md file included in your GitHub repository.

- Structure your report by using the report template that Starter_Code.zip includes, ensuring that it contains the following:
    - An overview of the analysis: Explain the purpose of this analysis.
    - The results: Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.
    - A summary: Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.
