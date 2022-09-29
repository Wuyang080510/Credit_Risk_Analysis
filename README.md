# Credit_Risk_Analysis

## Project Overview
The purpose of this project is to use various machine learning models to predict credit risk. 
Six supervised machine learning models were used and evaluated to decide the best method of detecting credit risk. 

The machine learning algorithms used were:

1.	RandomOverSampler 
2.	SMOTE algorithms 
3.	ClusterCentroids algorithm 
4.	SMOTEENN algorithm 
5.	BalancedRandomForestClassifier (bias reduction model) 
6.	EasyEnsembleClassifier (bias reduction model)

A credit card credit dataset from LendingClub, a peer-to-peer lending services company, was used to perform the analysis. As the good loans data outnumber the risky loans, the data is intensively unbalanced. The resampling technique was used to enhance prediction accuracy. 

## Result

### Naive Random Oversampling
- Accuracy Score: 66.1%
- Precision High Risk: 1%
- Precision Low Risk: 100%
- Recall High Risk: 72%
- Recall Low Risk: 60%

![Random Oversampling Accuracy Score](https://github.com/Wuyang080510/Credit_Risk_Analysis/blob/main/image/RandomOversamplerAccuracyScore.png)

![Random Oversampling Confusion Matrix and Classification Report](https://github.com/Wuyang080510/Credit_Risk_Analysis/blob/main/image/RamdomOverSamplerConfusionMatrixandClassificationReport.png)

### SMOTE Oversampling
- Accuracy Score: 65.8%
- Precision High Risk: 1%
- Precision Low Risk: 100%
- Recall High Risk: 62%
- Recall Low Risk: 69%

![SMOTE Accuracy Score](https://github.com/Wuyang080510/Credit_Risk_Analysis/blob/main/image/SMOTEOversamplingAccuracyScore.png)

![SMOTE Confusion Matrix and Classification Report](https://github.com/Wuyang080510/Credit_Risk_Analysis/blob/main/image/SMOTEOversamplingConfusionMatrixand%20ClassificationReport.png)

### Cluster Centroids Undersampling
- Accuracy Score: 54.4%
- Precision High Risk: 1%
- Precision Low Risk: 100%
- Recall High Risk: 64%
- Recall Low Risk: 53%

![Cluster Centroids Accuracy Score](https://github.com/Wuyang080510/Credit_Risk_Analysis/blob/main/image/ClusterCentroidAccuracyScore.png)

![Cluster Centroids Confusion Matrix and Classification Report](https://github.com/Wuyang080510/Credit_Risk_Analysis/blob/main/image/ClusterCentroidConfusionMatrixandClassficationReport.png)

### SMOTEENN Sampling (combination of over- and under-sampling)
- Accuracy Score: 54.5%
- Precision High Risk: 1%
- Precision Low Risk: 100%
- Recall High Risk: 69%
- Recall Low Risk: 40%

![SMOTEENN Accuracy Score](https://github.com/Wuyang080510/Credit_Risk_Analysis/blob/main/image/smoteennAccuracyScore.png)

![SMOTEENN Confusion Matrix and Classification Report](https://github.com/Wuyang080510/Credit_Risk_Analysis/blob/main/image/smotennConfusionMatrixandClassficationReport.png)

### Balanced Random Forest Classifying
- Accuracy Score: 78.9%
- Precision High Risk: 3%
- Precision Low Risk: 100%
- Recall High Risk: 70%
- Recall Low Risk: 87%

![Balanced Random Forest Accuracy Score](https://github.com/Wuyang080510/Credit_Risk_Analysis/blob/main/image/BalancedRandomForestAccuracyScore.png)

![Balanced Random Forest Confusion Matrix and Classification Report](https://github.com/Wuyang080510/Credit_Risk_Analysis/blob/main/image/BalancedRandomForestConfusionMatrixandClassificationReport.png)

### Easy Ensemble AdaBoost Classifying 
- Accuracy Score: 93.2%
- Precision High Risk: 9%
- Precision Low Risk: 100%
- Recall High Risk: 92%
- Recall Low Risk: 94%

![Ensemble Accuracy Score](https://github.com/Wuyang080510/Credit_Risk_Analysis/blob/main/image/EnsembleClassifierAccuracyScore.png)

![Ensemble Confusion Matrix and Classification Report](https://github.com/Wuyang080510/Credit_Risk_Analysis/blob/main/image/EnsembleCassifierConfusionMatrixandClassificationReport.png)

## Summary
For a lending service provider, grand loans to an applicant with high credit risk will cause significant monetary loss for the company. It is more important to predict all the accounts with high credit risk. Therefore, the sensitive (recall) score is more important than the precision score when predicting credit risk. We want the model that lets the least amount of high-risk loans be undetected. 
The top three models for recall scores are:
- Easy Ensemble AdaBoost Classifying (92%)
- Naive Random Oversampling (72%)
- Balanced Random Forest Classifying (70%)

The balanced accuracy score is also a significant index to consider when determining a good machine learning model. Among the six machine learning models used in this analysis, Easy Ensemble AdaBoost Classifying has the highest accuracy score, which is 93.2%. Balanced Random Forest Classifying follows Ensemble AdaBoost Classifying with an accuracy score of 78.9%. 

Taking these two indicators under consideration, Easy Ensemble AdaBoost Classifying turned out to be the best model here for predicting high-risk loans.
