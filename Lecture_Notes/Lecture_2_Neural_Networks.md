# Lecture 2: Neural Networks


**Neuron Model**
Neuron model: multiply all inputs eg. x1, x2 by weights w1 and w2 respectively, add bias w0 to the sum to obtain pre activation z and then the activation function (think about activation function as a sigmoid function).

**Simplififed Neuron**
- simply function by adding extra input w0 and adding 1 at the start (?). 

- Single layer: n neurons that all take the same m inputs. They can see all the inputs.

- for a single neuron you have a vector of weights
- for a single layer, you have a matrix of ms (??)

We can write this as z= W pow(T) * x
- apply the activation function f(z) element by element in z to obtain activation a
- Note that activation is applied element by element -> a 
- output activation a: element by element -> f(W (powT) * x)
- w10,w11, w12 in each column for example, so that gives n+1 rows and n columns
- The dimensions of the vector have to be the same as the matrix to be able to multiply vector by matrix so instead need to transpose it. Hence we get -> f(W transpose x)

**Multiple Layers**

- Still have m inputs, all neurons in the first nlayer can see inputs, then all neurons per single layer go in one weight matrix w in layer one.
- Forward propagation : the input for one layer is going to be the input for the next layer, cascading
- Hidden layer: combines the features to the way it thinks it should to predict the output 

W(1)T * x -> fist layer output 
This then goes in to the second layer 

**Activation Function**

- To ensure non-linearity...

**Rectified LU**

- ...

Sigmoid logistic function: derivative always positive, output in [0,1] range so can be interpreted as probability.
Hyperbolic tangent: between [-1,1] 
Softmax function: modified to be in range between [0,1]

Output layer and its activation function
- For single class classification and regression problems we need one neuron in the output layer
- In multi-class classification we need 

**Gradient descent**

- Iterative method to find a minimum of a differentiable function (optimisation)
- Starting from point x0 how can we iteratively approach the minimum of f(x).
- Algorithm: initialise x-i-1 = x0
- We compute the derivative f'(x) and move xi = xi-1 - hf'(xi-1)

First step:
- calculate derivative
- Find the starting point
- Find the step size
- Find the gradient
- And calculate function until a set number of iterations
NB: make sure you reach the minimum when you put the number of iterations, jus try and change the number of iterations and test it until you reach the point
- You can also change the time step to find the minimum faster, but you run the risk of getting the wrong minimum  and jumping to another part of the function
- Another issue that can arise is that you can get different minimums depending on where you start especially if it is a function with multiple troughs.

-> Exercise 1: can assume it has 2 input variables


### Back Propagation


- This usually happens in the background in Tensorflow
- gradient descent needs to minimise loss function by changing the weights, and modify those weights as you descend.
- This is referred to as h, but also as learning rate for the purpose of ML
- Loss function: takes the ouput of the final layer and the expected output from the training set
- Need to find the gradient of the loss function basically
- the activation function of the final layer is multiplied by the ouput of the previous layer (?)
- Chain rule: preactivation of z dependent on L of previosu layer (??)
- a is f(z)

- To need to pick a random point from our training method, to make the technique less computationally heavy  -> stochastic gradient descent
- loss: comparison between output from training set to the output 
- Repeat process until neural network is trained -> when it reaches the minimum

**Initialisation**
Before doing the gradient, need to initialise the weights: first randomly ( so as not to introduce symmetry) and also need to have values to be near zero 

### Tensorflow

- Free and open source, focuses on neural network and developed by Google Brain Team for internal Google use
- ```pip install tensorflow```
- Extra tip for Python: use ```pathlib``` library to avoid hardcoding file paths
- NB: to make sure that all values in the table are floating point values -> conver to flat using ```as.type(float32)```

Application:
- Can also encode the string (eg. g =1, b =0) using scikit learn's ```LabelEncoder```
- Fit it
- Then put that as train/test split eg. 0.3
- When you put the input in layer one eg. 10, Tensorflow will assume that that is the case in the second layer (so no need to put it)

Optimiser: eg. SGD, but also can look for others on tensorflow docs
Loss: in a binary classification proble use ...









