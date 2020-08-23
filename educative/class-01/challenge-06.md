# Challenge 6: Nested Loop with Multiplication
A more advanced exercise based on the Big O of an algorithm which involves nested loops and the loop variables increment with multiplication.

## Problem Statement
**Code Snippet**
```

n = 10  # can be anything
sum = 0
pie = 3.14

for i in range(n):
    j = 1
    while j < i:
        sum += 1
        j *= 2
    print(sum)

```

### My solution:
The outer loop runs n times. The inner loop runs log₂(n) times. Therefore we have nlog₂(n).

### Solution Review:
The outer loop is O(n) as it iterates over n. The inner while loop iterates over i which is always less than n and j is doubled each time therefore it is O(log₂(n)). Therefore, the total becomes O(n⋅log₂(n))
