# Lecture 12: Parallel Computing


- For example when calculating a sum: can split each iteration into chunks where one computer does each chunk and you add them together at the end.

**Three strategies:**

- 1:  all the partial sum information sent to one processor and just that one processor sums it. -> Number of steps = 3
- 2: split the partial sum info into two processors and then information is sent to one processor. -> Number of steps =2.
- 3: each processor processes the partial sum on their own (expensive, not energy efficient). -> Number of steps is 2.

- Synchronisation of the access: when one processor is working on smthg else eg. tabs open, then it may be slower than other processors so need to be aware of which one works on which.

**Measures of computational power & decision-making**

To choose the tradeback between number of processors and number of calculations (T(p)), can do T(1)/T(p), the **speed up**.
Ratio between runtime of algorithm on one processor and runtime of algorithm on all processors.
- Overhead: measure how much the speed up differs.
- Efficiency: ratio between speed-up and number of processors -> need a bigger value of the ratio
Ideally the closer to 1 it is the better.


DD-DA Framework: split 3D data in a cube and taking in observations. Overlap at border cases are accounted for and compensated for using a correction number.
Example: Caspian Sea: North/South divide according to expert knowlegde, so decomposing in horizontal slices for different processors. Note that this doesn't balance the data.
Can akso do a decomposition along time variable: 


### Zainab Titus PhD: well data assimilation over time

- Goal based sensitivity: calculated delta m to be very small -> H delta(m) = -g
- H is the hessian second order sensitivity 
- Do iterations of this to improve the model
- Model keeps showing different temperature over time while observations show constant temperature (? why  is that?)
- When doing covariance matrix giving priority to senor data. Saying that sensor data is 'near perfect'.


permeability depends on local geology, did you have a specific location in mind when conduction this? or specific application?

- By optimising the input can take any world data and compare iteratively to find the data, no need for optimising the weigths -> done by working on the inverse modelling



Assessment: 4 questions 4 separate notebooks


- Both background and satellite/observation data have the same timesteps. So use the same timesteps for DA (has been simplified for you, dont need to choose timesteps)
- assimilate model data with model data and obs with obvs
- Can use any autoencoder eg. convulational etc
- question 3: same thing as the competition
- show that you understand how to select good parameters its ok if you dont get THE best
