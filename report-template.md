
# Module 20 - Report Template


## Overview of the Analysis
In this Analysis various techniques were used to instantiate, fit and evaluate a model based on loan risk. 
* The classes to predict were "healthy loan" (0) and "high-risk loan" (1), originally having _{0: 75036, 1: 2500}_ datapoints in the dataset. 
* The stages of the Analysis were: 
  * Creation of labels and features data structures 
  * Data split into training and testing datasets 
  * Creation of model instance and the corresponding fitting 
  * Predictions calculation 
  * Model evaluation 
* In the model creation stage, two methods were used: 
  * Linear model with a Logistic Regression classifier
  * Random over-sampling the minority class, feeding the resulting balanced classes into a Logistic Regression classifier


## Results
Model 1: Logistic Regression, imbalanced datasets
* Balanced accuracy: 0.944 
* Precision: 
  * Label 0: 1.00 
  * Label 1: 0.87 
* Recall: 
  * Label 0: 1.00 
  * Label 1: 0.89 

Model 2: Logistic Regression, previous Random over-sampling
* Accuracy: 1.00 
* Precision: 
  * Label 0: 1.00 
  * Label 1: 0.99 
* Recall: 
  * Label 0: 0.99 
  * Label 1: 1.00 


## Summary
For this Analysis, it was used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can predict the creditworthiness of borrowers. Comparing the results for accuracy, precision and recall above, it can be seen that: 
* With no over-sampling, the performance of the Logistic Regression linear model depends on the problem to solve: the Logistic Regression model had a very good performance with class 0; however for class 1 the performance degraded. 
* After over-sampling, the Logistic Regression model had a very good performance with both class 0 and class 1. 

For this specific example, based on the metrics, the recommended model to use is Logistic Regression fit with Random over-sampled data. 
