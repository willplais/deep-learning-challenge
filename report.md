# Using Nonprofit Foundation Data to Predict Successful Funding

## Overview

This data analysis uses nonprofit foundation data of funding grants to try and predict wether future funding will lead to successful projects. It utilizes this data through a neural network model trained on the past data available. I am aiming for a model accuracy of 75%.

The target I am training on is whether the funding was successful as this is what we want to predict. The features I are training on are the following:

* Application Type
* Affiliation
* Classification
* Use Case
* Organization
* Income Amount
* Special Considerations
* Asking Amount

There were two additional variables we excluded from the data as they were not relevant to our analysis. These are the EIN number and the applicants name.

Next the data needed to be normalized and cleaned to be able to be trained on. The application type and classification values were to numerous to be useful for this purpose so the fields were condensed to other in the following ways. Application type with less than 500 results were condensed into other; classifications were condensed to other for results with less than 1000.

The scaled data was then seperated into training and testing data; then needed to be scaled to not give any special weight to any particular field. I utilized the StandardScaler function inlcuded in SciKitLearn to scale the data.

A neural network model was then compiled using various layers and activation methods. I utilized relu, tanh, and sigmoid activations while training the model to acheive a final accuracy of around 72%.

## Results

The model was able to come close to our goal accuracy but not quite able to reach 75%. 

* Neural Network Model 1:
    * Accuracy: 0.7292 (72.92%)
    * Successful Precision: 0.7167 (71.67%)
    * Successful Recall: 0.8074

* Neural Network Model 2:
    * Accuracy: 0.73 (73%)
    * Successful Precision: 0.7184 (71.84%)
    * Successful Recall: 0.8056

* Neural Network Model 3:
    * Accuracy: 0.7279 (72.79%)
    * Successful Precision: 0.7115 (71.15%)
    * Successful Recall: 0.8173

## Summary

The neural network model was able to get very close to our goal so as a tool to predict wether a project would be successful could be a good thing to have from the foundations perspective. A decision tree classification model I believe would get you a pretty similar result but with so little data available here a neural network model can get you a better result with practically no resource constraints.
