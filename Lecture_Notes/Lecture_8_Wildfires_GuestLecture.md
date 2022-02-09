# Lecture 8: Guest Lectures Wildfires


Use of PCA for dynamical systems with SVD.

Training model in the latent space, using autoencoding. 

Sometimes more efficient to have neurons less than latent space to increase efficiency (?)

Wildfire data is integers so can normalise betwee 0 and 1. 
When doing upsampling, use the same parameter as in the encoder.
Sometimes that doesn't correspond so can do a cropping method when you have too many parameters/ when they dont correpsond

**Unstructured Data**

Pixels are square so have specific dimesions, easy to train NN on.
But what about unstructured data? How do we use autoencoders on that unstructured data?


## Summary of Pros and Cons

**PCA**

Cons
- Linear data only, so only good results on linear (not on non-linear ones)
- Reconstructs PCs


**SVD AE**

Cons
- Has more steps so more expensive to compute, and takes longer time

Can generate unsee data in latent space to generate some noise to test our data against. Putting it in the latent space allows this to be less expensive.



## Data Assimilation

-when covariance matrix is large, there are a high number of uncertainties
- BLUE using background info xb and real time observation y 
- 3DVAR observations using single time step while 4DVAR uses multiple time steps.

- When you don't know covariance matrix, can do iterative method until you find it.
- Latent assimiltion: data assimilation in the latent space
- Do some preprocessing so as to be in the same latent space then do the encoding/PCA in the latent space, then decompress using decoder/PCA etc


Assessment: will be reduced ordering and latent assimilation.






