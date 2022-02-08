# Lecture 7: Data Assimilation

Data assimilation has different definitions depending on the data eg. atmospheric, mathematical etc
For a computationally intensive problem.

Put together forecasting initial input data and observed data, combine and use it to make a new forecast.

Data assimilation is key to minimise error propagation.

**Bayes Theorem: Bayesian Data assimilation**

Merging the two overlaps in data eg. observations and initial inputs with errors

When dealing with imbalanced data, one way to deal with it is through undersampling or oversampling.
Can use oversampling when big data set is very meaningful and you don't want to lose that specific data.

Both undersampling and oversampling can be in a supervised and unsupervised way although supervised is consequentially not random.

In a error covariance matrix, the non diagonal values are the error correlation between the different points eg. different sensors in a room, so if they are zero, there is no correlation. -> Not realistic in weather forecasting.

Not enough to just have observations, then problem is mathematically ill-posed so why we combine both inputs


**Tikhonov Regularisation**

Local minimum

Uses a Kalman Filter: data assimilation method 

Kalman gain matrix: K= BH (transpose) * (HBH transpose + R)^-1

Uses B, H , R
R: Observation error covariance
H: Obserbation Operator
B: Background error covariance



**Notations and Assumptions** 

Thru data assimilation we aim to obtain an optimal estimation x of the true state which can be a physical field.
