# deep-learning-challenge
Module 21

![image](https://github.com/user-attachments/assets/29c03ca7-fc4e-4f82-9d05-60295118555f)


# Navigation

 - Models
    - AlphabetSoupCharity - HDF5 file output created by initial training code.
    - AlphabetSoupCharity_Optimization - HDF5 file output created by optimization code.
 - AlphabetSoupCharity_Optimization - jupyter notebook file, created in Google Colab, that contains the code for optimizing the model.
 - README - contains final analysis.
 - Starter_Code_Colab - jupyter notebook file, created in Google Colab, that contains the initial code for training the model.

# Overview of the Analysis

The purpose of this project was to use machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

The results below are for the most optimized model 

## Results

Using bulleted lists and images to support your answers, address the following questions.

# Data Preprocessing

 - What variable(s) are the target(s) for your model?
   - The targets are the successful applicants. Within the dataset, this column is labeled as IS_SUCCESSFUL.

 - What variable(s) are the features for your model?
   - The features are all the other columns in the dataset. This includes but is not limited to, application types, income, ask amount, affiliation, and classification etc.

 - What variable(s) should be removed from the input data because they are neither targets nor features?
   - EIN and NAME columns can be removed as they are neither targets nor features.
  
# Compiling, Training, and Evaluating the Model

- How many neurons, layers, and activation functions did you select for your neural network model, and why?
   - Initially, I used two layers, the first with 80 nodes and the second with 30 nodes. I used one activation function, relu, for both layers. Since we've transformed the data to binary outputs the relu activation function is the most appropriate choice. For the output layer, I chose 1 node as it is a binary classifier model with only one output, ie was the funding application successful yes or no? The output layer activation of sigmoid was used since the model output is a binary classification between 0 and 1. These achieved an accuracy score of 73%, rounded.
 
- PHOTOS

  
