# Lecture 12: Parallel Computing


- For example when calculating a sum: can split each iteration into chunks where one computer does each chunk and you add them together at the end.
Three strategies:
- 1:  all the partial sum information sent to one processor and just that one processor sums it. -> Number of steps = 3
- 2: split the partial sum info into two processors and then information is sent to one processor. -> Number of steps =2.
- 3: each processor processes the partial sum on their own (expensive, not energy efficient). -> Number of steps is 2.

- Synchronisation of the access: when one processor is working on smthg else eg. tabs open, then it may be slower than other processors so need to be aware of which one works on which.
- 




