# credit_risk_analysis

Bootcamp Module 17 - Supervised Machine Learning

## Overview

This analysis is to use machine learning to help identify high-risk loans based on a number of factors which describe the loan applicant.

## Results

- Naive Random Oversampling
  - Balanced Accuracy: 66.63%
  - Precision: 0.01
  - Recall: 0.70
- SMOTE Oversampling
  - Balanced Accuracy: 66.23%
  - Precision: 0.01
  - Recall: 0.63
- Undersampling
  - Balanced Accuracy: 66.23%
  - Precision: 0.01
  - Recall: 0.69
- Combination Sampling (SMOTEENN)
  - Balanced Accuracy: 54.47%
  - Precision: 0.01
  - Recall: 0.72
- Balanced Random Forest Classifier
  - Balanced Accuracy: 78.88%
  - Precision: 0.03
  - Recall: 0.70
- Easy Ensemble AdaBoost Classifier
  - Balanced Accuracy: 68.80%
  - Precision: 0.88
  - Recall: 0.38


## Summary

Most machine learning models produced accuracy between 66% and 68%, except combination sampling and balanced random forest classifier which had accuracies of 54% and 79%, respectively.

The precision (the ratio of correctly predicted high-risk loans to incorrectly predicted high-risk loans) of the models also typically fell around 1% and 3%, with the exception of the Easy Ensemble AdaBoost classifier, which had a precision score of 88%

Recall (the fraction of high-risk loans successfully predicted as high-risk) was also somewhat consistent across models, typically in the range of 69% to 72%, except SMOTE oversampling and Easy Ensemble AdaBoost Classifier which had recalls of 63% and 38%, respectively.

The Easy Ensemble AdaBoost Classifier (EEAC) produced the most precice model, but had poor recall relative to the other models. This means that while this model was able to predict with the most precision which loans were high risk, it had the highest rate of false negatives (high-risk loans it predicted as low-risk). The overall accuracy was in the typical range for the tested machine learning models.

Of all the machine learning algorithms tested, the EEAC is the most suitable for practical application. Because it has high precision and poor recall, it is most likely that the loans flagged as high-risk truly are high-risk. It is only able to identify about 40% of the actually high-risk loans, and about 10% of the results might be incorrectly flagged as high-risk. If these limitations are considered acceptable, than this model would be recommended for use.

The other models had extremely high false-positive rates which would limit their practical application, despite correctly identifying a higher perentage of the high-risk loans.


