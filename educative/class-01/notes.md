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

### Types of  Analysis
**Worst Case Analysis**
- maximum time of algorithm over all inputs of size **n**
- provides an upper bound on running time
- an absolute guarantee that the algorithm would not run longer no matter what the inputs are

**Average Case Analysis**
- expected time of algorithm over all input of size **n** (sometimes used)

**Best Case Analysis**
- not reliable, of limited value, never used!

The running time of an algorithm is also known as its ***time complexity***. The ***space complexity*** of
an algorithm is the amount of additional memory space that the algorithm requires.


## 2. Intro to Asymptotic Analysis and Big O
Asymptotic analysis is a way to classify the running time complexity of algorithms. We have
seen that the time complexity of an algorithm can be expressed as a polynomial.

### Asymptotic Analysis
We can observe that we only want to worry about large input sizes only (how bad can a poorly
designed algorithm get?) Mathematicians have a tool for this sort of analysis called ***asymptotic
notation***. Asymptotic notation compares two functions, say **f(n)** and **g(n)** for very large values
of **n**.
- we are comparing functions in the limit (asymptotically)
- we are comparing functions where n -> infinity (what happens as **n** goes to infinity)
- lim -> ∞ f(n)

Constant factors:
- constants can be ignored for large **n** i.e. n + 5 = n
- coeficients can be ignored for large **n** i.e. 2n = 2

### Asymptotic Notation
There are three main ways to classify the bounds of an algorithm:
- Big Oh O Notation
- Big Omega Ω Notation
- Big Theta Θ Notation

### Big O Notation
- asymptotic "less than"
- upper bound
- f(n) = O(g(n)) implies: f(n) ≤ g(n)

### Big Omega Notation
- asymptotic "greater than"
- lower bound
- f(n) = Ω(g(n)) implies: f(n) ≥ g(n)

### Big Theta Notation
- asymptotic "equality"
- tightly bound i.e. "ideal" bound (growing at the same rate)
- f(n) = Θ(g(n)) implies: f(n) = g(n)

### Big O Notation Definition
O(g(n)) = { f(n): there exist

###
