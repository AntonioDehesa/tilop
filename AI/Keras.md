# Keras 
Python Deep Learning API. Open Source Neural Network Library written in Python. It runs on TensorFlow, Microsoft Cognitive Toolkit, or Theano. Specifically designed for quick experimentation with Deep Learning. 

## Practice case: Bank notes forgery

Some of these bank notes were forgeries.
The researches created a dataset from these bank notes, by taking 400x400 images and extracting numerical features from the wavelets of the images.  
The data is not an image, directly. 
This exercise is just to learn how to use Keras for general machine learning.  
Once we learn about Convolutional Neural Networks, we can expand on Keras to feed in image data into a network. 

## sklenar: Scaler object

This is from the Python for CV repo, the Keras Basics file. 
In line 15, we use the scaler object. The reason why we fit only to the training set, and not the whole set, is because training for the entire set would be assuming things for the testing set, which we can not do, as we can not assume in real life. This woul be "cheating", and it is called Data Leakage. 

## sklearn: model selection

This will help to divide the entire set intro a training and testing set. 

## Keras: layers - Dense
Regular deeply connected neural network layer. 

## Keras: models - Sequential
Groups a linear stack ot layers into a keras.model. 
First, we add the inputs, then the neurons, the hidden layer, and finally, the output. 
Then we compile, and train. 

### Sources 
Python for Computer Vision with OpenCV and Deep Learning, by Jose Portilla