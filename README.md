# Credit_Risk_Classification
* * *

## Background Information
- - -
There are various techniques to train and evaluate a model based on loan risk. This project uses a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

## Summary Report
- - -
### Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* The purpose of this analysis is to create a model that will make predictions on classifying healthy versus high-risk loan.

* The dataset contains 77,535 instances and 8 features. The features includes:
 0   loan_size         77536 non-null  float64 ---the total amount of the loan
 1   interest_rate     77536 non-null  float64 ---the interest rate
 2   borrower_income   77536 non-null  int64   ---the borrower's annual income
 3   debt_to_income    77536 non-null  float64 ---the ratio of debt to income
 4   num_of_accounts   77536 non-null  int64   ---the total number of accounts
 5   derogatory_marks  77536 non-null  int64   ---a negative item, such as a late payment or foreclosure. 
 6   total_debt        77536 non-null  int64   ---total amount of debt
 7   loan_status       77536 non-null  int64   ---0 for healthy loan and 1 for high-risk loan
Given the information above, we want to predict the loan_status of a future entry.

* In this model, `value_counts` will be the prediction factor `y` and has a value of 0 and 1, whereas 0 represents healthy loan and 1 represents high-risk loan.

Stage 1, we prepare the datasets. We label the `value_counts` column as `y` and the rest of the features as `X`. We check for non NAN values and how the data is stratified on `y`. Then, we split the dataset into training set and testing set.
Stage 2, we set up the prediction model. Since we want to perform a classification model, we choose Logistic Regression in this case. We set up the model with `solver="lbfgs" and  random_state=1`. We fit in the training dataset `X_train` and `y_train`. Then, we make prediction base on `X_test`.
Stage 3, we evaluate the model's performance. We calculate the `balanced_accuracy_score`, generate the `confusion_matrix`, and print the `classification_report`.
Stage 4, we resampled training data using RandomOverSampler. Since we are dealing with imbalanced data, we oversample the minority class to reduce class imbalance. We repeat stage 1 to 3 using the resampled data and evaluate the model's perfromance.

### Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  
  



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

### Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.






## File Paths
- - -
- Code: credit_risk_classification.ipynb
- Data: Resources ---> lending_data.csv

## Notes
- - -
This data analysis is conducted as an individual project by Bochao Gia Liu. 

## References
- - -
1. 
2. Image:guide_risk-management-banking_featured-img_1127x340 https://reciprocity.com/wp-content/uploads/2022/05/guide_risk-management-banking_featured-img_1127x340.jpg
3. Data: data for this dataset was generated/provided by edX Boot Camps LLC, and is intended for educational purposes only.
