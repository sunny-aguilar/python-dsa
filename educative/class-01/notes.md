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
- computer languages are implemented differently

### Analytical Evaluation
Since comparing algorithms has various factores that make it almost impossible to evaluate, we
are forced to do an analytical / theoretical comparison.

However, two key points remain:
- we must compare algorithms for the same input size
- we must consider all possible inputs of the given size

We assume a hypothetical computer on which some primitive operations are executed. We consider
a specific input size **n**. We then count the number of operations executed by an algorithm for a
given input. The algorithm that results in fewer primitive operations is considered better.

A ***primitive operation*** can be considered simple operations that are typically implemented
as processor instructions. This includes assignment, reading from a variable, comparing two values,
arithmetic operations, and calling a function.

### Asymptotic Analysis
**Worst Case Analysis**
- maximum time of algorithm over all inputs of size **n**

**Average Case Analysis**
- expected time of algorithm over all input of size **n** (sometimes used)

**Best Case Analysis**








## 2. Intro to Asymptotic Analysis and Big O


