# Credit_Risk_Analysis

## Overview
The purpose of this project is to use the available dataset and predict credit risk with machine learning techniques. Several machine learning models are used to predict credit risk using the credit card credit dataset from LendingClub, a peer-to-peer lending services company. 

Credit risk is an unbalanced classification problem because good loans outnumber the risky loans. In this analysis, different techniques are used to train and evaluate models with unbalanced classes. 

Imbalanced-learn and scikit-learn libraries are used to build and evaluate models using resampling. Data was oversampled using the RandomOverSampler and SMOTE algorithms, and undersampled using the ClusterCentroids algorithm. SMOTEENN algorithm was used for a combinatorial approach of over- and undersampling.

Two machine learing models, BalancedRandomForestClassifier and EasyEnsembleClassifier are used to compare and to predict credit risks. The performance of these models were evaluated and a recommendation was provided on whether they should be used to predict credit risk.

## Results

### Oversampling

**Naive Random Oversampling**

![image](https://user-images.githubusercontent.com/31812730/211210755-4e1aefe0-c30e-4857-85cd-0c60492485cf.png)

![image](https://user-images.githubusercontent.com/31812730/211210797-1c42151c-22fb-4f72-9769-c1b5c1f3db83.png)

**SMOTE Oversampling**

![image](https://user-images.githubusercontent.com/31812730/211210889-52b93c02-02b1-4f4d-aa69-0a13bddeeb67.png)

![image](https://user-images.githubusercontent.com/31812730/211210914-a0296ca9-935d-40b7-b77c-8f33cebd2cb9.png)

### Undersampling



## Summary
In reviewing all six models, the EasyEnsembleClassifer model yielded the best results with an accuracy rate of 93.2% and a 9% precision rate when predicting "High Risk candidates. The sensitivity rate (aka recall) was also the highest at 92% compared to the other models. The result for predicting "Low Risk" was also the highest with the sensitivity rate at 94% and an F1 score of 97%. Therefore, if a model needed to be recommended to perform this type of analysis, then this one would be the clear choice.

Ranking of models in descending order based on "High Risk" results:

EasyEnsembleClassifer: 93.2% accuracy, 9% precision, 92% recall, and 16% F1 Score
BalancedRandomForestClassifer: 78.9% accuracy, 3% precision, 70% recall and 6% F1 Score
SMOTE: 65.2% accuracy, 1% precision, 61% recall and 2% F1 Score
SMOTEENN: 64.5% accuracy, 1% precision, 72% recall and 2% F1 Score
RandomOverSampler: 64.0% accuracy, 1% precision, 66% recall and 2% F1 Score
ClusterCentroids: 54.5% accuracy, 1% precision, 69% recall and 1% F1 Score
A side note that should be considered is that original dataset had 99% of the applications classified as "Low Risk" with only 1% of the data classified in the "High Risk" category. This may skew the results greatly as there is a risk that the Machine Learning algorithms are creating clusters drawing from too small of a dataset of actual "High Risk" applications. This margin of risk might not be something that banks would be comfortable accepting.
