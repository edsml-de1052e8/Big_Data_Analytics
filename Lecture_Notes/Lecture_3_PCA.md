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

After PCA: this means that the new variables are uncorellated with one another and are linear combinations of one another.
So the output is strictly linear -> issue when you don't want this on the application side or when the solution seeked is complex (not linear).

NB: standardising step = computing the mean, variance, std, covariance etc

### Assignement Info 

- Air pollution indoor: Projection and then interpolation 
- Make sure you have a slice of what is happening at a specific height eg. 1.5m in the dataset
- So cutting the room at that level for 2 D space instead of 3D at different times

- Second dataset is RGB and is a picture of what is happening at this slice
- Submit the error and the time





