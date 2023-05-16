# Credit Risk Analysis

## Overview of the Analysis

For this project, we are using a historical dataset of loan activity to predict whether or not future borrowers are credit worthy.  Each record in the dataset is labeled as either being a healthy loan or a risky loan.  The remaining features are what we use in the model to predict the health  of a loan.  These includes factors such as the size of the loan, the rate, income of the borrower, and their debt to income ratio, amongst others.  <br><br>

We used a logistic regression model to make our predictions.  Some data prep steps we took in the process include:
    -Separating the features and the target variables <br>
    -Splitting the data into testing and training data<br>
    -Oversampling the minority class in order account for the imbalance between the healthy and risky loans<br><br>

## Results
* Machine Learning Model 1 - no resampling :<br>
  * The model predicts risky loans with 87% precision, meaning that of all loans that were classified as risky, 87% were actually risky.<br>
  * Recall is slightly higher, at 89%--meaning that the model captured 89% of the risky loans<br>  
  * Recall is slightly higher, at 89%--meaning that the model captured 89% of the risky loans<br> 
  * Overall balanced accuracy of the model is also quite strong at 94% <br> 
  * For healthy loans, the model had near perfect precision and recall <br> 

* Machine Learning Model 2 (oversamplign of the risky loans):
  * Precision mirrors the original model at 87% <br>
  * After doing the oversampling, recall has jumped to 98% <br>
  * Accuracy also benefited from the oversampling, increasing to 99% <br>
  * Previson and recall of the healthy loans remains nearly perfect <br>
  
## Summary

Overall, both models perform well.  The resampled model improves upon the first model with better recall and overall accuracy, 98% and 99%, respectively.  Even through precision is slightly lower at 87%, I would still recommend this model.<br><br>
The main concern from a financial perspective would be, are there many risky loans that we aren't catching?  Given the near perfect recall score of the healthy loans, the answer to that question would be no. The model does a good job of capturing all the unhealthy loans <br><br>
 The main drawback to this model is that there are a small number of borrowers we are flagging as a credit risk when they would actually be healthy loans.  The lender would be losing out of this business, but overall this is a very small proportion of the total population.  <br><br>
 


