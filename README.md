# Credit_Risk_Analysis
## Overview of Analysis
## Purpose:
- Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, I employed different techniques to train and evaluate models with unbalanced classes. I used imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.
#### Deliverable 1:
- Using imbalanced-learn and scikit-learn libraries, I evaluated three machine learning models by using resampling to determine which is better at predicting credit risk. First, I used the oversampling RandomOverSampler and SMOTE algorithms, and then the undersampling ClusterCentroids algorithm. Using these algorithms, I resampled the dataset, viewed the count of the target classes, trained a logistic regression classifier, calculated the balanced accuracy score, generated a confusion matrix, and generated a classification report.
#### Deliverable 2:
- Using imbalanced-learn and scikit-learn libraries,I used a combinatorial approach of over- and undersampling with the SMOTEENN algorithm to determine if the results from the combinatorial approach are better at predicting credit risk than the resampling algorithms from Deliverable 1. Using the SMOTEENN algorithm, I resampled the dataset, viewed the count of the target classes, trained a logistic regression classifier, calculated the balanced accuracy score, generated a confusion matrix, and generated a classification report.
#### Deliverable 3:
- Using imblearn.ensemble I trained and compared two different ensemble classifiers (BalancedRandomForestClassifier and EasyEnsembleClassifier). These algorithms helped me to resample the dataset, view the count of the target classes, train the ensemble classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.
## Results
RandomOverSampler model
![Screen Shot 2022-11-09 at 7 49 02 PM](https://user-images.githubusercontent.com/106174279/200988527-e245d8d2-eea2-4a1c-97d3-2aab0e73409d.png)
- The balanced accuracy score is 65%.
- The high_risk precision is about 1% only with 62% sensitivity which makes a F1 of 2% only.
- Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 68%.
SMOTE model
![Screen Shot 2022-11-09 at 7 49 59 PM](https://user-images.githubusercontent.com/106174279/200988709-3da0acca-3792-4a4d-b0bd-0ea73e789bdd.png)
- The balanced accuracy score is 64%.
- The high_risk precision is about 1% only with 63% sensitivity which makes a F1 of 2% only.
- Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 66%.
ClusterCentroids model
- The balanced accuracy score is 65%
![Screen Shot 2022-11-09 at 7 40 59 PM](https://user-images.githubusercontent.com/106174279/200987569-93f273e2-7d04-4417-9d11-18e380c395be.png)
- The high_risk precision is about 1% only with 61% sensitivity which makes a F1 of 1% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 45%.
![Screen Shot 2022-11-09 at 7 42 59 PM](https://user-images.githubusercontent.com/106174279/200987781-404e7fbf-c7ac-4316-a2e6-95f15de1f06d.png)
SMOTEENN model
- The balanced accuracy score is about 62%.
- The high_risk precision is still 1% only with 68% sensitivity which makes a F1 of only 2%.
- Due to the high number of false positives, the low_risk sensitivity is 57%.
![Screen Shot 2022-11-09 at 8 03 43 PM](https://user-images.githubusercontent.com/106174279/200990646-f7c5f2eb-a97b-4b00-8c65-a82856f585a7.png)

BalancedRandomForestClassifier model
- The balanced accuracy score improved to about 79%.
- The high_risk precision is still low at 4% only with 67% sensitivity which makes a F1 of only 7%.
- Due to a lower number of false positives, the low_risk sensitivity is now 91% with 100% presicion.
![Screen Shot 2022-11-09 at 8 02 48 PM](https://user-images.githubusercontent.com/106174279/200990466-6d17902d-81a1-4542-8aef-031e6438d956.png)

EasyEnsembleClassifier model
- The high_risk precision is still low at 7% only with 91% sensitivity which makes a F1 of only 14%.
- Due to a lower number of false positives, the low_risk sensitivity is now 94% with 100% presicion.
![Screen Shot 2022-11-09 at 8 02 21 PM](https://user-images.githubusercontent.com/106174279/200990380-cd97ad66-1617-4c9c-929e-cee995a213b5.png)

## Summary 
- Results of machine learning models
- recommendation on the model to use
- justify reasoning
The models we used to discover the credit risk analysis have shown very weak precision when it comes to see if credit risk is high. However, the ensomble models brought some improvement in regards to the sensitivity of the high risk credits. For example, the easyensembleclassifier model shows 92% recall. This says that it can find almost all the high risk credit. Yet with low precisions, many of the low risk credis are wrongly detected as high risk. This would not be good for the bank's credit strategy and infringe on its revenue because it is missing business.
I would not recommend that the bank uses any of these models to predict credit risk.
