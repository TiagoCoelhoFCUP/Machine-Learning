# Bayes Decision Boundary & Bias-Variance Trade-off

Evaluating how good is the approximation of a certain model to the Bayes Decision Boundary without knowing the probability density function of the data is only possible by observing the actual boundary produced. With that said, we used three different methods that directly attempt to approximate the Bayes Decision Boundary, to predict the Outcome in the Pima Indians Diabetes dataset (https://www.kaggle.com/uciml/pima-indians-diabetes-database), using only two predictors so that the produced boundaries can be observed. The methods used were:
<ul>
  <li> K-nearest neighbours (where we tried different values of k to further understand the influence of the hyperparameter in the produced boundary) </li>
  <li> Logistic Regression </li>
  <li> Quadratic Discriminant Analysis </li>
</ul>

Each of these models has different assumptions and will lead to different degrees of expressiveness, which results in different biases and variances for each one. This was also studied in this work, by comparing the results of the different methods.

![plots](https://user-images.githubusercontent.com/13381706/163276904-ca8a65ee-6c41-4aeb-998f-8f64abf8e9f1.png)

The bias-variance trade-off was also studied in more detail with the Yeast UCI dataset (https://archive.ics.uci.edu/ml/datasets/Yeast), in which we selected the best model to predict the localization sites of proteins, among the K-nearest neighbours, logistic regression and decision trees. In order to make the best selection possible, we divided the dataset set in train and test, then, in the train we performed hyparameter tuning and cross validation to validate the models with the best parameters. In the end we compare the different methods in the test set. Since localization site of proteins is heavily unbalanced, the methods that were used to train the models take that into consideration. 

The dataset yeast is composed by eight predictors that describe properties of proteins and a response that is a class of the localization site of the protein in the observation. The goal is to build a classification system that predicts the cellular localization sites of proteins.

After selecting the best models for each of the method studied we are left out with four models, the Logistic Regression, k-nearest neighbours with k=15, the Bagging Classifier with less variance and the Random Forest with 3 max features. Logistic Regression accuracy is around 50%, and the other three models around 60%, so the first model studied is clearly not the best choice for the yeast dataset.

![image](https://user-images.githubusercontent.com/13381706/163277172-625d03ea-52d5-4113-ad32-9fb9788ad18f.png)
