# Challenge 5: Nested Loop with Multiplication
A more complex exercise based on the Big O of an algorithm which involves nested loops and the loop variables increment with multiplication.

## Problem Statement
**Code Snippet**
```

n = 10  # can be anything, this is just an example
sum = 0
pie = 3.14

for var in range(1, n, 3):      // n/3 => n
    j = 1
    print(pie)
    while j < n:                // log₃(n)
        sum += 1
        j *= 3
print(sum)  # O(1)

```

### My solution:
The outer loop runs in n/3 => n time and the inner loop runs in log₃(n) time therefore we have a combined total runtime of n⋅log₃(n)

### Solution Review:
- Outer Loop: 1 + 3 + 6 + 9 + ... + n = n/3
- Inner Loop: 1 + 3 + 9 + 27 + ... + n = ​​log₃(n)

Therefore total time complexity is O(n⋅log₃(n))
