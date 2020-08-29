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
- Time complexity: **O(n)**

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

## What is Slicing?
Accessing/modifying several elements from objects such as lists/strings/tuples requires using a for-loop in most languages but in Python, you can use square brackets and a colon to define a range of elements within a list that you wan to access or 'slice.'
```
list[start:end]
```
-  note that 'end' is index - 1 or the total number of elements starting with 'start'

### Slide Notation Example
An example using slicing to perform various operations on lists.

**Example 1: Indexing elements of a list**
List elements can be indexed and printed as follows:
```
list = list(range(10))                          # create a list
print(list)                                     # print the list
print(list[0:4])                                # output a slice of the list
```
output
```
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
[0, 1, 2, 3]
```

With Python lists, it is not necessary to specify the last or first index; you can simply leave the end or start blank
|Index          |Meaning                                        |
|---------------|-----------------------------------------------|
|list[start:]   |all numbers greater than start uptil the range |
|list[:end]     |all numbers less than end uptil the range      |
|list[:]        |all numbers within the range                   |

**Example:**
```
list = list(range(10))
print(list[3:])                       # 3, 4, 5, 6, 7, 8, 9
print(list[:3])                       # 0 1 2
print(list[:])                        # 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
```

**Output:**
```
[3, 4, 5, 6, 7, 8, 9]
[0, 1, 2]
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

### Stepped Indexing
You can also index elements in steps like in a for-loop such as
```
for (int i = 0; i < 10; i += 2)
{
  cout << arr[i] << endl;
}
```

**Python Syntax**
```
list[start:stop:step]
```
```step``` specifies the increment (can also decrement)

**Example:**
```
list = list(range(10))          # define a range of 10 values
print(list[0:9:2])              # 0, 2, 4, 6, 8
print(list[9:0:-2])             # 9, 7, 5, 3, 1
```

**Output**
```
[0, 2, 4, 6, 8]
[9, 7, 5, 3, 1]
```

### Initializing List Elements
You can add/modify the contents of a list by specifying a range of elements that you want to update and setting it to the new value:
```
arr[start:end] = [list, of, new, values]
```

**Example:**
```
x = list(range(5))
print(x)                                # 0, 1, 2, 3, 4
x[1:4] = [45, 21, 83]
print(x)                                # 0, 45, 21, 83, 4
```
The 1:4 in the square brackets means that the elements at position 1, 2 and 3 will be set to the new values [45, 21, 84].


**Output:**
```
[0, 1, 2, 3, 4]
[0, 45, 21, 83, 4]
```

### Deleting Elements from a List Elements
The del keyword is used to delete elements from a list.
```
arr[start:end] = [list, of, new, values]
```

**Example:**
```
list = list(range(10))
print(list)                                 # 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
del list[::2]
print(list)                                 # 1, 3, 5, 7, 9
```

**Output:**
```
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
[1, 3, 5, 7, 9]
```

***Explanation:*** Here, the empty start and end indices refer to 0 and length of the list by default, whereas 2 is the step size.


### Negative Indexing
We can use negative numbers to begin indexing the list elements from the end.
```
arr[-5]
```
Here, this would access the fifth-last element of a list.

**Example:**
```
list = list(range(10))
print(list)
print(list[4:-1])  # 4, 5, 6, 7, 8
```

**Output:**
```
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
[4, 5, 6, 7, 8]
```
Here, the list above displays from the 4th index to the second last index


### Slicing in Strings
We can also use the slicing technique on strings since strings are an array of characters.
**Example:**
```
my_string = "somehow"
string1 = my_string[:4]
string2 = my_string[4:]
print(string1, string2)
```

**Output:**
```
some how
```
