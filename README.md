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

The following classification algorithms were used for the purpose of carrying out a comparative study on the basis of their relative model performance viz.Logistic Regression, KNN, Gaussian Naïve Bayes, Kernel-Support Vector Machines, Decision Trees, Random Forests.
Each of the above models had been trained. The trained model had then been used to predict the labels corresponding to the validation set. Based on the relative performance of each of these models, the top three performing models had been selected.
The following table tabulates the details pertaining to the model used, hyper parameters (default parameters) used and 
the performance(accuracy) obtained for each of the classification models employed.

![image](https://github.com/medha-chippa/The-Analysis-and-Classification-of-Banking-Data-using-Ensemble-Semi-Supervised-Learning-/assets/55135185/ade5918e-4961-4dd8-ada6-b1ef896f89d4)

The top three performing models on the basis of their relative accuracies (depicted in the table above) are Support Vector Machines, Decision Trees and Random Forests, the accuracies of which are as follows viz. 90%, 89%,91% respectively.

The hyper parameters pertaining to each of the models were adjusted through the use of Grid Search. At the end of this process, a combination of the best hyper parameters are obtained on the basis of desired metric (accuracy in this case).

Ensemble Semi-Supervised Learning:
The validation set was assumed to be unlabeled. Self-labelling, a Semi-supervised learning had then been used to demonstrate the use unlabeled data for classification. This algorithm proceeds by utilizing the labelled samples of the dataset (training in this case) for the purpose of generating the labels corresponding to the unlabeled data (validation set in this case). The resultant labels (labels generated for the validation data) are then treated as true labels. The train data along with its correspond true labels and the validation data along with its corresponding predicted labels are combined and then used to train a classifier. This classifier is then used to predict the labels corresponding to the test data.
The performance of the final model depends on the quality of labels generated. For the purpose of improving the quality of the labels thus generated, a semi-supervised learning algorithm inspired by the tri-training method had been employed [3].
An ensemble of 3 models is used to self-label the validation set. The Majority voting scheme is then used to determine the final class label corresponding
to each of the samples in the validation set. As mentioned, the above three models are selected on the basis of their relative performance.

Post the successful construction of the model, each of these 3 models are trained on the training data. Since the validation set was assumed to be unlabeled, each of the trained models are used to self-label the validation set. The self-labels (predicted labels) are from here on treated as true labels. The training set with its original true labels and the validation set along with its self-labels are then collectively used to train a final model (random forest classifier).

The final model is then used to label the test data. In other words, the trained model is then used to predict the labels pertaining to the Test Data.

RESULTS:

A comparative study between the base line model and the primary model was conducted to assess the relative performance of the primary model and the base line model.

Base-Line Model/Vanilla Model: The model that was a result of collectively using the original true labels corresponding to both the train and validation sets for the purpose of training the final model.

Primary Model: The model that was a result of collectively using the original true labels corresponding to the training set and the self-labels corresponding to the validation set for the purpose of training the final model 

![image](https://github.com/medha-chippa/The-Analysis-and-Classification-of-Banking-Data-using-Ensemble-Semi-Supervised-Learning-/assets/55135185/fa501395-c85d-4aad-83cc-98975119913a)

![image](https://github.com/medha-chippa/The-Analysis-and-Classification-of-Banking-Data-using-Ensemble-Semi-Supervised-Learning-/assets/55135185/84b11e53-c616-4078-aab7-c9f37aa48526)

![image](https://github.com/medha-chippa/The-Analysis-and-Classification-of-Banking-Data-using-Ensemble-Semi-Supervised-Learning-/assets/55135185/6e257bef-afe0-4575-81ad-627bcbf1fae8)










