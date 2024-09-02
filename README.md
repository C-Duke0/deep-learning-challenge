# deep-learning-challenge
Deep Learning Model Analysis for Alphabet Soup
Overview
The purpose of this analysis was to develop a deep learning model to predict the success of funding applications for Alphabet Soup, a hypothetical non-profit organization. By leveraging historical data on various features related to funding requests, the goal was to build a neural network that could classify whether an application would be successful or not. This predictive capability would allow Alphabet Soup to better allocate resources and make data-driven decisions in their grant-giving processes.

Results
Data Preprocessing
Target Variable:

IS_SUCCESSFUL: Indicates whether a funding application was successful (1) or not (0). This is the target variable for our classification model.
Feature Variables:

All other variables in the dataset were considered features, except for the non-contributing ones identified later. Key features included:
APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, ASK_AMT, SPECIAL_CONSIDERATIONS
Removed Variables:

EIN and NAME: These identifiers were removed because they do not provide predictive value.
Additional features with low or negative correlation with IS_SUCCESSFUL were also removed, including AFFILIATION_CompanySponsored, ORGANIZATION_Association, CLASSIFICATION_C2100, APPLICATION_TYPE_T19, APPLICATION_TYPE_T4, etc.
Model Compilation, Training, and Evaluation
Neural Network Architecture:

Layers and Neurons:
Input Layer: Based on the number of input features.
Hidden Layers:
First hidden layer: 160 neurons with ReLU activation.
Second hidden layer: 60 neurons with ReLU activation.
Third hidden layer: 30 neurons with ReLU activation.
Output Layer: 1 neuron with sigmoid activation for binary classification.
Activation Functions:
ReLU for hidden layers, chosen for its effectiveness in preventing the vanishing gradient problem.
Sigmoid for the output layer to predict probabilities between 0 and 1.
Performance:

The model achieved an accuracy of approximately 72-73%. Despite various optimization attempts, the model did not meet the higher target performance of 75-80%.
Steps Taken to Improve Performance:

Adding More Hidden Layers: Added additional layers to increase model complexity, with minimal improvement.
Increasing Neurons: Increased neurons in hidden layers to enhance model capacity, leading to slight accuracy improvements.
Dropout Regularization: Implemented dropout layers to prevent overfitting, with little impact on performance.
Changing Activation Functions: Tested different activation functions like Leaky ReLU, but saw no significant improvement.
Dropping Low-Correlation Features: Removed features with low or negative correlation to the target variable, which did not significantly improve accuracy.
Hyperparameter Tuning: Conducted a randomized search for optimal hyperparameters using Keras Tuner, but saw marginal improvements.
Summary
The deep learning model achieved a reasonable accuracy of around 72-73% but did not meet the initial target accuracy. Various strategies were employed to improve performance, including architecture changes, feature selection, and hyperparameter tuning, but these yielded limited success.

Recommendations
To potentially improve model performance, consider the following alternatives:

Ensemble Methods: Techniques like Random Forests or Gradient Boosting Machines could provide better performance and robustness for tabular data.
Support Vector Machines (SVM): SVMs might be effective for binary classification, especially for non-linear relationships.
Logistic Regression with Feature Engineering: A simpler, well-regularized logistic regression model with enhanced feature engineering could achieve comparable or better results.
Given the current performance and the dataset characteristics, exploring these alternative machine learning models is recommended.

