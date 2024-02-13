# deep-learning-challenge
Module 21

# Module 21 Report

## Overview of the Analysis

   


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

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
  --no change compared to attempt 2
  --268/268 - 0s - loss: 0.5721 - accuracy: 0.7256 - 374ms/epoch - 1ms/step
Loss: 0.5721397995948792, Accuracy: 0.7255976796150208



## Summary
