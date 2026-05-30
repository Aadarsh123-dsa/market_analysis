## BANK MARKET ANALYSIS
Marketing is the process by which companies create value for customers and build strong customer relationships in order to compute value from customers in return.
Marketing Campaigns are characterized by focusing on the customer needs and their overall satisfaction. There are different variables that determine whether a marketing campaign will be successful or not. These are :
1. Segment of the Population:
   To which segment of the population is the marketing campaign going to address and why? This is important to which part of population should receive message.
2. Distribution Channel to reach the customer's place:
   It is about finding ways to reach message out.
3. Price:
   To find best price to reach the potential customers.
4. Promotional Strategy:
    This is the way the strategy is going to be implemented and how are the potential clients going to be address.

# Dataset Description 

There are in total 16 features including numeric as well as categorical features and an output feature too called deposit .
- Bank Client Data:

| Features | DESCRIPTION |
| ---------| ----------- |
| Age   | numeric   |
| job   | type of job (categorical) |
| Marital| (categorical: 'divorced','married','single')|
| Education | (categorical: primary, secondary, tertiary and unknown)|
| Default  | has credit in default (categorical) |
| housing | has housing loan? (categorical) |
| loan |  has personal loan? (categorical) |
| Balance | Balance of the individual |


 - Related with the last contact of current campaign:


| Features | DESCRIPTION |
| ------- | -------- |
| contact | contact communication type (categorical: 'cellular','telephone') |
| month   | last contact month of year (categorical) |
| day     | last contact day of the week (categorical) |
| duration| last contact duration, in seconds (numeric) |


 - Other Attributes :



| Features | DESCRIPTION |
| ------- | -------- |
| campaign | number of contacts performed during this campaign |
| pdays | number of days that passed by after the client was last contacted from a previous camp |
| previous | number of contacts performed before this campaign and for this client |
| poutcome | outcome of the previous marketing campaign (categorical) |

- Output feature :

 | Features | DESCRIPTION |
| ------- | -------- | 
| Deposit | whether done or not (categorical )|

Fortunately, there are no missing values. If there were missing values we will have to fill them with the median, mean or mode. I tend to use the median but in this scenario there is no need to fill any missing values. This will definitely make our job easier!

# ANALYSIS 
1. Here, median ages are almost similar in both the cases of deposit so it is not a strong predictor value but older customer subscribe slightly more hence still important.
2. Balnce might influence deposits but there are lot of outliers to deal . High balance customers may be more financially active.
3. Longer calls suggest more subscribers so it is a powerful predictor here.
4. Day is not a good feature as almost similar.
5. Previous days can be an important feature here but here are different spread patterns.
6. Suprisingly, lower campaign values perform better. This suggest that excessively marketing calls can reduce the effectiveness and impact.
7. job affects deposit subscription behavior so it is an important feature.
8. customer without personal loans subscribe more.
9. May have huge impact so here timings also matters a lot.
10. Family responsibilities here influences the financial decision.
11. It is common that if no default is there then people will have deposit so it is not a important feature too.
12. Cellular contact comparatively perform much better to reach the customers so here it is also an good feature to analyze.
13. Education level may impact on the reach of awareness.
14. Housing suggest that people already with housing loan do not afford furthur liabilities so this feature may affect too.
15. poutcome does not suggest much as unknown have higher counts with no and yes and here the success has greater yes but having less counts overall .


# ML MODEL ANALYSIS 
-  PREVIOUS RESULTS

| MODELS  | Accuracy  | F1 score | Recall  |
|--------|-----------|----------|----------|
| Logistic REGRESSION | 0.80967 | 0.79616 | 0.777881 |
| KNN | 0.77563  | 0.744518 | 0.68416  |
| DECISION TREE | 0.793103 | 0.78104 | 0.772258 |
| SVM | 0.83475 | 0.8281322 | 0.833177 |


- AFTER EDA RESULTS


| MODELS  | Accuracy  | F1 score | Recall  |
|--------|-----------|----------|----------|
| Logistic REGRESSION | 0.80743| 0.800371 | 0.80787 |
| KNN | 0.755933| 0.72899  | 0.686972 |
| DECISION TREE | 0.82266  | 0.81950 | 0.84254  |
| SVM | 0.833407  | 0.831062  | 0.85754  |


# CONCLUSION 
overall recall scores and accuracy are improved in SVM, DECISION TREES  AND LOGISTIC REGRESSION as per the statement.

# solutions for next marketing campaign 
1. Months of Marketing Activity: We saw that the the month of highest level of marketing activity was the month of May. However, this was the month that potential clients tended to reject term deposits offers. For the next marketing campaign, it will be wise for the bank to focus the marketing campaign during the months of March, September, October and December.
2. Campaign Calls: A policy should be implemented that states that no more than 3 calls should be applied to the same potential client in order to save time and effort in getting new potential clients.
3. Age Category: The next marketing campaign of the bank should target potential clients in their 20s or younger and 60s or older.
4. House Loans and Balances:  the next marketing campaign should focus on individuals of average and high balances in order to increase the likelihood of suscribing to a term deposit.
5. Target individuals with a higher duration (above 375): Target the target group that is above average in duration, there is a highly likelihood that this target group would open a term deposit account.






   


