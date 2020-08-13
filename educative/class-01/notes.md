# Comparing Algorithms

## 1. Intro to Complexity Measures
How do we know which algorithm is better when we compare two algorithms that accomlish
the same goal?

### Important Criteria: Time and Space
- One important aspect that determines the "goodness" of an algorithm is the amount of time
it takes to solve a given problem. Faster is better.

Another aspect to consider is the amount of memory required to solve an algorithm. Less
memory used is better.

The goals of an algorithm are:
- always correct
- always terminates

### How Do We Compare Execution Time?
One can always compare to algorithms by running them on a computer while measuring the execution
time and the algorithm that finishes first will win. However, there are many issues with this
approach:
- input size can have a large impact on execution time therefore both algorithms must be tested
using the same input size
- the input given to both algorithms needs to be the same in order to prevent any disadvantages due
to specific input
- the algorithms must be tested on the same exact hardware otherwise faster hardware will have a
an advantage over a better algorithm running on slower hardware.

### Analytical Evaluation
Since comparing algorithms has various factores that make it almost impossible to evaluate, we
are forced to do an analytical / theoretical comparison.

However, two key points remain:
- we must compare algorithms for the same input size
- we must consider all possible inputs of the given size


## 2. Intro to Asymptotic Analysis and Big O


