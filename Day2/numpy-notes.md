1. What is NumPy?

NumPy (Numerical Python) is a Python library for fast numerical computation.

It provides:

N-dimensional arrays (ndarray)

Fast mathematical operations

Tools for linear algebra, statistics, broadcasting, etc.

NumPy arrays are much faster and memory-efficient than Python lists.

2. Why Use NumPy Over Python Lists?

Python lists:

Can store mixed data types → slow

No vectorized operations → uses loops

Higher memory usage

NumPy arrays:

Homogeneous data (all items same type)

Vectorized operations (no loops)

Faster due to C-optimizations

Less memory usage

3. Creating NumPy Arrays
import numpy as np

(a) From Python List
arr = np.array([1, 2, 3])

(b) Multi-dimensional Array
arr2 = np.array([[1, 2, 3], [4, 5, 6]])

4. Array Attributes
Property	Meaning	Example
arr.ndim	Number of dimensions	1D / 2D
arr.shape	Rows × Columns	(2, 3)
arr.size	Total elements	6
arr.dtype	Data type	int32 / float64
5. Useful NumPy Functions
Zeros array
np.zeros((3, 3))

Ones array
np.ones((2, 4))

Range
np.arange(1, 10, 2)

Even spacing
np.linspace(1, 5, 10)

6. Array Indexing
1D
arr[0], arr[-1]

2D
arr2[0, 1]   # row 0, col 1

7. Array Slicing
1D
arr[1:4]
arr[:3]
arr[::2]     # step = 2

2D
arr2[:, 1]    # all rows, column 1
arr2[0:2, 1:3]

8. Vectorized Operations (No Loops)
arr + 2
arr * 5
arr1 + arr2
arr1 / arr2


Vectorization = very fast operations applied to entire arrays.

9. Broadcasting

Allows operations on arrays of different shapes, automatically expanding smaller array.

Example:

arr2 = np.array([[1,2,3],[4,5,6]])
arr2 + 10


(10 is broadcast across every element)

10. Mathematical Functions
np.sqrt(arr)
np.exp(arr)
np.log(arr)
np.mean(arr)
np.median(arr)
np.std(arr)

11. Boolean Indexing
arr[arr > 5]

12. Real-World Example
Example: Temperature Conversion

Convert Celsius to Fahrenheit:

c = np.array([0, 10, 20, 30])
f = c * 9/5 + 32

Example: Marks Dataset
marks = np.array([45, 67, 89, 72, 56])
marks.mean()
marks.std()
marks.max()

13. Reshaping Arrays
arr.reshape(3, 2)

14. Flattening
arr.ravel()   # returns 1D view

15. Copy vs View

view() → shares memory

copy() → creates new array

Example:

a = np.array([1,2,3])
b = a.view()
c = a.copy()

16. Sorting
np.sort(arr)

17. Axis Parameter
Row-wise & column-wise operations
arr2.sum(axis=0)   # column-wise
arr2.sum(axis=1)   # row-wise

18. Random Module
np.random.rand(3, 3)
np.random.randint(1, 10, (2, 2))
