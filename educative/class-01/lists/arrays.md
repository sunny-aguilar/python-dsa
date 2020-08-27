# Arrays
Here we learn about arrays and how they are used in Python.

## Introduction
In Python, an array is an ordered sequence of homogeneous elements (can only hold elements of one datatype). The type is constrained and specified at the time of creation.

## Initializing Arrays
Python arrays are initialized using the array library.
```
import array
new_array = array.array('type', [list])
```
```Type``` defines the data type and ```list``` is a Python list containing homogenous elements.

**Example:**
```
import array

# type: 'd' (float), initializer list: [1, 2, 3]
new_array = array.array('d', [1, 2, 3])
print(new_array[0])
```
**Line 4** creates an array. ```d```




