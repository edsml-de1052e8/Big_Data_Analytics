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
- 
