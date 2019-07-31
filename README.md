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