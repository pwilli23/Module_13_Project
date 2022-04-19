# Module 12 Report

## Overview of the Analysis

* The purpose of the analysis is to help Alphabet Soup company, a venture capital firm, identify which businesses will be successful in the future given the firms income amount, ask amount, status, organization type, affiliation, and application type. 

* To do this we created 3 different binary neural network models and tested the accuracy of each see which of the 3 was the best model

## Model Creation Set Up: 

### Stage 1: Creating Our Neural Network Model:

* Step 1: We first had to import the appicant data csv file into our Jupyter Notebook using the `read_csv` function 

* Step 2: Next, we reviewed the data types using the `dtypes` function and converted all categorical variables to 1 or 0 values using the `OneHotEncoder` function

* Step 3: Used the `concat()` function to combine the categorical variable DataFrame and the numerical DataFrame

* Step 4: 

## Stage 2: Evaluate the Models Peformance:

* Step 1: Checked the balanced accuracy score of the model using the `balanced_accuracy_score` function

* Step 2: Generated a confusion matrix for the model to see by the numbers how accurate our model was: `confusion_matrix`

* Step 3: Printed the classification report for the model using the `classification_report_imbalance()` function. 

## The Resampling Method: 

### Stage 1: Use the Resampled Data and the LogisticRegression classifier to fit a new model to make predictions:

* Step 1: Use the `RandomOverSampler` function to set the `random_state` to 1 

* Step 2: Fit the original training data to the random_oversampler model by using the `fit_resample` function

* Step 3: Use the `LogisticRegression` function to fit the model and make predictions

### Stage 2: Evaluate the Models Performance:

* Check for the same statistics as in model 1

## Results

### Machine Learning Model 1:

* Model 1 had a 93.935% balanced accuracy score

* The model's precision for healthy loans was close to 100% while the precision identifying high-risk loans was 86%

* The model's recall for healthy loans was also close to 100% while the recall for high-risk loans was 91%
### Machine Learning Model 2:

* Model 2 had a 99.3% balanced accuracy score 

* The model's precision for healthly loans was close to 100% while the precision for high-risk loans was 84% 

* The model's recall for healthy loans was 99% while the recall for high-risk loans was 99%

## Summary

* In conclusion, Model 2 outperformed Model 1 because it more precisely identified and predicted the high-risk loans.  It is While it was slightly less accurate predicting and identifying healthy loans, its ability to identify those borrowers who are likely to default on a loan was signifcantly better.  It is more important for the credit union to better identify high-risk borrowers than it is to lend out more money to those who are less likely to pay back.   