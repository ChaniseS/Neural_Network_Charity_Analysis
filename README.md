# Neural_Network_Charity_Analysis
## Overview:
This analysis was broken into three parts:
1. Preprocessing the data for the neural network
2. Compile, Train and Evaluate the Model
3. Optimizing the model

While using Neural Networks and Machine Learning, I was able to use features in the dataset to create a binary classifier that will help predict if the applicants that will be funded by a Charitable organization, called Alphabet Soup, will be successful. 
With this analysis we had a dataset containing various measures on 34,000 organizations that have been funded by Alphabet Soup. 

## Results:
**Data Processing**
- What variable(s) are considered the target(s) for your model?
  - IS_SUCCESSFUL Column is the target in my model
- What variable(s) are considered to be the features for your model?
  - APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT are the features in my model
- What variable(s) are neither targets nor features, and should be removed from the input data?
  - The EIN and NAME columns are identification information and have been removed from the input data.
**Compiling, Training, and Evaluating the Model**
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
  - This network model is made of 2 hidden layers with 80 and 30 neurons respectively. The input data has 43 features and 25,724 samples. The output layer is made of a unique neuron as it is a binary classification. To speed up the training process, we are using the activation function ReLU for the hidden layers. As our output is a binary classification, Sigmoid is used on the output layer.
For the compilation, the optimizer is adam and the loss function is binary_crossentropy.
- Were you able to achieve the target model performance?
  - Although the model accuracy turned out to be pretty high at under 75%, it's not a enough of a performance to help predict the outcome of the charity donations.
- What steps did you take to try and increase model performance?
  - To increase the performance of the model, we applied bucketing to the feature ASK_AMT and organized the different values by intervals.
We increased the number of neurons on one of the hidden layers, then we used a model with three hidden layers.
We also tried a different activation function (tanh) but none of these steps helped improve the model's performance.

## Summary:
The Deep Learning Neural Network Model had an accuracy score of 50% after optimization. The initial neural network had a accuracy score of 69%.
This loss in accuracy can be explained from the fact that the model overfitted.
We could take it a step further and optimize our neural network by removing more features or simply adding more data to the dataset to increase accuracy.
