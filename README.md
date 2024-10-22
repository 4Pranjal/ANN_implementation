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
## Getting Started
To get started with the complete projects including all the algorithm, follow these steps:

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/4Pranjal/ANN_implementation.git
   ```

2. Navigate to the directory:

   ```bash
   cd ANN_implementation
   ```

3. Install the required libraries:

   ```bash
   pip install -r requirements.txt
   ```
---

## Data Preparation

- Load the dataset using `pd.read_csv('Churn_Modelling.csv')`.
- Divide the dataset into independent features (X) and the dependent feature (y).
- Perform one-hot encoding for categorical columns ('Geography' and 'Gender').
- Concatenate the one-hot encoded columns with the original feature set.
- Split the dataset into training and testing sets using `train_test_split()`.
- Scale the independent features using `StandardScaler`.
---
## Creating the Neural Network

- Initialize a Sequential model using `Sequential()`.
- Add Dense layers for the input, hidden, and output layers.
- Utilize activation functions ('relu' for hidden, 'sigmoid' for output).
- Compile the model with the 'Adam' optimizer, 'binary_crossentropy' loss, and accuracy metric.
---
## Training and Early Stopping

- Implement early stopping using the `EarlyStopping` callback.
- Train the model using `fit()`.
- Monitor validation loss and halt training if it doesn't improve.
---

## Making Predictions and Evaluation

- Predict outcomes on the test set using `classifiers.predict()`.
- Convert predicted probabilities into binary values (0 or 1).
- Compute the confusion matrix using `confusion_matrix()`.
- Calculate accuracy using `accuracy_score()`.
---
## Results
After training the model we got this as our results, 

![111](https://github.com/user-attachments/assets/37c62e41-549c-4238-a574-29d69ca690ac)

1. Train Loss (blue line): The training loss remains relatively stable throughout the training process, fluctuating slightly but showing no clear improvement trend. It hovers around 0.44 to 0.46, suggesting the model struggles to reduce loss further as training progresses.

2. Test Loss (orange line): The test loss shows higher variability, with sharp fluctuations between 0.38 and 0.42. Despite these fluctuations, test loss remains lower than the training loss, indicating potential overfitting, where the model performs better on unseen data but doesn’t generalize well.

A more stable and converging loss curve would indicate better training.

![222](https://github.com/user-attachments/assets/17f60929-e661-4ea8-8014-ea278db700c6)

---
## Conclusion

This repository provides a complete implementation of building an ANN for predicting customer churn. It covers data loading, preprocessing, model creation, training with early stopping, visualization of training history, making predictions, and evaluating model accuracy.

## 🙏 Contributors

This repository is maintained by 4Pranjal. Feel free to use and modify the code for educational and research purposes.

For any questions or suggestions, you can contact me through my GitHub profile: [@4Pranjal](https://github.com/4Pranjal).

Made with ❤️ by [Pranjal Jain](https://github.com/4Pranjal)

---
 
