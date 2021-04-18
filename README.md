# Fictional-Bank-Credit-Card-Customer-Attrition-Analysis
Using Random Forest and Logistic Regression models, with Qualitative Analysis, Insights and Recommendations

This project uses the fictional bank credit card dataset from https://www.kaggle.com/sakshigoyal7/credit-card-customers?select=BankChurners.csv
Aim: to identify which customers are likely to attrite and to provide insights and recommendations to the bank 

## Organisation: Random Forest notebooks and Logistic Regression notebooks
To investigate which number of features selected would result in optimal model with best f1 score
Tried making random forest model and logistic regression models using 4,5,6,7,8 features respectively. 
For each specified number of features for selection, Recursive Feature Selection (RFS) and Select From Model (SFM) methods are included in the same Logistic Regression model file. 
# File Names for Random Forest Notebooks:
# File Names for Logistic Regression Notebooks:

## Main notebook: 
First section consists of basic EDA followed by Data Cleaning. The imbalanced data was upsampled before train_test_split() to 
Second section is for creating the Random Forest model by first doing RandomSearchCV to narrow the scope of possible optimal parameters, followed by GridSearchCV for hyperparameter tuning.

Third section is for creating the Logistic Regression model by doing GridSearchCV for hyperparameter tuning. RFE method was used to select best number of features because the f1 scores were generally higher than the ones obtained from SFM method of feature selection for the various number of features specified.
# File Name for Main Notebook: 

Summary of results:
Total Transaction Count and Total Relationship Count (number of products held by the bank) can significantly decrease % of customers attriting from the bank. 
Recommendation for bank to increase Total Transaction Count by increasing customer spending incentives and to increase Total Relationship Count by offering more of their other financial products to their existing credit card customers. (Details can be found in slides provided)
