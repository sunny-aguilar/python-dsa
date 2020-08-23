# Challenge 4: Nested Loop with Multiplication
An exercise based on the Big O of an algorithm which involves nested loops and the loop variables increment with multiplication.

## Problem Statement
**Code Snippet**
```

n = 10  # n can be anything, this is just an example
sum = 0
pie = 3.14
var = 1

while var < n:
    print(pie)
    for j in range(1, n, 2):
        sum += 1
    var *= 3
print(sum)

```

### Solution Review:
The outer loop runs a total of log_3(n)log(n) times. The inner loop, on the other hand, runs a total of log_3(n) x (n/2). **Therefore, the Big O complexity is: O(n⋅log_2(n))**

**Explanation**
The outer loop ``` while var < n ``` runs log₃(n) times since ``` var ``` will first be equal to 1, then 3, then 9, ..., until it is 3^k such that 3^k ≤ n. This means that the outer loop runs a total of log₃(n) times. The inner loop runs a total of log₃(n) x (n/2).

**Running Time Complexity Calc**
log₃(n) + n⋅log₃(n) => n⋅log₃(n) => log₂(n) / log₂(3) = n⋅log₂(n) / 1.585 => n⋅log₂(n) => O(n⋅log₂(n))

**Change of Base:**
We want to change from base 3 to base 2 so we can convert this using the property of log_a(b) = log_c(b) / log_c(a)<br />
log₃(n) => log₂(n) / log₂(3)

