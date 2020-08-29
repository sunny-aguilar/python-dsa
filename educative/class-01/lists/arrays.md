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

### Append and Extend Methods
We can add one time to the end of an array using ```append()``` method or add several items using the ```extend()``` method

```
import array

numbers = array.array('i', [1, 2, 3])

numbers.append(4)
print(numbers)                              # array('i', [1, 2, 3, 4])

## extend() appends iterable to the end of the array
numbers.extend([5, 6, 7])
print(numbers)                              # array('i', [1, 2, 3, 4, 5, 6, 7])
```

### + operator (concatenation)
You can concatenate two arrays using the + operator

```
import array

odd = array.array('i', [1, 3, 5])
even = array.array('i', [2, 4, 6])

integers = array.array('i')                 # creating empty array of integer
integers = odd + even

print(integers)
```

### How do you remove/delete elements?
TO delete one or more items from an array, use the del statement as with lists

```
import array

integer_array = array.array('i', [1, 2, 3, 3, 4])

del integer_array[2]              # removing third element
print(integer_array)              # Output: array('i', [1, 2, 3, 4])

del integer_array                 # deleting entire array
print(integer_array)              # Error: array is not defined
```

You can also use the ```remove(val)``` method that will remove the first element that is equal to ```val``` in the array.
> **Note:** An error is thrown if the index exceeds the size of the array or element is not found in the array.


