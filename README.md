# Credit_Risk_Analysis
Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, analyze, predict credit risk.

Overview of the loan prediction risk analysis:

### Background:
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, we’ll need to employ different techniques to train and evaluate models with unbalanced classes. We used imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.Various libraries and algorithms were used to build and evaluate models using resampling including:

imbalanced-learn
scikit-learn
RandomOverSampler
SMOTE algorithms
ClusterCentroids algorithm
SMOTEENN algorithm
BalancedRandomForestClassifier (bias reduction model)
EasyEnsembleClassifier (bias reduction model)

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once we’re done, we’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

### Purpose of this analysis:
Explain how a machine learning algorithm is used in data analytics.
Create training and test groups from a given data set.
Implement the logistic regression, decision tree, random forest, and support vector machine algorithms.
Interpret the results of the logistic regression, decision tree, random forest, and support vector machine algorithms.
Compare the advantages and disadvantages of each supervised learning algorithm.
Determine which supervised learning algorithm is best used for a given data set or scenario.
Use ensemble and resampling techniques to improve model performance.

#### Results:
The results for the six machine learning models including their respective balanced accuracy, precision, and recall scores are as follows:

#### Naive Random Oversampling

![alt_text](https://github.com/RGK73/Credit_Risk_Analysis/blob/main/Images/Naive_Random_Sampling.png)

Balanced Accuracy: 0.7856360112968401

Precision: The precision is low for High-risk loans and is high for Low-risk loans.

Recall: High/Low risk = .71/.86

#### SMOTE Oversampling

![alt_text](https://github.com/RGK73/Credit_Risk_Analysis/blob/main/Images/SMOTE_oversampling.png)

Balanced Accuracy: 0.7966770207605626

Precision: The precision is low for High-risk loans and is high for Low-risk loans.

Recall: High/Low risk = .71/.88

#### Undersampling

![alt_text](https://github.com/RGK73/Credit_Risk_Analysis/blob/main/Images/undersampling.png)

Balanced Accuracy: 0.7742313998976678

Precision: The precision is low for High-risk loans and is high for Low-risk loans.

Recall: High/Low risk = .77/.78

#### Combination Under-Over Sampling

![alt_text](https://github.com/RGK73/Credit_Risk_Analysis/blob/main/Images/combined_under_over_sampling.png)

Balanced Accuracy: 0.7975462408998795

Precision: The precision is low for High-risk loans and is high for Low-risk loans.

Recall: High/Low risk = .72/.87

#### Balanced Random Forest Classifier

![alt_text](https://github.com/RGK73/Credit_Risk_Analysis/blob/main/Images/Balanced_Random_Forest_Classifier.png)

Balanced Accuracy: 0.7818811414482034

Precision: The precision is low for High-risk loans and is high for Low-risk loans.

Recall: High/Low risk = .64/.92

#### Easy Ensemble AdaBoost Classifier

![alt_text](https://github.com/RGK73/Credit_Risk_Analysis/blob/main/Images/Easy_Ensemble_AdaBoost_Classifier.png)

Balanced Accuracy: 0.9254565671948463

Precision: The precision is low for High-risk loans and is high for Low-risk loans.

Recall: High/Low risk = 0.07/1.00

### Summary:
When working with balanced accuracy, the highest compared accuracy between 0 and 1 and is closest to 1 is the best machine learning model. For the credit card data set, the Easy Ensemble AdaBoost Classifier is the best model to choose with its 1.00 balanced accuracy. The other models were below .90 balanced accuracy. The precision for all models were similar and within an appropriate range. The recall score also needs to fall within 0 and 1, with numbers closer to 1 being the better model. The Easy Ensemble AdaBoost Classifier had the highest recall score, making it the final best machine learning model to choose for further credit card analysis.
