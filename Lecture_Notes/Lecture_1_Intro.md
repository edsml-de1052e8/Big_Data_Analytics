# Lecture 1: Introduction to Big Data

6 Vs of Big data:

- Volume: 90% of data created in the last 2 years
- Velcity
- Veracity; big data doesn't always mean good data, sometimes the problem occurs with noise
- Visualisation
- Value
- ..

Type of Data Analysis
- Descriptive analysis: what happened?
- Diagnostic analysis: Why did it happen?
- Predictive analytics: What is likely to happen in the future
- Prescriptive analytics: What is the best course of action to take? -> decision-making


The prediction of the system is affected by errors:
- simplification of the model
- Discretization of the model

These lead to
- Implementation by finite precision computations
- Model approximation error
- Round off error
- Discretisation error

Error can be broken down in 2 terms:
- Absolute error= approx value - true value
- relative error: (absolute error/ true value)-1 

Error on the solution sigma= mu * c * sig (??)

But there is an issue with the true value, most of the time we don't have it we can only approximate it!

Some effects of the errors

S always has the same dimensionality as A. The shape is preserved by S
Need to do singular decomposition of a matrix.


How to deal with these errors:

**Truncated SVD**

look at values on the diagonal, conditionalise the data, truncate the matrix to a smaller number in order to have a condition number that is 'better'.

Some effects of the errors: all methods based on SVD 
- Principal Component Analysis (PCA)
- Karnuhen-Loeve (KLT)
- Hotelling Transform 
- ...


**Digital Twins**

- Data Driven Models: Surrogate Models -Physics Informed ML
- Uncertainty Quantification and Minimization
- Explainable AI

**Managing Data for AI**
- BUilding data driven models becomes difficult in many real world scenarios due to dimensionality constraints, matrices become so large that they are difficult to work with 


**Some Approaches**
Accuracy is linked to the error, efficiency is linked to time.
Difference between offline and online
- Offline R&D: cleaning and training
- Online Production: adjusting  and running

Optimal sensor placement: maximisig the quality of data collected by sensors, estimating where to best place them.
Parameter Estimation:






