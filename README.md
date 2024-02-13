# deep-learning-challenge
Module 21

# Module 20 Report Template

## Overview of the Analysis

The purpose of this analysis was to help a bank classify future borrowers as risky applicants or worthy of loan. Available data on loan amount, interest rate, income, debt to income ratio, number of accounts held with the bank, number of derogatory remarks, total amount of debt and whether on not they defaulted on the loan in question were leveraged from 77,537 bank customers. Of those customers, the majority (75,036) were were in good standing. This is to be expected, as those with low credit scores may be less likely to apply and therefore approved for a loan. However, this imbalance limits the model's exposure to characteristics associated with risky borrowers (loan_satus=1), thus potentially introducing bias in predicting default loan status.  Therefore, in addition to logistic regression using the available data set, an oversampling excercise was also completed. 

The first step was to preview the dataset (lending_data.csv) to determine what data is available. Next, two new dataframes (x and y) were created from the initial file.  One dataframe (y) included a single target variable that we'd like to predict, loan status (0=healthy, risky=1).  The other dataframe (x) contained all variables except loan status. Next we checked the distribution of classifications (healthy versus default loan status) in the target dataframe. This step checks for balance in the categorical target we are trying to predict.  Next we split both dataframes into a test and a train dataframe. Generally speaking, the train set contains 75% of the data.  Given we are prediciting a categorical outocome, we fit the training data to a logisitic model.  Then loan status was predicted based on the X test data. The performance of the prediction was then evaluated using an accuracy score, confusion matrix, and a classification report. The same steps were repeated for resampled data to ensure the model is not biased towards healthy loans (0) where the majority of data is found.         


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  --The accuracy of the logistic regression model using the original dataset got 95% of predictions correct.  
  --The confusion matrix revealed there were 56 false negatives, meaning this model incorrectly predicted 56 risky loan applicants (1's) and approved them for loans. This is refelected in the risky loan recall score of 91%. 
  --Precision and recall for healthy loans were high, at 100% and 99% respectively. 
             



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  --The accuracy of the resampled model was 99%.
  --Precision and recall for healthy loans were identical to model 1, at 100% and 99% respectively.
  --False positives were reduced from 56 to 4 in model 2.  This translated to a higher recall score of 99% for risky loan applicants.   

## Summary

In model 2, we aimed to reduce false negatives, thereby increasing recall. Attempting to reduce false positives would decrease precision, however losing precision is a trade-off that minimizes risk to the bank. 

Accuracy was higher in machine learning model 2. Additionally, the goal of increasing recall (i.e. reducing false positive instances where risky loan applicants are approved for loans) was accomplished in model 2 which employed resampling until balance in number of healthy loan and risk loan applicants were balanced (56271 in each group). Performance depends on the problem at hand. In this case, increasing recall was important because predicting risky loan applicant (1's) were the priority.  There is less danger to the bank due to false positives (i.e. wrongly classifying healthy loan applicants as risky).    
