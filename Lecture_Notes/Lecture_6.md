# Lecture 6: Compression using One Hot Encoders and PCA


**Example: Using Covid Dataset**

- SEIRS Model: Susceptible Exposed Infectious and Removed Model. 
In a 10 x 10 grid with each square representing a population . Each population is either mobile or static in their movement.
This gives us 100 variables for each time step. Need to compress this bc high data points.

Steps:

- get a training dataset from values
- Reshape data into 1D, 2D or 3D 
- Normalize it using standard scaler 
- PCA, first using all 800 variables
- can change number of explained variance here, 99.9% variance with 15 principal components
- Check results with MSE eg. 0.30
- Save data with ```joblib``` library and savetxt 

**Encoding**

- Early stopping: to stop the training set once it reaches your set 'good point'
- Encoder: with linear activation, and set input eg. 800.
 OR
 
 - *Non linear hot encoder*: instead of being linear activation change to "elu" activation which includes a middle time step.
 - Can also change the number of epochs
 - Calculate MSE eg. 0.10

- *Convulational Hot Encoder*: activation changed to "elu" as well, and using ```keras.layers.Conv2D(64, kernel_size =3, passing = "SAME", activation = "elu"),```
- 
