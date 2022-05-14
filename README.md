# Neural Network Charity Analysis
## Overview of the loan prediction risk analysis:
The purpose of this project is to use deep-learning neural networks with TensorFlow platform in Python, to analyze and classify the success of charitable donations.
I have used the following methods for the analysis:
* preprocessing the data for the neural network model,
* compile, train and evaluate the model,
* optimize the model.
## Resources:
* charity_data.csv
* Python
* Jupyter Notebook
## Results:
### Data Preparation:
* EIN and Name columns were dropped as they don’t bring any value to the analysis.
* The column IS_SUCCESSFUL contains binary data refering to weither or not the charity donation was used effectively. This variable is then considered as the target for our deep learning neural network.
* The rest of the columns, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT, were used as features for the model.
### Model Training, and Model Evaluation:
* This deep-learning neural network model is made of two hidden layers with 80 and 30 neurons respectively.
The output layer is made of a unique neuron as it is a binary classification.
To speed up the training process, I used the activation function ReLU for the hidden layers. As output is a binary classification, Sigmoid is used on the output layer.
For the compilation, the optimizer is adam and the loss function is binary_crossentropy.
* The model accuracy is under 75%. This is not a satisfying performance to help predict the outcome of the charity donations.
* To increase the performance of the model, I applied bucketing to the feature ASK_AMT and organized the different values by intervals.
I increased the number of neurons on one of the hidden layers, then we used a model with three hidden layers.

I also tried a different activation function (tanh) but none of these steps helped improve the model's performance.
## Summary:
I didn’t reach the goal of 75% accuracy for the model.

**Recommendation:**
As potential improvements I would try to remove such columns as application type and classification. They may occur to be noisy feature. The increase of quantity of neurons seems to be insufficient. The changes should be done in preprocessing dataset.

