# Introduction to Lists
In this lesson, we define lists, how they are used in Python and how they are different from arrays.

In Python, a ***list*** is an ordered sequence of heterogeneous elements (can hold elements with different data types).

Example:
```
list = ['a', 'apple', 23, 3.14]
```

Lists can hold:
- integers
- strings
- characters
- functions
- any other data type including other lists

The elements can be accessed or ‘indexed’ using square brackets. The first element in a list is accessed using index 0 (as on line 7), the second element is accessed using 1, and so on.

## Important List Functions
These are some of the most useful built-in Python list functions.

### The ``` Append() ``` function
Use this function to add a single element to the end of a list.
- Use it like ```list.append(value)```
- Time Complexity: **O(1)** constant time.
```
list = [1, 3, 5, 'seven']
print(list)
list.append(9)
print(list)
```
**Output**
```
[1, 3, 5, 'seven']
[1, 3, 5, 'seven', 9]
```
<br />

### The ``` Insert() ``` function
Inserts an element to the list.
- Use it like ```list.insert(index, value)```.
- Time Complexity: **O(1)** constant time.
```
list = [1, 3, 5, 'seven']
list.insert(0, 2)
print(list)
```
**Output**
```
[2, 1, 3, 5, 'seven']
```
<br />

### The ``` Remove() ``` function
This function removes the given element at a given index.
- Use it like ```list.remove(element)```
- Time Complexity: **O(n)** constant time
- Runtime error if value does not exist

```
list = [1, 3, 5, 'seven']
print(list)
list.remove('seven')
print(list)
list.remove(0)
print(list)
```

**Output**
```
[1, 3, 5, 'seven']
[1, 3, 5]
Traceback (most recent call last):
  File "main.py", line 5, in <module>
    list.remove(0)
ValueError: list.remove(x): x not in list
```
<br />

### The ``` pop() ``` function
Removes the element at the given index. If no index is given, then it removes the last element. So ```list.pop()``` would remove the last element. Time complexity depends on which element is removed.
- Time Complexity: **O(1)** for the last element
- Time complexity: **O(n)** Removing anything other than the last element

```
list = [1, 3, 5, 'seven']
print(list)
```

**Output**
```
[1, 3, 5, 'seven']
```
<br />

### The ``` Reverse() ``` function
Reverses a list.
- Use it as ```list.reverse()```
- Time complexity *O(n)**

```
list = [1, 3, 5, 'seven']
print(list)
list.reverse()
print(list)
```

**Output**
```
[1, 3, 5, 'seven']
['seven', 5, 3, 1]
```
<br />

