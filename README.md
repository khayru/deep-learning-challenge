
Overview:

The purpose of this analysis from Alphabet Soup’s business team I was given the CSV  file containing more than 34,000 organizations that have received. 
For this assignment, I started using a Jupyter Notebook

Results: Using bulleted lists and images to support your answers, address the following questions:

What variable(s) are the target(s) for your model?

APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special considerations for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

What variable(s) are the features of your model?

What variable(s) should be removed from the input data because they are neither targets nor features?
Compiling, Training, and Evaluating the Model

EIN and NAME—Identification columns have been dropped without affecting the model.

How many neurons, layers, and activation functions did you select for your neural network model, and why?
The layer 3 layer, 8 hidden_nodes_layer1,  and 840 promes.

# Define the model - deep neural net, i.e., the number of input features and hidden nodes for each layer.
input_number = len(X_train[0])
hidden_nodes_layer1 = 8
hidden_nodes_layer2 = 5

_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
dense (Dense)                (None, 8)                 840       
_________________________________________________________________
dense_1 (Dense)              (None, 5)                 45        
_________________________________________________________________
dense_2 (Dense)              (None, 1)                 6         
=================================================================
Total params: 891
Trainable params: 891
Non-trainable params: 0


Were you able to achieve the target model performance?
I was able to achieve the target of 72% model accuracy 

# Evaluate the model using the test data
model_loss, model_accuracy = nn.evaluate(X_test_scaled,y_test,verbose=2)
print(f"Loss: {model_loss}, Accuracy: {model_accuracy}")
8575/8575 - 2s - loss: 0.5634 - acc: 0.7264
Loss: 0.5633616806883853, Accuracy: 0.7264139652252197

What steps did you take in your attempts to increase model performance?
No action was found, and no neurons have been added.

Summary: 
Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

My recommendation about this deep learning model, after I developed the model I was able to achieve 72% accuracy. I believe this is a good module to put into practice. An accuracy close to considering to be a good model 
my opping is to get high accuracy than 72% by

 1-add more data 
 2-check data cleaning
 3- use a different model 
