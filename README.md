# Neural Network Implementation (ANN_implementation)

This repository contains an implementation of an Artificial Neural Network (ANN) using TensorFlow for predicting customer churn based on the 'Churn_Modelling.csv' dataset.

## Contents

1. [Introduction](#introduction)
2. [Setup](#setup)
3. [Data Preparation](#data-preparation)
4. [Creating the Neural Network](#creating-the-neural-network)
5. [Training and Early Stopping](#training-and-early-stopping)
6. [Visualizing Training History](#visualizing-training-history)
7. [Making Predictions and Evaluation](#making-predictions-and-evaluation)
8. [Conclusion](#conclusion)
9. [Notebook File](#notebook-file)

## Introduction

This repository showcases the process of creating, training, and evaluating an ANN for predicting customer churn using TensorFlow. The dataset 'Churn_Modelling.csv' is used to train and evaluate the model.

## Setup

- Install TensorFlow using `!pip install tensorflow`.
- Import the required libraries: `numpy`, `matplotlib.pyplot`, `pandas`, and `tensorflow`.

## Data Preparation

- Load the dataset using `pd.read_csv('Churn_Modelling.csv')`.
- Divide the dataset into independent features (X) and the dependent feature (y).
- Perform one-hot encoding for categorical columns ('Geography' and 'Gender').
- Concatenate the one-hot encoded columns with the original feature set.
- Split the dataset into training and testing sets using `train_test_split()`.
- Scale the independent features using `StandardScaler`.

## Creating the Neural Network

- Initialize a Sequential model using `Sequential()`.
- Add Dense layers for the input, hidden, and output layers.
- Utilize activation functions ('relu' for hidden, 'sigmoid' for output).
- Compile the model with the 'Adam' optimizer, 'binary_crossentropy' loss, and accuracy metric.

## Training and Early Stopping

- Implement early stopping using the `EarlyStopping` callback.
- Train the model using `fit()`.
- Monitor validation loss and halt training if it doesn't improve.

## Visualizing Training History

- Access training history using `model_history.history`.
- Plot training accuracy and loss using `matplotlib.pyplot`.

## Making Predictions and Evaluation

- Predict outcomes on the test set using `classifiers.predict()`.
- Convert predicted probabilities into binary values (0 or 1).
- Compute the confusion matrix using `confusion_matrix()`.
- Calculate accuracy using `accuracy_score()`.

## Conclusion

This repository provides a complete implementation of building an ANN for predicting customer churn. It covers data loading, preprocessing, model creation, training with early stopping, visualization of training history, making predictions, and evaluating model accuracy.

## Notebook File

- The implementation details and code can be found in the [`ANN_implementation.ipynb`](ANN_implementation.ipynb) Jupyter Notebook.

---

Repository created by [@4Pranjal](https://github.com/4Pranjal)
