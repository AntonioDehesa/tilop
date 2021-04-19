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


## Cost Function

In this case, we will use: 
* y to represent the true value
* a ti represent the neuron´s prediction

In terms of weights and bias:
* w*x + b = z
* Pass z into activation function f(z) = a

### Quadratic cost

C = Sum(y-a)^2 / n
* we can see that larger errors are more prominent due to the squaring
* unfortunately this calculation can cause a slowdown in our learning speed

### Cross Entropy 
C = (-1/n)sum(y*ln(a)+(1-y)*ln(1-a))
* This cost function allows for a faster learning
* The larger the difference between y and a, the faster the neuron can learn

# 
We now have 2 key aspects of learning with neural networks: 
* the neurons with their activation function
* the cost function

But, the learning is still missing. 


# Gradien Descent and Back Propagation

## Gradient Descent
Gradient descent is an optimization algorith for finding the minimum of a function. 
To find a local minimum, we take steps proportional to the negative gradient. 


Cost in y axis, and weight in x axis.
By finding this minimum, we can minimize the cost.  
Finding this minimum is simple for 1 dimension, but our cases will have many more parameters, meaning we´ll need to use the built-in linear algebra that our Deep Learning library will provide.  
By using gradient descent, we can figure out the best parameters for minimizing our cost. For example, finding the best values for the weigths of the neuron inputs. 

## Back Propagation

Back Progagation will help us to quickly adjust the optimal parameters or weights across our entire network.  
It is used to calculate the error contribution of each neuron after a batch of data is processed.  
It relies heavily on the chain rule (calculus) to go back through the network and calculate these errors. 

It calculates the error at the output and then distributes back through the network layers. (It reminds me to control theory). 
It requires a known desired output for each input value (supervised learning). 

## Source
Python for computer Vision with OpenCV and Deep Learning, by Jose Portilla