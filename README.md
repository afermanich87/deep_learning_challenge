# deep_learning_challenge

## Overview
The nonprofit foundation Alphabet Soup wants a tool to select the applicants for funding with the best chance of success in their ventures. Using knowledge of machine learning and neural networks, the features in the provided dataset will be used to predict whether applicants will be successful if funded by Alphabet Soup. The below results go through the steps taken to achieve a more accurate model. 

## Results
### Data Preprocessing

* The target variable for this model is the `IS_SUCCESSFUL` column
* The following variables are features for this model:
 	1. `NAME` (added as a feature for the optimized model)
 	2. `APPLICATION_TYPE`
 	3. `AFFILIATION`
 	4. `CLASSIFICATION`
 	5. `USE_CASE`
 	6. `INCOME_AMT`
 	7. `ASK_AMT`
* The following variables were removed from the data:
	1. `EIN`
	2. `SPECIAL_CONSIDERATIONS`
	3. `STATUS`
	4. `ORGANIZATION` (removed for the optimized model)

### Compiling, Training, and Evaluating the Model

The following plot depicts the accuracy of the original data model:

![image](https://github.com/afermanich87/deep_learning_challenge/assets/120151717/d919c315-8866-46a7-8b26-5dd1dfbfcb96)

* For the final, optimized model there were 3 inner layers and one outer layer created. The number of neurons in each layer can be seen in the snapshot of code below. I used ReLu for the activation on the inner layers and Sigmoid as the activation for the outer layer. 

![image](https://github.com/afermanich87/deep_learning_challenge/assets/120151717/20562c6a-ac1c-41af-9d6c-6063524b8404)

* The original trained model predicted an accuracy level of ~73%. Using various methods of optimization the trained model was able to achieve above the 75% target threshold with a final accuracy level of ~78% (as seen in the plot below).

![image](https://github.com/afermanich87/deep_learning_challenge/assets/120151717/c7340b51-4801-4bf4-8565-47ad54a69956)


* To achieve the optimized model, the name column was added back to the binning process due to the variabilty. The organization column was additionally dropped to reduce the number of columns and had fewer unique values in comparison with the other featured columns. A third neuron layer was added to the neural netowork to add complexity. Finally, the epochs and number of neurons were increased from the original trained model. Through the various changes and some trial and error, I was able to achieve an accuracy level over 75%. 

### Summary

* The final optimized model was able to predict outcomes with 78% accuracy. While this was a marked increase from the original trained model, which was predicting outcomes with only 73% accuracy, there may be different models that could better classify this dataset. The k-nearest neighbors algorithm, for example, could be a better model by using algorithims to determine the ouput based on classifying the input by similar "neighboring" data. 


### Resources
Received help from TA's during office hours. Asked specifically about how to save HDF5 files in Google Colab. Lastly, I used the activites from module 21 as a guide for setting up the neural network model.
