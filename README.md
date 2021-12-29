# Business understanding 

CLV presents value all eatimated future profit obtained from a customer over his relationship. It's regarded as an important metrics in managerial terms that provides insight into the profit-ability of business in the future. Thus, CLV prediction model could help marketer to better target the most potential and valuable customer group and take incentive strategy to retain them. 

It takes into account the total financial transaction of customer: The total discounted transaction per customer ( we will explain the formula in the code)



# Data description:

The data at hand is a part of the database of a fundraising organization. The description of the tables is in Appendix.
The fundraising organization gave you a data dump of March 2, 2020. They will use the model you create today (October 28) to measure their CLV in the future 3 years.

# Solution:
We decided to apply 2 phase model here.
1. We only take into account the customers that have CLV > 0 ( not considering the losing customer)
   1) Train CLV model on train observation which have CLV>0 
	 2）Apply CLV model on all test observations to get CLV predictions  ( Linear regression)
2. We use classification model to predict whether CLV>0 or CLV==0 (churner or non-churner)




# The creation of basetable
1)Based on the description, we need to determine the time windows for both the purpose model as well as the model building phase. Store the relevant moments of your model building phase in the variables end_independent, start_dependent & end_dependent 


2) Subset the extrel dataset according to the appropriate time window. Remember, we are trying to analyze the donors already started their relationship during the independent period and predict their behavior during dependent period. Thus, take into account the following:
a.The start of the relationship should be before (or equal to) the end of the independent period.
b.The end of the relationship should be later than the start of the dependent period (or missing)
c.The donor should have at least one transaction during the dependent period.


# Algorithm: 
Phase 1: Linear Regression
Phase 2: Logistic Regression & Random Forest 




