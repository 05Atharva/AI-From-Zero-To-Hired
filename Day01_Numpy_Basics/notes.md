# Day 1: NumPy Basics

## What is NumPy?
NumPy is a Python library used for numerical computations. It provides support for arrays, matrices, and many mathematical functions to operate on these data structures.

---

## Why Use NumPy?
- Faster than Python lists
- Offers broadcasting and vectorization
- Supports multidimensional arrays
- Rich set of mathematical operations

---

## NumPy Arrays
### Creating Arrays

import numpy as np

# 1D Array
a = np.array([1, 2, 3])

# 2D Array
b = np.array([[1, 2, 3], [4, 5, 6]])

# Zeros
z = np.zeros((2, 3))

# Ones
o = np.ones((3, 3))

# Full
f = np.full((2, 2), 7)

# Identity matrix
i = np.eye(3)

# Random values
r = np.random.rand(2, 2)

# Range
ar = np.arange(10)

# Linspace
l = np.linspace(0, 1, 5)

Array Attributes
a = np.array([1, 2, 3])
print(a.shape)        # (3,)
print(a.dtype)        # int32
print(a.ndim)         # 1
print(a.size)         # 3

Indexing and Slicing
arr = np.array([[1, 2, 3], [4, 5, 6]])
print(arr[0, 1])      # 2
print(arr[:1])        # [[1 2 3]]
print(arr[1, :])      # [4 5 6]

Reshaping and Slicing
y = np.arange(16).reshape(4, 4)
sliced = y[1:3, :]
print(sliced)
# Output:
# [[ 4  5  6  7]
#  [ 8  9 10 11]]

Broadcasting
a = np.array([[1], [2], [3]])
b = np.array([10, 20, 30])
result = a * b
print(result)
# Output:
# [[10 20 30]
#  [20 40 60]
#  [30 60 90]]

# Math Functions
z = np.array([1, 2, 3, 4, 5])
print(np.mean(z))     # 3.0
print(np.median(z))   # 3.0
print(np.std(z))      # 1.4142...

# Practice Exercises with Solutions
# Create a 2D array of shape (3, 4) filled with 7s
arr = np.full((3, 4), 7)
print(arr)
# [[7 7 7 7]
# [7 7 7 7]
# [7 7 7 7]]

# Create a NumPy array from 1 to 100 and reshape to (10, 10)
x = np.arange(1, 101).reshape((10, 10))
print(x)
# [[  1   2   3   4   5   6   7   8   9  10]
# [ 11  12  13  14  15  16  17  18  19  20]
# [ 21  22  23  24  25  26  27  28  29  30]
# [ 31  32  33  34  35  36  37  38  39  40]
# [ 41  42  43  44  45  46  47  48  49  50]
# [ 51  52  53  54  55  56  57  58  59  60]
# [ 61  62  63  64  65  66  67  68  69  70]
# [ 71  72  73  74  75  76  77  78  79  80]
# [ 81  82  83  84  85  86  87  88  89  90]
# [ 91  92  93  94  95  96  97  98  99 100]]

# Slice out the 2nd and 3rd rows from a 4x4 array
y = np.arange(16).reshape(4, 4)
sliced = y[1:3, :]
print(sliced)
# [[ 4  5  6  7]
# [ 8  9 10 11]]

# Multiply two arrays using broadcasting
a = np.array([[1], [2], [3]])
b = np.array([10, 20, 30])
result = a * b
print(result)
# [[10 20 30]
# [20 40 60]
# [30 60 90]]

# Find the mean, median, and standard deviation
z = np.array([1, 2, 3, 4, 5])
print(np.mean(z))     # 3.0
print(np.median(z))   # 3.0
print(np.std(z))      # 1.4142135...
