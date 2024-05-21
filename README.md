# Report on the Neural Network Modeling Optimization for Alphabet Soup Charity

## Files:
- **AlphabetSoupCharity_Optimization.ipynb:** 
  - This Jupyter Notebook contains the preprocessing steps for the Alphabet Soup Charity project.
- **AlphabetSoupCharity.h5:** 
  - This HDF5 file contains the optimized neural network model.
- **AlphabetSoupCharity_Optimization.h5:** 
  - This file contains the model architecture of the optimized neural network designed to achieve higher than 75% accuracy.

## Overview of the Analysis:
The objective of this analysis was to develop a deep learning model for predicting the success of charity donations for Alphabet Soup. The aim was to achieve a predictive accuracy exceeding 75% through data preprocessing, neural network model design, optimization, and performance evaluation.

## Results/Data Preprocessing:
- **Target Variable(s):** 'IS_SUCCESSFUL' indicates the success or failure of a charity donation.
- **Feature Variables:** 
  - Includes APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT, and IS_SUCCESSFUL.
- **Variables Removed:** 
  - 'EIN' and 'NAME' columns were eliminated as they weren't relevant to the analysis.

## Results/Compiling, Training, and Evaluating the Model:
The neural network consisted of multiple dense layers, including hidden layers with appropriate activation functions.
- **Number of Layers:** 
  - The latest neural network model utilized four layers: an input layer, three hidden layers, and an output layer. Each hidden layer incorporates a dropout layer to enhance robustness. The first hidden layer employs ReLU activation, the second employs tanh activation, and the third employs sigmoid activation. This selection aims to strike a balance between model complexity and generalization, facilitating the capture of diverse data patterns.
- **Activation Functions:** 
  - ReLU is used for all dense layers except the output layer, which uses the sigmoid activation function suitable for binary classification.

## Summary:
Despite trying various optimization techniques like adjusting neuron count, layer depth, activation functions, optimizers, and learning rates, the model only achieved around 72.57% accuracy and fell short of the 75% target. While the model showed promise, further exploration and refinement are needed.

## Recommendation:
Considering the limitations of the deep learning model, a gradient boosting classifier like XGBoost or LightGBM may be more suitable. These models are known for their accuracy with tabular data like ours and could potentially provide the accuracy boost we're looking for.
