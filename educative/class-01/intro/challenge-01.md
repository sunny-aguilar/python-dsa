# Challenge 1: Big O of Nested Loop with Addition
Compute the Big O complexity of an algorithm which involves nested loops where the loop variable increase with addition.

## Problem Statement
**Code Snippet**
```
n = 20
sum = 0
pie = 3.14

for var in range(i, n, 3):
  print(pie)
  for j in range(1, n, 2):
    sum += 1
    print(sum)

```

### Solution Review:
The line ```for var in range(1,n,3)``` gets executed n/3 times and the ```for j in range(1,n,2)``` gets executed n/2 times for each iteration of the outer loop which makes it run a total of n/3 x n/2 which is O(n²)



