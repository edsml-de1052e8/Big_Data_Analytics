# Lecture 3: PCA


To measure how error propagates: SVD


### PCA
- can reduce error
- allows for dimension reduction -> when data is too big to manage
- Definition: PCA simplifies the complexity of the data while retaining the trends and patterns

- You have your matrix -> do SVD -> then you see you get the following:
- The first principal component in the direction of greatest variabiity (covariance)
- second is the next ortogonal direction of great variability
- So the last eigen value with reduced covariance is not always representative of the variability of the data

STEPS:
- standardise data
- Calculate ...

PCA mean : sum of vectors/ number of vectors
Uses the following indices: mean, matrix data, covariance and variance

reminder: Transpose eg. 
{ 1 2
3 4}

{ 1 3
2 4}


**Dimension Reduction**

The parameter k is the largest values in a matrix S.
The parameter k has to be large enough to allow fitting the data but also small enough to filter out non relevant representational detail.


NB: When you cut the data, be careful to keep value of k for good accuracy but also good performance in terms of running time.

