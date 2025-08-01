# 📘 NumPy Notes - Day 2

---

## 🔢 Mathematical Operations

Performed element-wise operations on arrays:
a + b     # Addition
a - b     # Subtraction
a * b     # Multiplication
a / b     # Division
Supports broadcasting (e.g., scalar + array)

Boolean Indexing
Filter elements using conditions:

arr = np.array([10, 20, 30, 40])
arr[arr > 25]   # Output: [30 40]
Creates a Boolean mask and returns only True elements.

Fancy Indexing
Select multiple non-contiguous elements:

x = np.array([100, 200, 300, 400, 500])
x[[1, 3, 4]]  # Output: [200 400 500]

Conditional Replacement
Modify values based on a condition:

a = np.array([1, 2, 3, 4])
a[a > 2] = 99  # Output: [1 2 99 99]

Aggregation Functions
Quick statistics using built-in NumPy functions:


np.sum(arr)       # Total sum
np.max(arr)       # Maximum value
np.min(arr)       # Minimum value
np.mean(arr)      # Mean value
With axis:

np.sum(arr, axis=0)   # Column-wise
np.sum(arr, axis=1)   # Row-wise