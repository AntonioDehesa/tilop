# Machine Learning Basics
* Recommended book: Introduction to Statistical Learning by Gareth James
## What is it? 
Method of data analysis that automates analytical model building  
Using algorithms that iteratively learn from data, machine learning allows computers to find hidden insights without being explicitly programmed where to look

## What is it used for? 
* Fraud detection
* Web search results
* Real-time ads
* Credit scoring
* Prediction of equipment failure
* Network intrusion detection
* Recommendation Engines
* Customer Segmentation
* Text Sentiment Analysis
* Pattern and image recognition
* Financial modeling (planning to do a project related to this later on. Trading bot)

## This course type
Supervised learning algorithms are trained using labeled examples, such as an input where the desired output is known.  
Such classification could be dogs and cats. 

## Steps for Machine Learning
### Get Your Data
Get the raw data you will need for your algorithm, such as the measurements from sensors, images from a camera, etc. 

### Clean your data
Now, you have to clean it and format it. This means that, in the case of images, all images must be the same size, the same format, they must have the same angle (i guess this can change depending on the type of project). 
A tool that can help you with this could be keras
### Divide it in two sets
#### Model Training and Building

With this data, we can train and build our model

#### Test Data

With this data, we can test if the model has been trained correctly, or if the results are correct. 
If neccessary, we can go back to training. 

#### Model deployment
After the tests have been concluded succesfully, we can actually deploy our model. 


## Classification metrics

The key classification metrics: 
* Accuracy
* Recall
* Precision
* F1-Score

Typically, in any classification task, your model can only achieve two results: 
* Either it was correct
* Or incorrect 

This would be a binary classification (two classes)

In the Python course for CV, the example will be about trying to predict if an image is a dog or a cat. 
1. Fit/train a model on training data
2. Test the model on testing data


Important to note, not all incorrect or correct matches hold equal value. 

### Accuracy 
Number of correct predictions made by the model divided by the total number of predictions
For example, if there were 80 correct predictions out of 100 predictions, then there is an accuracy of 80%  
Accuracy is not a good choice with unbalanced classes. Why? in the case of having 99 images of dogs, and 1 of cats, then if the model incorrectly outputs 'Dog' with every image, it would still have an accuracy of 99%

### Recall
ability of a model to find all the relevant cases within a dataset.  
The precise definition of recall is the number of true positives divided by the number of true positives plus the number of false negatives.

### Precision

Ability of a classification model to identify only the relevant data points. 
Precision is defined as the number of true positives divided by the number of true positivies plus the number of false positives. 

### Recall and precision
Often you have a trade-off between Recall and Precision
While recall expresses the ability to find all relevant instances in a dataset, precision expresses the proportion of the data points our model says was relevant actually were relevant. 

### F1-Score
In cases where we want to find an optimal blend of precision and recall we can combine the two metrics using what is called the F1-Score
* Harmonic mean of precision and recall taking both metrics into account in the following equation:  
F1 = 2*(precision*recall)/(precision + recall)

* We use the harmonic mean instead of a simple average because it punishes extreme values
* A classifier with a precision of 1.0 and a recall of 0 hasa simple average of 0.5, but an F1 score of 0
