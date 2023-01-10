
Dataset 
The Mushroom Dataset is originally donated to the UCI Machine Learning repository. It includes 21 categorical variables which are the basic characteristics of mushrooms such as `odor`, `ring_type`, `gill_size`, and `veil_type`, and the dataset has 8124 observations. The label that is used to predict is `class` and it has two classes, `p` means poison, and `e` which means edible. 

Methods
To get a high accuracy prediction, Decision Tree, Logistic Regression, Random Forest, K-nearest neighbors and will be used to predict the class of the mushroom. The model which performs the best based on its accuracy will be used as the final model. The processes of the analysis including:
Data cleaning: 
Checking if there are any missing values.
Since all the variables are categorical variables, they need to be changed to dummy variables with 0 or 1 for further prediction.
Data segregation: The dataset will be divided into training set (80%) and test set (20%)
Model fitting and predicting: Fit all the models mentioned and get accuracy from each. Then compare the accuracy and pick the one with the highest accuracy score. 

Production and Expectation
This analysis will be performed in python notebook (Google Collab), and a PowerPoint will be given based on EDA, findings, and model predictions. At the end of this project, I am expected to learn basic knowledge about the characteristics of mushrooms by EDA, and get a model with a high accuracy which can be used as a reference when mushroom sellers dealing with different types of mushrooms. 

Findings 

Data Cleaning
There is no missing value in the dataset and all the data points are keep as it. 
EDA
21 categorical variables are in the data, and all of them are the characteristics of mushroom. The plots below are the example of some of the characters.
By looking at the dataset, the target variable is `class` which indicates if the mushroom is edible or poison. There are 4208 (51.8%) are edible and 3916 (48.2%) are poison. The number of observations in the two categories are close.

Looking at the count of cap shape, convex and bell shape are the most common shapes among all the shapes listed in the dataset. 

The habitat bar plot shows that most of the mushroom are captured in urban (u), grass (g) and meadows (m).

                     	 

Compare the population between class, several (v) is the most common population in both. But most of the several populations are poison.

Data pre-processing 
Since all the variables are categorical, they are all converted to dummies, which 1 indicates “yes”, and 0 indicates “no”. For instance, cap-shape are divided into 6 columns (cap-shape_b, cap-shape_c, cap_shape_f, etc), when any observation contains the characteristic, it equal to 1 and 0 otherwise). After converting all the features into dummies, target variable is extracted (‘class’). Then, the data is divided into train and test data set (80%-20%).
 
Classification Models
Five models are used to fit and test the mushroom data set, the metric that used to see the performance of the models is the accuracy rate, which corresponds to the proportion of observations that have been correctly classified. The models are including:

Random Forest
 
The accuracy of the random forest model is 100%. By looking at the confusion matrix, the false positive and false negative are 0, which can be concluded that random forest model predicts the test dataset 100% correct.


Logistics Regression

The accuracy of the logistics regression model is about 99.82%. By looking at the confusion matrix, the false positive and false positive is 3, which cut down the accuracy rate by approximate 0.1.


Naïve Bayes

The accuracy of the Naïve Bayes model is about 96.06%. By looking at the confusion matrix, the false positive and false positive is 2, and false negative is 62, which cut down the accuracy rate by about 4%.


K-Nearest Neighbor

The accuracy of the KNN model is 100% with the number of neighbors of 5. By looking at the confusion matrix, the false positive and false negative are 0, which can be concluded that random forest model predicts the test dataset 100% correct.



Decision Tree

The accuracy of the Decision Tree model is about 99.57% with max_depth of 10, random_state of 100, min_samples_leaf of  20. By looking at the confusion matrix, the false positive and false positive is 7, and false negative is 0, which cut down the accuracy rate by about 1%.



Limitation 
By looking back to the result of the models that made, random forest and KNN model perform “perfect” with an accuracy rate of 100%. The reason for the perfect score is that there are some features that have an imbalance distribution on the target. In other words, some of the feature has a big impact on the target variable. The variable importance score plot below shows that odor_ n, gill_size_b, odor_f, and gill_size_n has a big effect in distinguish the class of the mushroom.

Other than the extremely high accuracy rate, all the features need to be identified by eyes, which is time consuming. Therefore, it is needed to have an advance method to detective the features.
 
Future Step
To better use machine learning to distinguish the class of mushrooms, pictures of mushroom can be added into the dataset so that Neural Network Model can be used to detected if the mushroom is poison or edible.
