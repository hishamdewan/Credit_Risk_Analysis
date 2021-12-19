# Credit Risk Analysis using Machine Learning

## Overview of the analysis 
The purpose of this analysis is to use machine learning towards predicting credit card risk from lending data from LendingClub, a peer-to-peer lending service. The analysis applies six machine learning models lending data set and evaluates the quality of the models using balanced accuracy scores and the precision and recall scores. The analysis evaluates the performance of these models and recommends whether any model should be used to predict credit risk.

### Resources

- Data sources: [LoanStats_2019Q1.csv](https://github.com/hishamdewan/Credit_Risk_Analysis/blob/main/LoanStats_2019Q1.csv) 
- Tools used: Python, Pandas, imbalanced-learn, scikit-learn

## Results 
The following list describes the balanced accuracy score and the precision and recall scores of all six machine learning models:

**1. Random Oversampling**

- The Random Oversampling model produced balanced accuracy score of *0.629*.
- The model had a precision score of *0.01* for predicting high credit risk, which is very low when it comes to correctly classifying high credit risk loans. The model had a recall score of 0.64, which means the model predictions are correct 64% of the time. 

![naive_random_oversampling](/Images/naive_random_oversampling.png)

**2. SMOTE Oversampling Model**

- The SMOTE model produced balanced accuracy score of 0.62.
- The model had a precision score of 0.01 for predicting high credit risk, which is very low when it comes to correctly classifying high credit risk loans. The model had a recall score of 0.68, which means the model predictions are correct 68% of the time.

![SMOTE](/Images/SMOTE.png)

**3. Cluster Centroids Undersampling Model**

- The model produced balanced accuracy score of 0.51.
- The model had a precision score of 0.01 for predicting high credit risk, which is very low when it comes to correctly classifying high credit risk loans. The model had a recall score of 0.46, which means the model predictions are correct 46% of the time.

![undersampling](/Images/undersampling.png)

**4. SMOTEENN Model - Combination of Oversampling and Undersampling**

- The model produced balanced accuracy score of 0.64.
- The model had a precision score of 0.01 for predicting high credit risk, which is very low when it comes to correctly classifying high credit risk loans. The model had a overall recall score of 0.56, which means the model predictions are correct 56% of the time. However, recall score of 72% for high risk loans is quite good. 

![SMOTEENN_combination_over_and_under_sampling](/Images/SMOTEENN_combination_over_and_under_sampling.png)

**5. Balanced Random Forest Classifier**

- The model produced balanced accuracy score of 0.78.
- The model had a precision score of 0.04 for predicting high credit risk, which is very low when it comes to correctly classifying high credit risk loans. The model had a overall recall score of 0.91, which means the model predictions are correct 91% of the time. Recall score of 66% for high risk loans is decent. 

![balanced_random_forest_classifier](/Images/balanced_random_forest_classifier.png)

**6. Easy Ensemble AdaBoost Classifier**

- The model produced balanced accuracy score of 0.91.
- The model had a precision score of 0.08 for predicting high credit risk, which is very low when it comes to correctly classifying high credit risk loans. The model had a overall recall score of 0.95, which means the model predictions are correct 95% of the time. Recall score of 87% for high risk loans is very good. 

![easy_ensemble_adaboost_classifier](/Images/easy_ensemble_adaboost_classifier.png)


## Summary
All of the models showcased poor precision score between 0.01 to 0.08 when it comes to predicting high credit risk. Most of the models had good recall or sensitivity scores for predicting low credit risk. Overall, Easy Ensemble AdaBoost Classifier was the most accurate in terms of precision and recall scores. 

Based on this analysis, I do not believe any of these models are appropriate for using credit risk analysis. Primary goal of credit risk analysis is to avoid loans that have high likely hood of defaulting. None of these models have statistically significant precision regarding predicting high credit risk loans. 