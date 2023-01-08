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

![image](https://user-images.githubusercontent.com/31812730/211215985-36a8a14e-d402-4562-b11f-b027c368e39e.png)

![image](https://user-images.githubusercontent.com/31812730/211216025-5d8eb82f-e2ef-474c-ad51-85e08390b43c.png)

### Combination (Over and Under) Sampling

![image](https://user-images.githubusercontent.com/31812730/211216125-2e5ff55a-eb3a-4a6d-a43f-191f1daefa7e.png)

![image](https://user-images.githubusercontent.com/31812730/211216146-e5b033d0-e603-44e8-804e-7af5bd54a1d3.png)

### Ensemble Learners

**Balanced Random Forest Classifier**

![image](https://user-images.githubusercontent.com/31812730/211216676-13c515eb-78f4-45b0-8216-0f72523594ba.png)

![image](https://user-images.githubusercontent.com/31812730/211216699-a458bbd9-df47-4415-b1dd-f6c064b96ed0.png)

**Easy Ensemble AdaBoost Classifier**

![image](https://user-images.githubusercontent.com/31812730/211216986-56c7ee67-2bec-462b-b534-488ea9481959.png)

![image](https://user-images.githubusercontent.com/31812730/211217016-91bef702-ea78-43b9-a512-3276488b922d.png)

## Summary

The summary of the results for the "High Risk" candidates from each model is shown in the table below:

![image](https://user-images.githubusercontent.com/31812730/211220042-1b24b48b-1dc2-4aa8-a582-78eb75741c66.png)

After reviewing the results of all six models, it can be concluded that the EasyEnsembleClassifer model yields the best results with an accuracy rate of 93.2% and a 9% precision rate when predicting "High Risk" candidates. The sensitivity rate(recall) was also the highest at 94%. Same is true for predicting "Low Risk" candidates. The sensitivity rate at 94% and an F1 score of 97%. 

EasyEnsembleClassifer is the recommended model to perform this type of analysis.
