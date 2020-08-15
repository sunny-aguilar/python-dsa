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
<img src="https://cdn.programiz.com/sites/tutorial2program/files/big0.png" width="400px">

### Big Omega Notation
Ω(g(n)) = { f(n): there exist positive constants C and n₀ such that 0 ≤ c⋅g(n) ≤ f(n) for all n ≥ n₀
- g(n) is an asymptotic lower bound for f(n)
- lower bound
- f(n) = Ω(g(n)) implies: f(n) ≥ g(n)
<img src="https://cdn.programiz.com/sites/tutorial2program/files/omega.png" width="400px">

### Big Theta Notation
Θ(g(n)) = { f(n): there exist positive constants C₁ and C₂ and n₀ such that 0 ≤ C₁⋅g(n) ≤ C₂⋅g(n) for all n ≥ n₀
- g(n) is an asymptotically tight bound for f(n)
- this means that when a run time is Θ(g(n)), the run time is at least C₁⋅g(n) and at most C₂⋅g(n)
- tightly bound i.e. "ideal" bound (growing at the same rate)
- f(n) = Θ(g(n)) implies: f(n) = g(n)
<img src="https://cdn.kastatic.org/ka-perseus-images/c14a48f24cae3fd563cb3627ee2a74f56c0bcef6.png" width="400px">

### Big O Notation Definition
O(g(n)) = { f(n): there exist positive constants C and n₀ such that 0 ≤ f(n) ≤ c⋅g(n) for all n ≥ n₀<br />
( { f(n): means "the set of all f(n) such that... )
- g(n) is an asymptotic upper bound for f(n)
- we only care for n beyond n₀
- what good is this? it tells us that for very large values of n, f(n) will be at most within a constant factor C of g(n)
<img src="https://cdn.programiz.com/sites/tutorial2program/files/big0.png" width="400px">

**Relate to Code**
This code snippet shows a simple loop & the cost to run it. We get an equation from this which is the run time.

```
sum = 0                       // C₁ - executes in contant time
for (i = 0; i < n; i++) {      // C₂⋅n - executes in C₂⋅n  time
  sum += array[i]
}
return sum                    // C₃ - executes in contant time
```

Total run time = C₁ + C₂⋅n + C₃

**What is the Big O runtime?**
- for big O, constants don't matter (we drop them)
- C₁, C₂, C₃ are hardware dependent so they don't matter
- O(n)is runtime (linear time) in this case since we only have one n

**Nonlinear Time**
- these are your curved graphs
- i.e., n² or n³

**Orders of Growth**

![Time Complexity](https://assets.digitalocean.com/articles/alligator/js/big-o-notation/o-complexity.png)

### Comparison of Some Common Functions
This table lists some commonly encountered functions in ascending order of rate of growth. Any function can be given as Big O of any other fucntion that appears later in this table.
> Constant O(1)
>
> Logarithmic O(log n)
>
> Square Root O(√n)
>
> Quadratic O(n²)
>
> Cubic O(n³)
>
> Polynomial O(n^k)
>
> Exponential O(k^n)
>
> Factorial O(n!)


### Simplified Asymptotic Analysis
Like mentioned previously, once we have obtained the time complexity of an algorithm by counting primitive operations, we can arrive at the Big O notation for the algorithm by:
- dropping the multiplicative constants with all terms
- dropping all bu the highest order term

> ### Example
> n² + 2n + 1 is O(n²)<br />
> n⁵ + 4n³ + 2n + 43 is O(n⁵)

**Polynomials of degree K is O(kⁿ)**
All polynomial functions f(n) of degree k are O(kⁿ). See proof. The polynomial proof tells you that you can ignore all the other terms in the polynomial because they are dominated by the leading term.

### Why Big O is preferred over other notations
It tends to be more useful to know that the worst case running time of a particular algorithm will grow at most as fast as a constant multiple of a certain function than to know that it will grow at least as fast as some other function.

### Useful Formulas & General Tips When Calculating the Time Complexity
- every time a list or array gets iteerated over c x length times, it is most likely O(n) time
- when you see a problem where the number of elements in the problem space gets halved each time, that will most probably be in O(log n) runtime
- whenever you have a singly nested loop, the problem is most likely in quadratic time

