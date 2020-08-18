# Challenge 1: Big O of Nested Loop with Multiplication
Compute the Big O complexity of an algorithm which involves nested loops and the loop variables increment with multiplication.

## Problem Statement
**Code Snippet**
```

n = 10  # Can be anything
sum = 0
pie = 3.14
var = 1
while var < n:
    print(pie)
    for j in range(var):
        sum += 1
    var *= 2
print(sum)

```

### My Solution:
Outer loop runs n times. Inner loop runs (n * k) times. Since it is increasing by a contant multiple, then it is running in log time. Therefore, we have a total run time of n * log n = O(n⋅logn)

### Solution Review:
The answer is O(n). The outer loop runs log(n)

