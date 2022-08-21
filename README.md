## Neural Network Charity Analysis

## Overview
Create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Results
### Data Preprocessing

* The target variable is "IS_SUCCESSFUL" which indicates if funding was successful.

* The features of the model include:
APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT

* The feature that was dropped
    * EIN: Employee Identification Number
    * NAME (was initially removed but re-added during the optimization phase)

### Compiling, Training, and Evaluating the Model

* There were 2 hidden layers in the neural network. The 1st layer contained 80 neurons and the 2nd hidden layer contained 30 neurons. The activation functions selected for each neural network were the ones listed below to each layer respectively:

    * "ReLu" Rectified Linear Unit activation function for the input layers. I used this function so that not all neurons need to be activated. If the output of the linear tranformation of the neuron was less than 0, then the neuron did not need to be activated. This would filter out many projects that would be unsucessful from receiving ABC funding.
    * Sigmoid activation function for the output layer.

* The initial accuracy from the deep-learning model was 72%. After optimizing the model, the accuracy reached 77.9%.

* In order to increase the performance of the model, I dropped the 'SPECIAL_CONSIDERATIONS' column and kept the 'NAMES' column, binned the 'NAMES' column, and raised the number of nodes in the 1st hidden layer by 85.

## Summary
The initial accuract of the deep learning neural network model in predicting the success or failure of a project that would receive ABC investment was 72%. After optimizing the model by keeping the "NAMES" column, binning the "NAMES" column, and increasing the 1st hidden layer by 85 nodes, the accuracy of the model increased by 77.9%

### Recomendation: 
A Random Forest Hierarchical Model may have solved the classification problem by being able to rank the importance of certain features/categorical variables.