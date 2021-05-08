# Bank-Credit-Card-Customer-Attrition-Analysis
Using Random Forest and Logistic Regression models, with Qualitative Analysis, Insights and Recommendations

This project uses the fictional bank credit card dataset from https://www.kaggle.com/sakshigoyal7/credit-card-customers?select=BankChurners.csv

Aim: to identify which customers are likely to attrite and to provide insights and recommendations to the bank 

## Organisation: 

### Main notebook: Completed Notebook.ipynb

First section consists of Data Cleaning followed by basic exploratory data analysis. The imbalanced data was upsampled after train_test_split() to generate new samples only in the training set to ensure our model generalises well on unseen data.

Second section is for creating the Random Forest model by first doing RandomSearchCV to narrow the scope of possible optimal parameters, followed by GridSearchCV for hyperparameter tuning.
We tried to investigate which number of features selected would result in the optimal Random Forest model with the best f1 score using 4,5,6,7,8 features respectively. Optimal number of features was determined to be 7.

Third section is for creating the Logistic Regression model by doing GridSearchCV for hyperparameter tuning. We tried to investigate which number of features selected would result in the optimal Logistic Regression model with the best f1 score using 4,5,6,7,8 features respectively. Both RFE and SFM methods were tested and RFE was used in the end because the f1 scores were higher. Optimal number of features was also determined to be 7.
For each specified number of features for selection, Recursive Feature Selection (RFS) and Select From Model (SFM) methods are included in the same Logistic Regression model file. 

Random forest was selected over Logistic Regression due to higher f1, accuracy and ROC-AUC scores. 

Last (but not least) section is for doing additional data analysis using the feature importances and final random forest model. We tried varying the values of the important variables to determine its effect on the number of people our model predicts will attrite. Total Transaction Count shows to be effective in decreasing the number of predicted people who attrite, while there seems to be no effect for Total Transaction Amount. Change in Transaction Count,  Change in Transaction Amt, Total Relationship Count, shows some effect in decreasing the number of predicted people who attrite. Avg Utilisation Ratio has almost no effect, and Total Revolving Balance was not tested because we thought it would be almost impossible for the bank to persuade customers to change.

### Summary of results:
Total Transaction Count and Total Relationship Count (number of products held by the bank) can significantly decrease the percentage of customers attriting from the bank. 

Recommendation for bank to increase Total Transaction Count by increasing customer spending incentives and to increase Total Relationship Count by offering more of their other financial products to their existing credit card customers. (Details can be found in slides provided)
