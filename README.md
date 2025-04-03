# Alphabet Soup NN Model Analysis 

## Overview

The following analysis was completed for the nonprofit foundation, Alphabet Soup, who needs a tool that can help it select the applicants for funding with the best chance of success in their ventures. To complete this, a binary classifier, such as the neural network model, was used to predict whether an organization receiving funding will be successful or not. 2 versions of the model were evaluated to compare accuracy. 

## Results 

### Data Preprocessing 
The dataset contained  over 34,000 records with information on past funding applicants including ... 
 - The **target variable** was the 'ISSUCESSFUL' column used for binary classification in both models. 
 - **Model 1 features** included everything in the dataset except the 'EIN' and "NAME' columns as those were unique identifiers that were considered non-beneficial for the first neural network model. Binning was also performed for low-frequency columns such as 'APPLICATION_TYPE', and 'CLASSIFICATION' where less common values were combined under "Other." 
 - **Model 2 features** included everything in the dataset except the 'EIN', 'STATUS', 'SPECIAL_CONSIDERATIONS' as those were considered non-beneficial for the optimized neural network model. Binning was also performed for low-frequency columns such as 'APPLICATION_TYPE', 'CLASSIFICATION', and 'NAME' where less common values were combined under "Other." 
###  Compiling, Training, and Evaluating the Model 
 ***Neural Network Model 1***: 
 
 The first neural network model was created by first using StandardScalar to scale numerical features and also splitting the data into training and testing datasets. The actual model was composed using ... 
 
 - Hidden Layers: 2 
 - Neurons Per Layer: 80 -> 30 
 - Activation Functions: relu -> relu -> sigmoid
 - Epochs: 100 
 
 The result was *72.31%* accuracy.  
 
***Neural Network Model 2***: 

The second neural network model was created by first using StandardScalar to scale numerical features and also splitting the data into training and testing datasets. The actual model was composed using ...  
 - Hidden Layers: 3
 - Neurons Per Layer: 100 -> 30 - 10
 - Activation Functions: relu -> relu -> sigmoid -> sigmoid 
 - Epochs: 100 

The result was *78.57%* accuracy.

## Summary 

In conclusion, the second optimized deep learning model achieved a final accuracy of 78.57%, showing an improvement over the initial model’s 72.31% accuracy. The addition of an extra hidden layer, refined feature selection, and optimized activation functions contributed to this increase in performance. However, despite these improvements, the model still has room for enhancement. An alternative machine learning model such as the Random Forest Classifier could also be used as it handles categorical data as well and can provide better interpretability through feature importance analysis. 
