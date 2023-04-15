# Neural_Network_Charity_Analysis

## Overview of the analysis

The purpose of this analysis is to create and evaluate a deep learning model to predict the success of AlphabetSoup's funding applications. The model is designed to assist the company in determining which applications to approve or reject, maximizing their impact on the projects they support.

## Results

### Data Preprocessing

- Target variable: 'IS_SUCCESSFUL' (binary variable indicating if the funding application was successful or not)
- Features: All remaining variables excluding 'EIN' and 'NAME' (e.g., 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', 'ASK_AMT')
- Variables to be removed: 'EIN' (Employer Identification Number) and 'NAME' (Name of the organization), as they do not contribute relevant information for predicting the success of funding applications.

## Compiling, Training, and Evaluating the Model

- For the neural network model, we selected:
  - 2 hidden layers with 80 and 30 neurons, respectively, chosen based on the input features' complexity and the need to capture non-linear relationships.
  - Activation functions: ReLU for the hidden layers to mitigate vanishing gradient issues and improve training speed, and sigmoid for the output layer to generate binary predictions.
- The model achieved an accuracy of 72%, which is slightly below the target performance of 75%.

- To increase model performance, I took the following steps:

  - Tuned hyperparameters, such as the number of hidden layers, neurons, and activation functions.
  - Implemented dropout layers to reduce overfitting.
  - Adjusted the batch size and number of training epochs.
  - Applied feature scaling and encoding to preprocess the input data.
  
## Summary

The deep learning model achieved an accuracy of 72% in predicting the success of AlphabetSoup's funding applications. Although it falls slightly short of the target performance, the model can still provide valuable insights for the organization.

For an alternative approach, we recommend trying a Gradient Boosting Classifier. This model is known for its high performance in handling complex datasets, and its ability to automatically learn feature interactions can potentially improve the prediction accuracy. Additionally, gradient boosting models are less prone to overfitting, which might contribute to better performance on unseen data.
