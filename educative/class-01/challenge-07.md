# Challenge 7: Nested Loop with Multiplication
A pro-level exercise based on the Big O of an algorithm which involves nested loops and the loop variables increment with multiplication and addition.

## Problem Statement
**Code Snippet**
```

n = 10  # can be anything
sum = 0
pie = 3.14
j = 1

for var in range(n):
    while j < var:
        sum += 1
        j *= 2
    print(sum)

```

### My solution:
Outerloop runs n times. Inner loop has j doubling at each iteration. Var is also increasing by 1 at each iteration.

### Solution Review:
Running Time Complexity = 1 + 1 + 1 + n + n + n + n = 3 + 5n.
