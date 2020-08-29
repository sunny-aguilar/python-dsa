# Lists vs Arrays in Python
## Differences
Python lists are very flexible and can hold completely heterogeneous arbitrary data but they use a lot more space than Python arrays. Each list contains points to a block of pointers, each of which in turn points to a full Python object.
- lists offer flexibility since each list element is a full structure containing both data and type info
- arrays lack flexibility but are more efficient for storing and manipulating data
![Image](https://i.ibb.co/WzFrKfW/Screen-Shot-2020-08-29-at-2-58-50-PM.png)

## Similarities
Arrays and lists are similarly both syntactical usage and functionality.
- both are mutable, i.e., the data in both is not contant and can be modified
- both can also be indexed and iterated through
- both can be sliced the same way

## When to use arrays and when to use lists
Arrays are better when yo uneed to store a lot of data and perform a large number of computationally intensive mathematical operations (NumPy is best suited for mathematical use cases).

## The NumPy Library
Here is how a NumPy array is initialized. They’re used in algorithms where a lot of mathematical operations are performed on large sets of data such as most machine learning algorithms.

```
import numpy as np
numpy_array = np.array([1, 2, 3])
print(numpy_array)
```


