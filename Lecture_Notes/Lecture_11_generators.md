# Lecture 11: Generators & MultiProcessing



Generator: not storing anything in memory, just creating the way to do it ('recipe')
Can't compute the length, or index as it just creates the formula, there is 'nothing' in it

Using ```next``` you can compute the first element of the generstor, and every time you type this it calls the next one (kinda like a for loop)

The use of generator is better than for loops especially with big data. 
Within a for-loop, instead of using ```return``` you can use ```yield``` instead to prevent stopping at every iteration and adding to it, this continues the process and creates a generator as well.
NB: you cant reuse the generator, cna only be used once.

This is called 'lazy single use iterables'

- The reason why you dont get outputs directly when typing a lot of functions in Python is bc it forces memory efficiency -> mostly thru generators


### Multiprocessing

- Concurrency: two ormore calculations happen within the same time frame 
- Parallelism: two or more calculations happend at the same moment. Special case of concurrency

```Pool``` is really useful as it puts in each argument a process 1, 2 and 3 respectively for example. -> don't need join and start function 








