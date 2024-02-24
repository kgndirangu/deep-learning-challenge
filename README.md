# deep-learning-challenge
Module 21

# Module 21 Report

## Overview of the Analysis
The analysis aimed to support nonprofit foundation Alphabet Soup in allocating funds to the ventures most likely to succeed. for funding with the best chance of success in their ventures. Data from 34,000 organizations that previously received funding from Alphabet Soup are available to train a machine learning model (specifically neural networks) to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.


## Results

1.  What variable(s) are the target(s) for your model? IS_SUCCESSFUL
2.  What variable(s) are the feature(s) for your model? APPLICATION_TYPE (created dummies), AFFILIATION, CLASSIFICATION (created dummies), USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
3.  What variable(s) should be removed from the input data because they are neither targets nor features? NAME and EIN, however I did try to test removing NAME. The model with the 'NAME' coulmn was unable to run on my machine due to RAM issues. 
4.  How many neurons, layers, and activation functions did you select for your neural network model, and why? The initial model used 2 layers with 80 and 30 neurons respectively. Activation function relu was used for layer 1 and 2, sigmoid was used for the output layer. Three optimization attempts were made (please see question #6).  
5.  Were you able to achieve the target model performance? None of those 3 attempts improved accuracy 
6.  What steps did you take in your attempts to increase model performance? The optimization steps tested below decreased model performance: 

* Initial model:
* 2 layers (80 and 30 neurons) with activation function relu; output layer used sigmoid
  * Loss: 0.5568206906318665, 
  * Accuracy: 0.7266472578048706

* Optimization Attempt 1:
  * Threshold for 'application type' and 'classification' were increased resulting in fewer bins.
    * Loss: 0.5648394227027893 
    * Accuracy: 0.725364446640014
             
* Optimization Attempt 2:
  * Increased layers 1 and 2 neurons to 100 and 20 and added a third hidden layer with 20 neurons
    * Loss: 0.5721397995948792
    * Accuracy: 0.7255976796150208

* Optimization Attempt 3:
  * Changed in layers 1 and 2 'relu' to 'sigmoid'; increased neurons to 120, 80, 40  (Note: tested reducing epochs to 50 but returned to 100 in the final model)
    * Loss: 0.5660290718078613
    * Accuracy: 0.7257142663002014



## Summary
Unfortunately none of the three optimization attempts achieved greater accuracy than in the initial model.  
Alternate options include changing the optimizer within this model. Additionally, other supervised learning models like decision trees, logistic regression, random forest, support vector (i.e. a classification model) could be deployed. 

References
https://www.analyticsvidhya.com/blog/2021/10/a-comprehensive-guide-on-deep-learning-optimizers/
