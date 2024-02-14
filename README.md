# deep-learning-challenge
Module 21

# Module 21 Report

## Overview of the Analysis

   


## Results

1.  What variable(s) are the target(s) for your model? IS_SUCCESSFUL
2.  What variable(s) are the feature(s) for your model? APPLICATION_TYPE (created dummies), AFFILIATION, CLASSIFICATION (created dummies), USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
3.  What variable(s) should be removed from the input data because they are neither targets nor features? NAME and EIN, however I did try to test removing NAME
4.  How many neurons, layers, and activation functions did you select for your neural network model, and why? In the intial model I used 2 layers with 80 and 30 neurons respectively. Activation function relu was used for layer 1 and 2, sigmoid was used for the output layer.  
5.  Were you able to achieve the target model performance? No
6.  What steps did you take in your attempts to increase model performance? Interestingly, all steps during optimization reduced model performance by XXX

* Initial Model:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  --268/268 - 1s - loss: 0.5568 - accuracy: 0.7266 - 502ms/epoch - 2ms/step
Loss: 0.5568206906318665, Accuracy: 0.7266472578048706

* Optimization Attempt 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  --268/268 - 1s - loss: 0.5648 - accuracy: 0.7254 - 536ms/epoch - 2ms/step
Loss: 0.5648394227027893, Accuracy: 0.725364446640014
             
* Optimization Attempt 2:
  * Added third  hidden layer, incresed from 80, 30 to 100 and 20 and added a third hidden layer with 20 
  --268/268 - 0s - loss: 0.5721 - accuracy: 0.7256 - 481ms/epoch - 2ms/step
Loss: 0.5721397995948792, Accuracy: 0.7255976796150208

* Optimization Attempt 3:
  * Change 'relu' to 'sigmoid' in layers 1 and 2, increase neurons to 120, 80, 40  
  --initally reduced epoch to 50
  --268/268 - 1s - loss: 0.5660 - accuracy: 0.7257 - 554ms/epoch - 2ms/step
Loss: 0.5660290718078613, Accuracy: 0.7257142663002014



## Summary
Note, did not save every 5 epochs during optimization due to time it takes to run the model.
Unable to achieve greater accuracy than in the initial model.  