# Credit_Risk_Analysis
Apply machine learning techniques to solve a real-world challenge: credit card risk

## Overview of the analysis:
The purpose of our analysis was to apply machine learning to a credit card dataset from LendingClub (a peer to peer lending service company) in order to predict credit risk. Our analysis was completed by using the following six sampling algorithms:<br>
- Oversampling with RandomOverSampler and SMOTE
- Undersampling with ClusterCentroids
- Combination over- / undersampling with SMOTEENN
- Ensemble sampling with BalancedRandomForestClassifier and EasyEnsembleClassifier

After sampling the data with each of these algorighms, our final task was to evaluate the metrics that were gathered to determine which model (if any) could be used to predict future high risk customers.

## Results:
Our six sampling models produced the following results.<br>

Key metrics for each model include:<br>
Balanced Accuracy Score - Measures effectiveness of a binary classifier on imbalanced classes to predict both true positives and true negatives.<br>
Precision - Percentage of true positive predictions that were correct.<br>
Recall - Percentage of positive results that were predicted correctly.<br>
F1 / Harmonic Mean - Single summary statistic balancing Precision and Recall.<br>

#### 1. Random Oversampling --
- Balanced Accuracy Score: 0.6573
- Precision (high risk): 0.01
- Recall (high risk): 0.71
- F1 / Harmonic Mean (high risk): 0.02

![Random Oversampling Metrics](https://github.com/jmueller187/Credit_Risk_Analysis/blob/main/Resources/RandomOversamplingMetrics.png)

#### 2. SMOTE Oversampling --
- Balanced Accuracy Score: 0.6622
- Precision (high risk): 0.01
- Recall (high risk): 0.63
- F1 / Harmonic Mean (high risk): 0.02

![SMOTE Oversampling Metrics](https://github.com/jmueller187/Credit_Risk_Analysis/blob/main/Resources/SMOTEOversamplingMetrics.png)

#### 3. Cluster Centroids Undersampling --
- Balanced Accuracy Score: 0.5442
- Precision (high risk): 0.01
- Recall (high risk): 0.69
- F1 / Harmonic Mean (high risk): 0.01

![Cluster Centroids Uncersampling Metrics](https://github.com/jmueller187/Credit_Risk_Analysis/blob/main/Resources/UndersamplingMetrics.png)

#### 4. SMOTEENN Combination Sampling --
- Balanced Accuracy Score: 0.6447
- Precision (high risk): 0.01
- Recall (high risk): 0.72
- F1 / Harmonic Mean (high risk): 0.02

![SMOTEENN Combination Sampling Metrics](https://github.com/jmueller187/Credit_Risk_Analysis/blob/main/Resources/SMOTEENNCombinationSamplingMetrics.png)

#### 5. Balanced Ramdon Forest Ensemble Sampling --
- Balanced Accuracy Score: 0.7885
- Precision (high risk): 0.03
- Recall (high risk): 0.70
- F1 / Harmonic Mean (high risk): 0.06

![Random Forest Classifier Metrics](https://github.com/jmueller187/Credit_Risk_Analysis/blob/main/Resources/RandomForestClassifierMetrics.png)

#### 6. Easy Ensemble AdaBoost Sampling --
- Balanced Accuracy Score: 0.9317
- Precision (high risk): 0.09
- Recall (high risk): 0.92
- F1 / Harmonic Mean (high risk): 0.16

![Easy Ensemble AdaBoost Metrics](https://github.com/jmueller187/Credit_Risk_Analysis/blob/main/Resources/EasyEnsembleAdaBoostMetrics.png)

## Summary:
After reviewing the results of the six sampling models, we saw that the Easy Ensemble AdaBoost Sampling returned the best metrics. Even though this was the top performing model, we do not recommend using any of the models to evaluate and predict credit risk. This is because each model had an extremely low F1 score, which tells us that there was a pronounced imbalance between Precision and Recall scores. As seen in our Results, Precision scores were low and Recall scores were high. Without having a balance between these scores, our models will not be able to predict credit risk accurately.
