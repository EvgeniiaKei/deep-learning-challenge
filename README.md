# deep-learning-challenge
Module 21

![image](https://github.com/user-attachments/assets/29c03ca7-fc4e-4f82-9d05-60295118555f)


# Navigation

 - [Models](https://github.com/EvgeniiaKei/deep-learning-challenge/tree/main/Models)
    - AlphabetSoupCharity - HDF5 file output created by initial training code.
    - AlphabetSoupCharity_Optimization - HDF5 file output created by optimization code.
    - AlphabetSoupCharity_Optimization1 - HDF5 file output created by optimization code.
 - [Starter_Code_Colab](https://github.com/EvgeniiaKei/deep-learning-challenge/blob/main/Starter_Code_Colab.ipynb) - jupyter notebook file, created in Google Colab, that contains the initial code for training the model.
 - [AlphabetSoupCharity_Optimization](https://github.com/EvgeniiaKei/deep-learning-challenge/blob/main/AlphabetSoupCharity_Optimization.ipynb), [AlphabetSoupCharity_Optimization1](https://github.com/EvgeniiaKei/deep-learning-challenge/blob/main/AlphabetSoupCharity_Optimization1.ipynb) - jupyter notebook file, created in Google Colab, that contains the code for optimizing the model.
 - README - contains final analysis.

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

1. How many neurons, layers, and activation functions did you select for your neural network model, and why?
   
   -  I implemented a two-layer architecture, with the first layer consisting of 80 nodes and the second layer having 30 nodes. I employed the ReLU activation function for both layers. Given that the data has been transformed into binary outputs, ReLU is the most suitable activation function. For the output layer, I opted for a single node, as this is a binary classification model that only requires one output: whether the funding application was successful (yes or no). I utilized the sigmoid activation function for the output layer, as it produces binary classifications ranging from 0 to 1. This configuration resulted in an accuracy score of approximately 73%

#  Optimization

 - First Optimization Attempt: 2 hidden layers & an outer layer, layer 1: 132 neurons, relu activation, layer 2: 66 neurons, relu activations, and Outer layer: 1 unit, sigmoid activation & adam optimizers for complier. (accuracy score of 72.6%)

 - After Attempt: Use auto-optimizing tuner (Best accuracy score of 72.8%)

 - Last Attempt: Optimized the model by adding an additional layer, adjusting the number of nodes, and leaving the name column as a feature.

   

2.  Were you able to achieve the target model performance?
   
    - Yes, with the optimization changes I was able to generate an accuracy score of 79% (rounded), which is higher than the acceptable criteria of 75%.
 

3.  What steps did you take in your attempts to increase model performance?
   
    - Added a third layer and changed the number of nodes for each layer to 80, 45, and 35 respectively. However, this did not seem to increase my accuracy score. So I reprocessed the data to include the name column, adding it as another feature, and then trained the model again, this time receiving an accuracy score of 78.85%.
There are several factors that suggest using the name as a feature could enhance the model's accuracy. The "name" column may hold significant information relevant to the classification task, which the model can utilize for learning. For instance, in some scenarios, names might indicate particular categories or classes. Additionally, the "name" column could be correlated with the target variable or other features within the dataset. Incorporating such correlated features enables the model to identify more intricate relationships in the data. Ultimately, including additional features, especially those that provide valuable insights, can contribute to the model's overall complexity.
 

# Summary

Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

In summary, the initial deep learning model achieved an accuracy score of 0.7282 with a loss of 0.5662, utilizing two layers with 80 and 30 nodes, respectively. The model excluded the name column from the original dataset. After optimization, the accuracy improved to 0.7884, and the loss decreased to 0.494, employing three layers with 80, 45, and 35 nodes, respectively. The optimized model included the name column as a feature.

To enhance the performance of the deep learning model, I recommend implementing additional preprocessing steps on the data to identify potential improvements in accuracy. This could involve techniques such as feature scaling, normalization, or handling missing values more effectively, which may lead to better model performance.

Additionally, we could explore using a Random Forest model as an alternative. Random Forest is particularly effective for nonlinear data and can handle both regression and classification tasks. Its ensemble approach not only improves accuracy but also reduces the risk of overfitting compared to a single model. This flexibility makes Random Forest a strong candidate for classifying funding application outcomes.







