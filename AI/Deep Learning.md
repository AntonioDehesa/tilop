# Python for CV Course by Jose Portilla
## Topics and Goals
* Keras Basics
* MNIST Data Overview
* Convolutional Neural Network Theory
* Keras CNN
* Deep Learning on Custom Image Files
* Understanding YOLO v3
* YOLO v3 With Python


## What is a neuron? 

Aritificial Neural Networks (ANN) have a basis in biology  
An artificial neuron is called a perceptron  


An artificial neuron (perceptron) has inputs and outputs. 
The basic model has two inputs and one output. 
The inputs will represent the values of features. 
Then, these values are multiplied by some weight. These weights are usually different for each input, but they can be the same, given the right circumstances.  
These weights begin as random values, and then these numbers change to improve the output. 
The results of these operations is then passed on to an activation function. There can be a lot of activation functions, but the most basic one would be binary.  
Now, these has a problem: in the case the input values are zero, the result will always be zero, regardless of the weights. That is why we use a bias, like a plus one, to avoid a zero case. 


## How do neural networks work? 
A neural network is a network of various layers of single perceptrons working together. 
A simple example would be:
Input layer -> 2 hidden layers -> output layer
The hidden layers are the ones inbetween the input and the output. 
So, recap... 
* Input layers: they take the real values from the provided data
* Hidden layers: they are between the input and output. 3 or more layers is a "deep network"
* Output layer: the finale estimate of the real output

## Activation functions 
The most basic example would be a binary function, which will output a 0 if certain condition is not met, and a value of 1 if the condition is met. 

The function would be: 
Z = w*x + b
where Z is the output, w the weights, x are the inputs and b is the bias. 

A little more advanced function would be the sigmoid function. 
Z = 1/(1+e^(-x))

This would give us a more smooth output. 

There are other activation functions, such as: 
* Tanh(z): The "same" as the sigmoid function, but the sigmoid goes from 0 to 1, and this one goes from -1 to 1
* Rectified Linear Unit: we simply input the output of the real function, into max(0,z). 