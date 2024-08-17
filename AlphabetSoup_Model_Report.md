
# Alphabet Soup Deep Learning Model Report

## Overview of the Analysis

The purpose of this analysis is to create a binary classifier using machine learning techniques, including neural networks, to assist in the prediction of successful funding applications for a nonprofit foundation named Alphabet Soup. This deep learning model aims to classify whether an applicant will be successful based on various features in the dataset therefore predicting the best chance of success.

## Results

### Data Preprocessing

- **Target Variable:**
  - The target variable for the model is the `IS_SUCCESSFUL` column, which indicates if an applicant received funding.

- **Features:**
  - The features selected for the model include all columns except for `IS_SUCCESSFUL` and `INCOME_AMT`. The features represent various characteristics of the funding applications, such as the amount requested, the application type, a use case and other company features. 

- **Removed Variables:**
  - Columns that do not contribute to the predictive model or are redundant are removed. These included unique identifiers such as `EIN` and `NAME`.  The `INCOME_AMT` column was removed to optimise the model, and was considered redundant to the success of applicant ventures.

### Compiling, Training, and Evaluating the Model

- **Neurons, Layers, and Activation Functions:**
  - The neural network was designed with several layers:
    - **First Layer:** 80 neurons, ReLU activation function.
    - **Second Layer:** 20 neurons, ReLU activation function.
    - **Third Layer:** 10 neurons, ReLU activation function.
    - **Output Layer:** 1 neuron, Sigmoid activation function.
  - ReLU is a popular choice for activation functions in deep learning models.  It adds non-linear functionality to the model.  As the model is a series of layers adding a non-linear function like ReLU to this type of data assists in enabling the training of more complex relationships in the data. The Sigmoid activation function is a common choice for the output layer, and is advantageous to the binary classificaiton nature of our data, and its superior interpretation of probability.

- **Model Performance:**
  - The final model achieved an accuracy of approximately **73.4%** on the test data, which is below the target accuracy of 75%.
!(https://github.com/rtTAP/Deep-Learning-Challenge/blob/main/Images/Model_Performance.jpeg)


- **Steps to Increase Model Performance:**
  - Various approaches were used to optimize the model, including:
    - Tuning the number of neurons and layers
    - Experimenting with different activation functions
    - Adjusting the number of epochs for training
  - Despite these efforts, the accuracy remained slightly below the target

## Summary

The deep learning model created for predicting the success of funding applications achieved an accuracy of 73.4%, which is close to, but below the desired threshold. A suggestion may be that, while the model captures some underlying patterns in the data, it may not be fully optimised.

**Recommendation:**
To improve the classification performance, it may be beneficial to explore alternative machine learning models such as Random Forests, Gradient Boosting Machines, or Support Vector Machines. These models might be able to capture complex patterns in the data that the current deep learning model has not. Additionally, further feature engineering, hyperparameter tuning, or the use of more sophisticated neural network architectures (like deep or wide networks) could also be explored to improve the model's accuracy.
