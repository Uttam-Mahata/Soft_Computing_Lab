# Assignment 1: Machine Learning Basics

This assignment covers the fundamental concepts of machine learning, including classification, regression, and model evaluation. The assignment is divided into several notebooks, each focusing on a different dataset and problem.

## Notebooks

- **Iris Flower Classification**: A classic classification problem to predict the species of an iris flower based on its sepal and petal measurements. The notebook demonstrates how to build and evaluate a simple classification model.
- **Mobile Price Range Prediction**: A classification problem to predict the price range of mobile phones based on their features. The notebook explores various classification models and analyzes their performance in terms of accuracy and overfitting/underfitting.
- **Melbourne House Price Prediction**: A regression problem to predict the price of houses in Melbourne. This assignment includes two notebooks that explore the dataset, perform feature engineering, and apply various regression models to predict house prices. The notebooks also analyze the impact of feature selection and model complexity on the prediction accuracy.

- **Housing Price Prediction**: A regression problem to predict the sale price of houses. The notebook covers data preprocessing, feature engineering, and the implementation of various regression models. It also includes an analysis of overfitting and underfitting.

### Theory

#### Classification

Classification is a supervised learning task where the goal is to predict the categorical class labels of new instances based on past observations. The output variable is a category, not a continuous value.

**Mathematical Notation:**

Given a set of training data $D = \\{(x_1, y_1), (x_2, y_2), ..., (x_n, y_n)\\}$ where $x_i$ is a feature vector and $y_i$ is a class label from a set of classes $C = \\{c_1, c_2, ..., c_k\\}$, the goal is to learn a function $f: X \\to Y$ that maps a feature vector $x$ to a class label $y$.

The performance of a classification model is often evaluated using metrics like accuracy, precision, recall, and F1-score.

#### Regression

Regression is a supervised learning task where the goal is to predict a continuous value. In this assignment, regression is used to predict house prices.

**Mathematical Notation:**

Given a set of training data $D = \\{(x_1, y_1), (x_2, y_2), ..., (x_n, y_n)\\}$ where $x_i$ is a feature vector and $y_i$ is a continuous target variable, the goal is to learn a function $f: X \\to Y$ that maps a feature vector $x$ to a continuous value $y$.

The performance of a regression model is often evaluated using metrics like Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared.

#### Overfitting and Underfitting

- **Overfitting**: A model that performs well on training data but poorly on unseen data is said to be overfitted. This happens when the model learns the training data too well, including the noise.
- **Underfitting**: A model that performs poorly on both training and unseen data is said to be underfitted. This happens when the model is too simple to capture the underlying patterns in the data.

**Mathematical Notation:**

The trade-off between bias and variance is a key concept in understanding overfitting and underfitting. The mean squared error (MSE) of an estimator can be decomposed as:

$$MSE = Bias^2 + Variance + Irreducible Error$$

- A model with high bias is underfitted.
- A model with high variance is overfitted.
