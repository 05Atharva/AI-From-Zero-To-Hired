#  NumPy Day 3 – Intermediate Concepts

##  np.random.shuffle()

- Shuffles an existing array **in-place**.
- Does **not return** a new array.
- Only works along the **first axis**.


arr = np.arange(5)
np.random.shuffle(arr)
print(arr)  # Elements are shuffled
np.transpose() on 1D vs 2D
For 1D arrays, .T has no effect.

For 2D+ arrays, it swaps axes (rows ↔ columns).


a = np.array([1, 2, 3])
print(a.T)  # Same as original

b = np.array([[1, 2, 3], [4, 5, 6]])
print(b.T)  # Transposed
 Flattening Arrays
.flatten() returns a copy of the array flattened to 1D.

.ravel() returns a view (if possible) of the flattened array.


matrix = np.array([[1, 2], [3, 4]])
flat = matrix.flatten()
Stacking Arrays
Combine arrays vertically or horizontally:

np.vstack() → stacks along vertical axis (rows).

np.hstack() → stacks along horizontal axis (columns).


a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
np.vstack((a, b))
np.hstack((a, b))
np.intersect1d()
Returns the common elements in two arrays (sorted & unique).


a = np.array([1, 2, 3, 4])
b = np.array([3, 4, 5])
np.intersect1d(a, b)  # [3, 4]
Copy vs View
.copy() → creates a completely new object (deep copy).

.view() → creates a shallow copy, changes reflect in original.


original = np.array([1, 2, 3])

# View shares memory
view = original.view()
view[0] = 99
print(original)  # [99  2  3]

# Copy does not affect original
copy = original.copy()
copy[1] = 88
print(original)  # Still [99  2  3]
Summary
Shuffle: Use np.random.shuffle() to reorder arrays in-place.

Flatten vs Transpose: Flatten to 1D, transpose only matters for 2D+.

Stack arrays using vstack, hstack after reshaping.

Use intersect1d() for finding common values.

Always prefer .copy() if original data must remain unchanged.