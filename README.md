# Credit-Risk-Analysis

## OVERVIEW OF THE LOAN PREDICTION RISK ANALYSIS: 

This project analyzes how all the factors in our loan_stats csv can help predict the credit risk status of credit card users. We used imbalanced-learn and scikit-learn libraries to design models and evaluate them using a resampling method. This includes: 

- Oversample the data using the RandomOverSampler and SMOTE algorithms. 

- Undersample the data using the ClusterCentroids algorithm. 

- Use a combinatorial approach of over and undersampling using the SMOTEENN algorithm. 

-Compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.

- Evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.



## RESULTS AND ANALYSIS:

## 1. Naive Random Oversampling: 


![1_RandomOversampler](https://user-images.githubusercontent.com/104735724/185832754-b8ca03d9-163b-42fc-b154-deb4789468e0.png)

- Precision: High Risk = 0.01; Low Risk = 1.00

- Recall: High Risk = 0.74; Low Risk = 0.58

- Balanced Accuracy Score = 0.66 (66%)

- Accuracy score is very less


## 2. SMOTE Oversampling: 


![2_SMOTE](https://user-images.githubusercontent.com/104735724/185833142-a12a82f8-6088-4ea7-a908-71769235e35a.png)


- Precision: High Risk = 0.01; Low Risk = 1.00

- Recall: High Risk = 0.62; Low Risk = 0.68

- Balanced Accuracy Score = 0.65 (65%)

- Accuracy score is very less


## 3. Cluster Centroids Undersampling: 


![3_ClusterCentroids](https://user-images.githubusercontent.com/104735724/185833267-38dbcb8d-729f-48c6-bb1b-9843df051a43.png)


- Precision: High Risk = 0.01; Low Risk = 1.00

- Recall: High Risk = 0.66; Low Risk = 0.41

- Balanced Accuracy Score = 0.55 (55%)

- Accuracy score went down as compared to the last algorithm


## 4. SMOTEENN (Combination of Over and Understanding):


![4_SMOTEENN](https://user-images.githubusercontent.com/104735724/185833501-622f1f5a-1e57-456b-af21-f183a523aa2f.png)


- Precision: High Risk = 0.01; Low Risk = 1.00

- Recall: High Risk = 0.77; Low Risk = 0.59

- Balanced Accuracy Score = 0.68 (68%)

- Accuracy score has imporved over last algorithm but still low


## 5. Balanced Random Forest Classifier:


![5_BalancedRandomForestClassifier](https://user-images.githubusercontent.com/104735724/185833618-70ed317c-6a92-4af9-8b4c-4859f1f8511d.png)


- Precision: High Risk = 0.03; Low Risk = 1.00

- Recall: High Risk = 0.70; Low Risk = 0.87

- Balanced Accuracy Score = 0.79 (79%)

- Accuracy Score is reasonaly good, much better than the 4 algorithms above


## 6. Easy Ensemble AdaBoost Classifier:


![6_EasyEnsembleClassifier](https://user-images.githubusercontent.com/104735724/185833723-a5b66e25-3b1f-46a9-96bd-3c4a6a93f921.png)


- Precision: High Risk = 0.09; Low Risk = 1.00

- Recall: High Risk = 0.92; Low Risk = 0.94

- Balanced Accuracy Score = 0.93 (93%)

- Accuracy score is very good - the best amongst all 6 algorithms


## SUMMARY: 

- The Balanced Random Forest Classifier and Easy Ensemble AdaBoost Classifier performed way better than the Oversampling, Undersampling and Combination algorithms. 

- Cluster Centroids undersampling had the worst algorithm with a score of 54%, while Easy AdaBoost Classifier had the best with a score of 93%. 

- The low-risk precision score stays the same across the board as 1.00. 

- Easy Ensemble AdaBoost Classifier has the best high-risk precesion score at 0.09 and combined lowest in all Oversampling/Undersampling/Combination algorithms at 0.01.

- The Oversampling/Undersampling/Combination algorithms also fare poorely than the Ensemble algorithms in terms of recall scores for both high-risk and low-risk loans.


## Recommendation: 

I would recommend ADABOOST because it has the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.

