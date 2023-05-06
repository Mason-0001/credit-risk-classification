# Module 12 Report Template

## Overview of the Analysis

The purpose of the following analysis was to use a large data set of loans and try to predict which loans were healthy and which were high risk. I had information about the loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, total dept, and finally the loan status (which was either 'healthy' or 'high risk'). I was specifically trying to use all of those variables to predict what the resulting loan status would be. 

In order to complete this process, I seperated out the variables from the result I was trying to predict, then split the data into a training and testing segment. Once done, I was able to use the LogisticRegression module to fit the model and create the prediction data. Using that, I was able to make a confusion matrix and classification report with the seperate testing data and the predictions to see how well the model worked. I also used the RandomOverSampler module to create training data that worked better due to it having an equal number of healthy/high risk data points.


## Results

* Machine Learning Model 1:
  * Model 1 predicts healthy loans almost perfectly, with a precision of 1.00 and a recall of .99. 
  * For unhealthy loans, the precision is .85 and the recall is .91. 
  * Lastly the balanced accuracy was roughly .95. This model 
    
* Machine Learning Model 2:
  * Model 2 predicts healthy loans almost perfectly, with a precision of 1.00 and a recall of .99. 
  * For unhealthy loans, the precision is .84 and the recall is .99. 
  * Lastly the balanced accuracy was roughly .99.

## Summary

When looking at the results from both the models we can conclude that Model 2 is superior to model 1. Both models predict and choose healthy loans very well however the more important loans to be able to predict are the 'high risk' loans. When we look at those numbers Model 2 has a recall that is .08 higher than Model 1 with a precision that is .01 lower. This means that Model 2 has a lower number of false negatives for 'high risk' or that it is much better at identifying 'high risk' loans. In order to do this, there is some precision that is sacrificed, meaning that there is a slightly higher likelyhood that you will have some healthy loans that are considered 'high risk' but the small amount of precision loss is worth it for the higher recall. Lastly, Model 2 has a higher balanced accuracy score which would indicate better performance for our inbalanced dataset (we have more 'healthy loans' in our dataset than 'high risk').

