# Breast Cancer Classification Using a Neural Network

This notebook demonstrates how to build and train a neural network for breast cancer classification. The dataset used is the Breast Cancer dataset from the UCI Machine Learning Repository.

## Neural Networks

A neural network is a computational model inspired by the structure and function of the human brain. It consists of interconnected nodes, called neurons, organized in layers. The network learns to perform tasks by adjusting the weights of the connections between neurons.

### Architecture

The neural network in this notebook has the following architecture:

-   **Input Layer**: The number of neurons in the input layer is equal to the number of features in the dataset.
-   **Hidden Layer**: A single hidden layer with 10 neurons.
-   **Output Layer**: A single output neuron that predicts the probability of breast cancer recurrence.

### Activation Function

The sigmoid activation function is used in both the hidden and output layers. The sigmoid function maps any input to a value between 0 and 1, which is ideal for binary classification problems.

**Mathematical Expression:**

$`\sigma(z) = \frac{1}{1 + e^{-z}}`$

## Dataset

The dataset used is the Breast Cancer dataset from the UCI Machine Learning Repository. It contains 286 instances and 9 features. The target variable is "Class", which indicates whether there was a recurrence of breast cancer.

## Data Preprocessing

The notebook performs the following data preprocessing steps:

-   **One-Hot Encoding**: Categorical features are converted into numerical format using one-hot encoding.
-   **Standardization**: Numeric features are scaled using the `StandardScaler` to have a mean of 0 and a standard deviation of 1.
-   **Handling Missing Values**: Missing values are filled with the mode (most frequent value) of the respective column.

## Training

The neural network is trained using the backpropagation algorithm. The goal is to minimize the error between the predicted output and the actual output. The error is calculated using the Mean Squared Error (MSE) function.

**Mean Squared Error (MSE):**

$`E = \frac{1}{2n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2`$

## Evaluation

The performance of the model is evaluated using the following metrics:

-   **Accuracy**: The proportion of correctly classified instances.
-   **Confusion Matrix**: A table that shows the number of true positives, true negatives, false positives, and false negatives.
-   **Classification Report**: A report that includes precision, recall, and F1-score for each class.

### K-Fold Cross-Validation

To ensure the robustness of the model, 5-fold cross-validation is performed. The dataset is split into 5 folds, and the model is trained and tested 5 times, with each fold being used as the test set once.
