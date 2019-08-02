# This is a AWS Fraud project from Table 1

# Banking Fraud
Every year, billions of banking transactions occur in the United States. While only a small portion of those are fraudulent, 
the results can be devastating is a fraudulent transaction is not discovered. Costs include damage to the customer, to the company,
and to regulator agencies tasked with confirming validity of payments.

# Datasets
- Over 6 million Banking Transactions
https://www.kaggle.com/ntnu-testimon/paysim1

This data set is a simulation, designed to accelerate research for financial applications. Each record is a single transaction, 
marked as cash in, cash out, debit, credit, or transfer. Each transaction will also have the amount, the name of origin, etc.
Interestingly enough you'll have 2 target columns. One appears to be an indicator isFraud, which should be a manual label.
Another is a flag based on a rule applied, that is, when a transaction has been attempted for over 200,000.


# Modeling Strategy
- Feature Engineer some additional predictors
- Train, test, validation datasets
- XGBoost algorithm within SageMaker

# End Goal
Decect fraudulent transactions by using the probability of the transaction from the model

## Data Dictionary:
step - maps a unit of time in the real world. In this case 1 step is 1 hour of time. Total steps 744 (30 days simulation).

type - CASH-IN, CASH-OUT, DEBIT, PAYMENT and TRANSFER.

amount - amount of the transaction in local currency.

nameOrig - customer who started the transaction

oldbalanceOrg - initial balance before the transaction

newbalanceOrig - new balance after the transaction

nameDest - customer who is the recipient of the transaction

oldbalanceDest - initial balance recipient before the transaction. Note that there is not information for customers that start with M (Merchants).

newbalanceDest - new balance recipient after the transaction. Note that there is not information for customers that start with M (Merchants).

isFraud - This is the transactions made by the fraudulent agents inside the simulation. In this specific dataset the fraudulent behavior of the agents aims to profit by taking control or customers accounts and try to empty the funds by transferring to another account and then cashing out of the system.

isFlaggedFraud - The business model aims to control massive transfers from one account to another and flags illegal attempts. An illegal attempt in this dataset is an attempt to transfer more than 200.000 in a single transaction.

## Kaggle Link:
https://www.kaggle.com/arjunjoshua/predicting-fraud-in-financial-payment-services