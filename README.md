# Bank_Lending_ML

This is a project based from Kaggle [default-of-credit-card-clients-dataset](https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset)

This project, however, have a narrative:

### The Problem:
The Bank has been losing money due to bad lending pratices through excessive lending that are not paid in time

    - For each customer who is estimated not to pay within the deadline but ends up paying, the bank incurs a cost of 1000 €.
 
    - For each customer who is predicted to be a good payer but does not pay within the deadline, the bank incurs a cost of 3000 €.

We need to help the bank figure out which customers will not be paying their loans within the stipulated schedule.
In addition, we also need to develop the machine algorithm that will result in the least cost for the bank.

### The Questions:
Based on the problem the bank is facing we can ask several questions, in order to help the bank better manage its lending department

    1. How many features are available? How many customers?
    A: There are 30000 customers and 23 features, plus the customer ID and the customer classification

    2. How many customers in the dataset were actually bad payers? And how many were not?
    A: The original datatset had 6636 bad paying customers and 23364 good paying customers
    
    3. Which model led to the best results? What metric was used to compare the different models?
    A: Three different models were used in this challenge, SVM, random forest and XGBoost. XGBoost displayed the best accuracy at 0.82 and an associated cost of 2.415.000 euros (down from 3.939.000 euros if the bank considers all paying customer good paying       customers).
    
    4. What are the most relevant features for determining if a customer is more likely to be a bad payer?
    A: Using XGBoost, the most relevant feature for determining a custumer as good or bad is PAY_0, Pay_3, and PAY_2.
    PAY_0: Repayment status in September, 2005 (-1=pay duly, 1=payment delay for one month, 2=payment delay for two months, ... 8=payment delay for eight months, 9=payment delay for nine months and above)
    PAY_2: Repayment status in August, 2005 (scale same as above)
    PAY_3: Repayment status in July, 2005 (scale same as above)
    
    5. What would be the cost for the bank without any model?
    A: Whiout the model the cost for tha bank would either be 3.939.000 euros if the bank considers all custumers as good or, 4.687.000 euros if the bank considers all customers bad.
    
    6. What is the cost the bank incurs with your model?
    A: With the selected model the bank incurs in a cost of 2.415.000 euros, less than 1.524.000 euros.

