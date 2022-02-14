# Lecture 11: Generators



Generator: not storing anything in memory, just creating the way to do it ('recipe')
Can't compute the length, or index as it just creates the formula, there is 'nothing' in it

Using ```next``` you can compute the first element of the generstor, and every time you type this it calls the next one (kinda like a for loop)

The use of generator is better than for loops especially with big data. 
Within a for-loop, instead of using ```return``` you can use ```yield``` instead to prevent stopping at every iteration and adding to it, this continues the process and creates a generator as well.
NB: you cant reuse the generator, cna only be used once.



