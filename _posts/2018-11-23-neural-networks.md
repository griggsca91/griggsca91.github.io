# Neuron

* Neuron pre-activation - (pre-activation)

`a(x) = b = sum(w*x) = b + w^T * x`

* Neuron (output) activation

`h(x) = g(a(x)) = g(b + sum(wi*x))`

w = a vector of connection weights
    
* this will determine how much affect a neuron (xi) that's connected to this neuron will have

b = neuron bias

* A larger bias will allow for more inputs to produce a 1 output from the neuron

g(*) is the activation function

## CREATE A PHOTO TO SHOW HOW THE NEURON WORKS

### Activation Functions

#### Linear Activation Function

* Just displays whatever is calculated by the pre-activation function
* There are no upper or lower bounds

`g(a) = a`

## CREATE GRAPH

#### Sigmoid activation function

`g(a) = sigm(a) = 1/(1+ exp(-a))`

* Always positive
* will create an upper bound of 1 and a lower bound of 0
* Only will ever increase for larger inputs


#### Hyperbolic Tangent Activation function

`g(a) = tanh(a) = (exp(a) - exp(-a)) / (exp(a) + exp(-a)) = (exp(2a) - 1)/(exp(2a) + 1) `

* Has an upper bound of 1 and a lower bound of -1
* Only will ever increase for larger inputs


#### Rectified linear activation function

`g(a) = reclin(a) = max(0, a)`

* Always postive
* No upper bound, has a lower bound of 0
* Only will ever increase for larger inputs
* Will output the activation result if it only outputs something higher than 0
* can produce sparse neurons (vectors with 0 values) since it's much easier to produce a 0 result   


## Single Neuron

### Perform a binary classification

* Binary classification is the output of 1 of 2 options `y = {0, 1}`
* logistic regression classifier
    * If `h(x) > .5` predict class 1
    * Else predict class 0
* Sigmoid and Tangent activation functions are good for this
* Not able to handle complex inputs; cannot solve linearly seperable problems (needs a line to go through a graph of inputs)

## Multilayer Neural Network

