# Assignment 5: Character Recognition using Neural Networks

This assignment demonstrates the use of neural networks for character recognition from two different types of displays: a 7-segment display for digits and a 5x5 grid for alphabets.

## Part 1: 7-Segment Digit Recognition

This part of the assignment focuses on recognizing digits (0-9) from a 7-segment display.

### Dataset

A balanced dataset is generated with 100 valid patterns (10 for each digit) and 100 invalid patterns. The valid patterns are oversampled to create a larger training set.

### Neural Network Architecture

-   **Input Layer**: 7 neurons (one for each segment of the display).
-   **Hidden Layers**: Two hidden layers with 10 neurons each.
-   **Output Layer**: 1 neuron for binary classification (valid or invalid digit).

### Activation Function

The sigmoid activation function is used in all layers.

**Mathematical Expression:**

$`\sigma(z) = \frac{1}{1 + e^{-z}}`$

### Training and Evaluation

The network is trained using backpropagation with the Mean Squared Error (MSE) loss function. The performance is evaluated using 5-fold cross-validation, and the average accuracy, precision, recall, F1-score, and specificity are reported.

## Part 2: 7-Segment Alphabet Recognition

This part of the assignment focuses on recognizing alphabets (A-Z) from a 5x5 grid display.

### Dataset

A dataset of 5x5 grid patterns for alphabets A-Z is generated, with variations created by flipping, shifting, and rotating the original patterns. This is augmented with 100 invalid patterns.

### Neural Network Architecture

-   **Input Layer**: 25 neurons (for the 5x5 grid).
-   **Hidden Layers**: Two hidden layers with 16 and 12 neurons, respectively.
-   **Output Layer**: 1 neuron for binary classification.

### Training and Evaluation

Similar to the digit recognition task, the network is trained using backpropagation with the MSE loss function and evaluated using 5-fold cross-validation.

## Key Concepts

### Backpropagation

Backpropagation is an algorithm used to train neural networks by calculating the gradient of the loss function with respect to the weights of the network. The weights are then updated in the opposite direction of the gradient to minimize the loss.

### Mean Squared Error (MSE)

The MSE is a common loss function used in regression and binary classification problems. It measures the average squared difference between the actual and predicted values.

**Mathematical Expression:**

$`E = \frac{1}{2n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2`$

### K-Fold Cross-Validation

K-fold cross-validation is a technique used to evaluate the performance of a model in a more robust way. The dataset is split into *k* folds, and the model is trained and tested *k* times, with each fold being used as the test set once. The final performance is the average of the performances on each fold.
