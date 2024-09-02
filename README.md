# deep-learning-challenge
## Deep Learning Model Analysis for Alphabet Soup
### Overview
The purpose of this analysis was to develop a deep learning model to predict the success of funding applications for Alphabet Soup, a hypothetical non-profit organization. By leveraging historical data on various features related to funding requests, the goal was to build a neural network that could classify whether an application would be successful or not. This predictive capability would allow Alphabet Soup to better allocate resources and make data-driven decisions in their grant-giving processes.

### Results
#### Data Preprocessing
#### Target Variable:

IS_SUCCESSFUL: Indicates whether a funding application was successful (1) or not (0). This is the target variable for our classification model.

#### Feature Variables:

Key features included:
APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, ASK_AMT, SPECIAL_CONSIDERATIONS

Removed Variables:
EIN and NAME

#### Model Compilation, Training, and Evaluation

- Layers and Neurons:
- Input Layer: Based on the number of input features.
- Hidden Layers:
- First hidden layer: 160 neurons with ReLU activation.
- Second hidden layer: 60 neurons with ReLU activation.
- Third hidden layer: 30 neurons with ReLU activation.
- Output Layer: 1 neuron with sigmoid activation for binary classification.
- Activation Functions:
- ReLU for hidden layers
- Sigmoid for the output layer to predict probabilities between 0 and 1.
- Performance:
- The model achieved an accuracy of 72.99%. 

#### Steps Taken to Improve Performance:

- Adding More Hidden Layers: Added additional layers to increase model complexity, with no improvement (72.91%).
- Increasing Neurons: Increased neurons in hidden layers to enhance model capacity, leading to no improvements (72.79%).
- Dropout Regularization: Implemented dropout layers to prevent overfitting, with little impact on performance (73.11%).
- Dropping Low-Correlation Features: Removed features with low or negative correlation to the target variable, which did not significantly improve accuracy (72.57%).

#### Summary
The deep learning model achieved a reasonable accuracy of around 72-73% but did not meet the initial target accuracy. Various strategies were employed to improve performance but these yielded limited success.
Given the limited improvement with various neural network architectures and optimizations, a different machine learning approach could be considered. Models such as Random Forests or Gradient Boosting Machines could potentially offer better performance.
