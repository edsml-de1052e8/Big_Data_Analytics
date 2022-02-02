# Lecture 1: Introduction to Big Data

6 Vs of Big data:

- Volume: 90% of data created in the last 2 years
- Velocity
- Veracity; big data doesn't always mean good data, sometimes the problem occurs with noise
- Visualisation
- Value
- Variability

Type of Data Analysis
- Descriptive analysis: what happened?
- Diagnostic analysis: Why did it happen?
- Predictive analytics: What is likely to happen in the future
- Prescriptive analytics: What is the best course of action to take? -> decision-making


Input data (initial conditions) -> M(P) L(u(t)) = f -> Solution forecast




The prediction of the system is affected by errors:
- Simplification of the model
- Discretization of the model

**Error**

Error on the solution: sigma = mu * c * delta

Any perturbation in the data delta propagates on the solution sigma by an amplification factor given by c = parameter that depends on the algorithm and mu = condition number of the problem.

These lead to: 
- Implementation by finite precision computations
- Model approximation error
- Round off error
- Discretisation error

Error can be broken down in 2 terms:
- Absolute error= approx value - true value
- relative error: (absolute error/ true value) -1 


But there is an issue with the true value, most of the time we don't have it we can only approximate it!

**Singular Value Decomposition (SVD)**

- A = U S V (transpose)
- U: orthogonal
- S: diagonal
- V: orthogonal 

NB: orthogonal matrix :  is a real square matrix whose columns and rows are orthonormal vectors. If its inverse is equal to its transpose.

- Eigenvalue-eigenvector factorization : A = USV(transpose)

**Some effects of the errors**

S always has the same dimensionality as A. The shape is preserved by S
Need to do singular decomposition of a matrix.


How to deal with these errors:

**Truncated SVD**

look at values on the diagonal, conditionalise the data, truncate the matrix to a smaller number in order to have a condition number that is 'better'.

Rank-k approximation to A: k < rA or k = rA 
Ak = Uk Sk Vk (transpose) 

**Elements of the diagonal matrix S are ordered** 

s1 > s2 > Sn > Sn+1 = Sk=0 


Some effects of the errors: all methods based on SVD 
- Principal Component Analysis (PCA)
- Karnuhen-Loeve (KLT)
- Hotelling Transform in MQC
- Proper Orthogonal Decomposition (POD) in MechEng
- Singualar Value Decomposition (SVD)
- Empirical Orthogonal Functions (EOF) in MetScience


**Digital Twins**

- Digital Twin: digital representation of a physical object, process or service
- Data Driven Models: Surrogate Models -Physics Informed ML
- Uncertainty Quantification and Minimization
- Explainable AI

Process:
- Learn the dynamic behind the data: Recurrent Neural Network
- Compress the data to develop reduce order models eg. Encoder-Decoder
- Make data-driven forecasting as much stable and reliable as possible eg. Generative Adversarial Networks

**Managing Data for AI**
- BUilding data driven models becomes difficult in many real world scenarios due to dimensionality constraints, matrices become so large that they are difficult to work with 
- Problem of noisy data: uncertainty and noise in the datacreates serious error propagation 
- Low quality data: data do not provide meaningful info over the whole field

Uncertainty quantification and minimization -> Data Science + ML = Data Learning Models

**Some Approaches**
Accuracy is linked to the error, efficiency is linked to time.
Difference between offline and online
- Offline R&D: cleaning and training eg. optimal data selection, parameters estimation (both accuracy) and surrogate models + data driven models (for efficiency)
- Online Production: adjusting  and running eg. data assimilation (accuracy) and data learning + surrogate models (efficiency).

Optimal sensor placement: maximisig the quality of data collected by sensors, estimating where to best place them.
Parameter Estimation:

**Dealing with data gaps**
- Deep assimilation 
- Data learning 

### Twitter API

- Application Programming Interface: allows apps to communicate data between each other eg. in a restaurant the APIs are the equivalent of a waiter
- Allow you to connect to endpoints of the internet
- In Python, you can do this using the request library, a library used for making HTTP requests
- You can specify in the query which fields you would like to be returned in the JSON tweet object
- Information about users, mentions, metrics and metadata can be incldued

- Javascript object notation (JSON): lanaguage used by APIs to transfer information. Open standard file froamt and data interchange format using human-readable text to store and transmit data objects consisting of attribute-value pairs
- JSON can be parsed into an object using the json library in Python


