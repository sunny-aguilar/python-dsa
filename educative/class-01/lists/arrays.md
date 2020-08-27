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
**Line 4** creates an array. ```d``` indicates that the array is of type float.

## Types of Arrays
There are several types of array in Python:

|Type code        |C Type       |Python Type        |Minimum Size in Bytes      |
|-----------------|-------------|-------------------|---------------------------|
|```c```           |character   |char               |1                           |
|```f```           |float       |float              |4                           |
|```d```           |double      |float              |8                           |
There are a few more like signed/unsigned int/short/long.

## Array Slicing
Array slicind is done in exactly the same way as list slicing is done.

### Changing or adding array elements
Arrays are mutable; their elements can be changed in the same way as list elements.
**Example:**
```
import array
integers = array.array('i', [1, 2, 3, 5, 7, 10])

# changing first element
integers[0] = 0
print(integers)  # array('i', [0, 2, 3, 5, 7, 10])

# changing 3rd to 5th element
integers[2:5] = array.array('i', [4, 6, 8])
print(integers)     # Output: array('i', [0, 2, 4, 6, 8, 10])
```

**Output:**
```
array('i', [0, 2, 3, 5, 7, 10])
array('i', [0, 2, 4, 6, 8, 10])
```




