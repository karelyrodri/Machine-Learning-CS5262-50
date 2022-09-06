# Credit Risk Assessment 
This project will focus on assessing credit risk.
This is the probability an individal will be unable to repay their debt obligations. The goal is to predict whether there is or is not credit risk given the information supplied in each record.

0 - Not a Credit Risk   
1 - Is a Credit Risk

## Problem Statement 

The goal is to create a credit risk model that will determine the likelyhood the money borrower will fail or succeed to repay the amount agreed upon including interest within the agreed upon time frame. 
The importance lies in maintaining maximum profit for the lender. With the model, an estimate will be calculated taking account the predicted risk to adjust the approximate profit figure.
### Performance Metric 

Average Expected Loss = $157,095   
This includes loan/credit principle and accumalated interest over the term based on the calculated Compound Interest formula applied to the data points set to be at risk 

Money Regained = $117,820    
This cost is calculated at about an average of 75% of the unpaid loan amount is regained by the lender 
Some examples of how lenders regain money is through forclosures, debt collectors, short sales, etc.

#### Confusion Matrix

0 - Will pay - not a credit risk   
1 - Does not pay - is a credit risk

True Positive: The record resulted as credit risk - 1 and was correctly predicted as a credit risk - 1

False Positive: The record resulted as not a credit risk - 0 and was incorrectly predicted as a credit risk - 1

False Negative: The record resulted as a credit risk - 1 and was incorrectly predicted as not a credit risk - 0

True Negative: The record resulted as not a credit risk - 0  and was correctly predicted as not a credit risk - 0
 
<img width="466" alt="Confusion Matrix - Business Costs" src="https://user-images.githubusercontent.com/106625643/188528927-682248db-333e-447d-8b65-6c3297b76a05.PNG">


tp = records that failed to pay   
fp = records that did pay   
fn = records that were expected to pay but failed to pay 

## About the Data 
Date is available at the following link:  https://docs.google.com/spreadsheets/d/1AvPiqVtKBoKFiX4h3uGFbWBty7ZhNt4FmWU6jrXhb8U/edit?usp=sharing

The origins or the data were found as a free public data set on kaggle.com 

Since then it has been altered in minor ways including removing irrelevant columns, combining categorical values into larger ranges (ex. less than 1 year, 1 year -> 1 year or less), changes to the purpose values (ex. replacing values such as Small_business to Business Loan)

The data source contains 21,341 records, however after data clean up (removing empty, NAN, and impossible values) there is 15,787 records and 12 features that will be used.

### Numeric Columns:

Loan Amount  
Credit Score   
Annual Income  
Monthly Debt   
Years of Credit History   
Credit Card Balance   
Credit Card Limit   
Interest Rate

### Categorical Columns:

Loan Term Length - [1 year, 3 year, 5 year, 7 year, 10 year, 15 year, 30 year]   
Years in Current Job - [1 Year or Less, 2 - 4 years, 5 - 7 years, 8 - 9 years, 10+ years]   
Home Ownership - [Rent, Home Mortgage, Home Owner]   
Loan Purpose - [Home Improvements, Business Loan, Car Loan, Home Loan, Medical Bills, Educational Expenses]

## Assignment 2 Comments
- "Average Expected Loss = $157,095" is this the average loan + interest that a financial firm stands to gain/lose? I don't quite understand from the current description
- Maybe add a note that if the customer doesn't pay back on time, although the firm experiences a short term loss of x amount, it should still recover at least a portion of it (depending on the loan type), whether via foreclosure methods, debt collectors, etc.
