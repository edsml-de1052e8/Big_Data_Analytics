# Lecture 6: Compression using One Hot Encoders and PCA

**Overfitting in Machine Learning**

- When data is customized for specific data.
- How to know if you are overfitting -> validation
- To prevent overfitting, datasets used to train a predictive model should always be divided at random into
-  **Training** set: Part of the dataset that we use to train the model, learning the coefficients of our logistic regression
-  **Validation** set: Part of the dataset that we use to validate the modell we tried
-  So by doing that we are testing the data with data that the model hasn't seen before, less bias
-  To check if you are overfitting or underfitting, check the accuracy of the *validation*. So if you have a very good validation accuracy around 0.9-1, then it is appropriate, if you have low validation accuracy (eg. 0.30 ish) you are overfitting and if you have a validation accuracy around 0.60-0.8 you might be underfitting

- NB: Validation accuracy goes down when train/test split is unbalanced eg. high training set and small validation set (0.8/0.2)

### Representativty of Training Data 🧏

- If the training data is not representative enough of the problem you are trying to solve, best to add more  representative data to generalise the model better
eg. occurence of cancer for any individual in a population, training a model on samples coming from male population only results in bias 


**Forward Selection**
- Start with a model with no variables then at every step check all the variables and select the one that increases validation accuracy or another metric the most and add it to the model
- Stopping criteria: when there are no more variables to add or when the metric doesn't increase enough eg. validation accuracy does not increase by at least 0.5%

**Backward Selection**
- Start with a model containing all the variables, at every step *remove* all the variables that have the least impact on the model  eg. reduces the validation accuracy the least. Stopping criteria is when there are no more variables to remove or when the metric decreases too much eg. validation accuracy doesn't increase by at least 0.5%
- In these two methods you are still learning at every step

**To prevent overfitting: train-test-validate**
-test set: part of he dataset that we only use at the end of the analysis to evaluate how our final model will perform on new data, the final one we report.


**Supervised learning** : ML approach defined by its use of labelled datasets. These are designed to train or sueprvise algorithms into classifying data or predicting outcomes accurately. Using labeled inputs and outputs the model can measure its accuracy and learn over time.
Can be classification or regression.

**Unsupervised learning**: ML algorithms to analyse and cluster unlabelled data sets. These algorithms discover hidden patterns in data without the need for human intervention. Used for clustering, association and dimensionality reduction.



### Encoder

- Encoding means to convert data into a required format
- Autoencoder: unsupervised artificial neural network designed to learn an identity function in an unsupervised way to reconstruct the original input while compressing the data in the process so as to discover a more efficient and compressed representation.
- Autoencoders attempt to replicate its input as closely as the output. Learns a reduced representation called latent space. It is non linear representation.

Characteristics:
- Data specific
- Unsupervised
- Not loss-less

- Encoder network: it translates original high dimension input into latent low-dimensional code. input size is larger than output size
- Decoder network: recovers data from the code, likely with larger and larger output layers

- so with autoencoder you are working on the delta part of the errors, the perturbation of the data/ noise.
- 





**Example: Using Covid Dataset**

- SEIRS Model: Susceptible Exposed Infectious and Removed Model. 
In a 10 x 10 grid with each square representing a population . Each population is either mobile or static in their movement.
This gives us 100 variables for each time step. Need to compress this bc high data points.

### Data Compression with PCA:

Steps:

- get a training dataset from values
- Reshape data into 1D, 2D or 3D 
- Normalize it using standard scaler 
- PCA, first using all 800 variables
- can change number of explained variance here, 99.9% variance with 15 principal components
- Check results with MSE eg. 0.30
- Save data with ```joblib``` library and savetxt 

### Compression with Encoding:

- Early stopping: to stop the training set once it reaches your set 'good point'
- Encoder: with linear activation, and set input eg. 800.
 OR
 
 - *Non linear hot encoder*: instead of being linear activation change to "elu" activation which includes a middle time step.
 - Can also change the number of epochs, learning rate, number of neurons or components etc.
 - Calculate MSE eg. 0.10

- *Convulational Hot Encoder*: activation changed to "elu" as well, and using ```keras.layers.Conv2D(64, kernel_size =3, passing = "SAME", activation = "elu"),```

For non linear problems Encoding gets you better results than PCA compression.

Can here you use a grid search to automatically figure the optimal hyperparameters for this 



