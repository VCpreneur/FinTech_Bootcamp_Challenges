# Module 12 Analysis Report 

## Overview of the Analysis

* The purpose of this analysis is to use various techniques to train and evaluate models with imbalanced classes. 

* We used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

* The data set we used included the following features: 
    - loan_size
    - interest_rate
    - borrower_income
    - debt_to_income
    - num_of_accounts
    - derogatory_marks
    - total_debt
    
* The target prediction was the Loan Status with the following labels: 
    - `0` (healthy loan)  
    - `1` (high-risk loan)

* Becase there was an imbalance in target labels in the provided data sets, we used the `imblearn` library to resample the data using its `RandomOverSampler` model. 

* Finally, we used `LogisticRegression` as our main classification model in this analysis. 

## Results

* Logistic Regression with Original Data - Classification Report:
  * ![Classification report for original data](Images/original_data.png)



* Logistic Regression with Over-sampled Data - Classification Report:
  * ![Classification report for over-sampled data](Images/oversampled_data.png)

## Summary

* There wasn't any considirable difference in predicting healthy loans after using the resampled data. But the model performed better after resampling (the second model above) in predicting high-risk loans espiacally that recall went from a .91 recall to a .99 at the expense of only .01 reduction in precision compared to the original data model.

* Based on the above, I recommend using the second model that used the oversampled data. 
