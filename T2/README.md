# Dataset Generation

In most Supervised Machine Learning Classification tasks, a dataset consisting of predictor variables and a target variable is given, and the aim is to find a function that maps the predictor variables into the target variable. The task proposed in this assignment was, however, given a method from a set of methods, to generate a dataset in which the given method performs better than all others.
The generated datasets for each model were developed according to the assumptions of each method, though, in some cases, we observed that other models performed as well as the method that we developed the dataset for. In the end, we were able to generate datasets for the whole set of models and interpret why each method performed well for each dataset.

The main objectives of our work are (a) to show that there is not a best general method for every dataset there is. Indeed, the choice of the best method very much depends on the data points one is given, as we will show in the following sections. The other main objective is (b) to show that, even though some of the methods used can always be approximated by other methods (e.g., a multilayer feedforward network with a non-polynomial activation function can approximate any continuous function), the complexity needed to perform such an approximation may not be worthwhile.

In order to accomplish the objectives proposed in the previous section, we have used ten different methods which are listed in the following paragraph. The **Logistic Regression (LR)** and the **Linear Discriminant Analysis (LDA)** are both based on a linear assumption. However, the latter also assumes that each class can be modeled by a Gaussian distribution, with all the classes sharing the same covariance matrix. The **Quadratic Discriminant Analysis (QDA)** assumes that the decision boundary is quadratic and, like LDA, that all classes follow a Normal distribution. However, in QDA, the classes can have different covariance matrices. **Decision Trees (DTs)** were also used, which are a very flexible method, but prone to overfitting, as well as **Random Forests (RFs)**, which are an ensemble of DTs. In what concerns **Support Vector Machines (SVMs)**, we have used three different types of kernels: **linear**, **polynomial** and **radial basis**. Finally, we have used **Multilayer Perceptrons (MLPs)**, which can be an extremely powerful method, with two types of activation functions: **ReLU** and **TanH**.

![image](https://user-images.githubusercontent.com/13381706/163273537-4a7dbd93-476d-4514-9803-90139a2e6c48.png)



