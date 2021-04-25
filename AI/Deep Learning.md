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


## MNIST Data

A classic data set in Deep Learning. Keras already includes 60000 training images, and 10000 test images. 
It contains handwritten single digits from 0-9. 
These images have values that represent a 28x28 array, and its values represent the grayscale image. 

We can think of the entire group of the 60000 images as a 4 dimensional array.
one dimension is the 60,000 images, another is the color dimension, which is 1 channel. and the other 2 dimensions are the x and y of the images. (60000,28,28,1). 

The labels use one-hot encoding. 

## Convolutional Neural Networks

Just like the simple perceptron, CNNs also have their origins in biological research.  
Biological vision works by "segmenting" the image the eyes are seeing. It first segments the image, and each section is managed by specific neurons. Then, they can be overlapped, and the information analyzed. 
This idea inspired an Artificial Neural Network architecture, which would become a CNN. 

### Tensors

N-Dimensional arrays that we build up to: 
* Scalar - 3
* Vector - [3,4,5]
* Matrix - [ [3,4],[5,6],[7,8] ]
* Tensor - [ [ [1,2], [3,4] ]],  
           [ [5,6],[7,8]]]

Basically, arrays of matrixes, or arrays of arrays of arrays of arrays.  
They are used, because they are convinient to feed in sets of images into our model - (I,H,W,C)
* I: Images 
* H: Height of Image in Pixels 
* W: Width of Image in Pixels 
* C: Color Channels: 1-Grayscale, 3-RGB

### DNN vs CNN

#### Densely-Connected Neural Network
Densely connected layer. It looks like every neuron in one layer is directly connected to every other neuron in the next layer. 

#### CNN
Each unit is connected to a smaller number of nearby units in the next layer. Meaning, not every neuron in one layer is directly connected to every neuron in the next layer. 


Why dont we just use DNN then? 
Simple. With images of 256x256 pixels, we would have 56k total connections. Too many parameters, and the bigger the images, the more parameters and connections.  
* Convolution helps, by segmenting the image, and allowing the neurons to support each other in each section.  
* Each CNN layer looks at an increasingly larger part of the image. 
* Having units only connected to nearby units also aids in invariance.
* CNN also helps with regularization, limiting the search of weights to the size of the convolution. 

The edge cases are "fixed" with the use of padding. 


### Convolutions and Filters

The filters are a moving window (the convolution) of nxn, which takes every element inside the window, and performs an operation, giving one output. 

### Pooling Layers 

They will subsample the input image, which reduces the memory use and computer load, as well as reducing the number of parameters. 

For example, we could use a kernel of 2x2, and move it accross the input image. Then, we evaluate what is inside the kernel, and pass only the max value to the next evaluation.  
This pooling removes a lot of information. a 2x2 with a stride of 2 will remove 75% of the input data. 

### Review Dropout

Form of regularization to help prevent overfitting. During training, units are randomly dropped, along with their connections.  This helps prevent units from co-adapting too much. 


## YOLO 

You Only Look Once. 
Helps by detecting and classifying images, as well as creating bounding boxes. 

Why YOLO?  
 
Prior detection systems repurpose classifiers or localizers to perform detection. 

They apply the model to an image at multiple locations and scales. High scoring regions of the image are considered detections.  

YOLO applys a single neural network to the full image, so it only looks at the image once. This network divides the image into regions and predicts bounding boxes and probabilities for each region. These bounding boxes are weighted by the predicted probabilities. So, one advantage of YOLO would be that it looks at the whole image at test time, so its predictions are informed by global context in the image.  

It also makes predictions with a single network evaluation, unlike systems like R-CNN, which require thousands for a single image. This makes it extremely fast, more than 1000 times faster than R-CNN and 100 times faster than Fast R-CNN. 

## Source
Python for computer Vision with OpenCV and Deep Learning, by Jose Portilla