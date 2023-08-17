# The-Analysis-and-Classification-of-Banking-Data-using-Ensemble-Semi-Supervised-Learning-

The analysis of Banking Data for the purpose of classifying customers into their likelihood of subscribing to a Term 
Deposit or not based on the marketing efforts in place. This is a binary classification problem that is centered around 
classifying customers into two classes based on their likelihood of subscribing to a Term Deposit given the marketing 
efforts in place. A machine learning approach inspired by the Tri-training approach has been employed.

DATASET

The Banking Dataset-Marketing Targets dataset out-lines the marketing campaigns conducted by a Portuguese 
Banking Institution and has primarily been sourced from the UCI Machine Learning repository with the inclusion of a 
few additional attributes. The dataset is a .csv file that is an open source resource available for a quick download [2]. 
The website houses two .csv files, namely train.csv, test.csv

The marketing campaigns were primarily based on telephonic conversations. 
The train data would be used for training, validation. The test data would be used for testing.
The train Dataset consists of 45,211 samples, 17 predictors and 1 response variable ordered by date (from May 2008 
through November 2010)
The test Dataset consists of 4521 samples, 17 predictors and 1 response variable.

PERFORMANCE MEASURES

Train and Test Accuracies:

The accuracy of both the base model and our model would be measured over the train data and the test data. A 
comparative study on the same would be carried out to identify possible over fitting or under fitting of data.
Accuracy over Cross Validated data:
10-Fold Cross Validation would be employed to ensure the model is unbiased towards the data at hand.

Confusion Matrix:

The Confusion matrix would be generated and examined to observe certain aspects of model performance such as the 
number of true positives, true negatives, false positives and false negatives.

OVERVIEW

![image](https://github.com/medha-chippa/The-Analysis-and-Classification-of-Banking-Data-using-Ensemble-Semi-Supervised-Learning-/assets/55135185/cbcf9dc4-a02d-4ff5-b4d4-a4dee8cecf65)

The data had been divided in the propotion 60:20:20, constituting the train, test and validation sets respectively.

The following classification algorithms were used for the purpose of carrying out a comparative study on the 
basis of their relative model performance viz. Logistic Regression, KNN, Gaussian Naïve Bayes, Kernel-Support 
Vector Machines, Decision Trees, Random Forests.
Each of the above models had been trained. The trained model had then been used to predict the labels corresponding 
to the validation set.
Based on the relative performance of each of these models, the top three performing models had been selected.
The following table tabulates the details pertaining to the model used, hyper parameters (default parameters) used and 
the performance(accuracy) obtained for each of the classification models employed.







