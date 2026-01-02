> **Source & credit** 
>  
> This NumPy cheat sheet is based on the public reference at  
> https://quickref.me/numpy.

---

# NumPy Cheat Sheet

**NumPy** is the fundamental package for scientific computing with Python — focused on fast operations on arrays & matrices. 

## Getting Started

### Introduction

To use NumPy:

```python
import numpy as np
```

---

## Importing / Exporting Data


```python
np.loadtxt('file.txt')  # Load array from a text file
```


```python
np.genfromtxt('file.csv', delimiter=',')    # Load array from a CSV file
```


```python
np.savetxt('file.txt', arr, delimiter=' ')  # Save array to a text file
```


```python
np.savetxt('file.csv', arr, delimiter=',')  # Save array to a CSV file
```



---

## Creating Arrays


```python
np.array([1, 2, 3]) # Create 1D array
```


```python
np.array([(1, 2, 3), (4, 5, 6)])    # Create 2D array
```


```python
np.zeros(3) # 1D array of zeros
```


```python
np.ones((3, 4)) # 3×4 array of ones
```


```python
np.eye(5)   # 5×5 identity matrix
```


```python
np.linspace(0, 100, 6)  # Evenly spaced array
```


```python
np.arange(0, 10, 3) # Range with step
```


```python
np.full((2, 3), 8)  # Full array of constant
```


```python
np.random.rand(4, 5)    # Random floats [0–1]
```


```python
np.random.rand(6, 7) * 100  # Random floats scaled
```


```python
np.random.randint(5, size=(2, 3))   # Random ints
```



---

## Inspecting Properties

```python
arr.size       # Number of elements
arr.shape      # Dimensions
arr.dtype      # Element type
arr.astype(...)# Cast type
arr.tolist()   # To Python list
np.info(np.eye)# Function docs
```



---

## Copying / Sorting / Reshaping

```python
np.copy(arr)        # Copy to new memory
arr.view(dtype)     # View with new dtype
arr.sort()          # Sort in place
arr.sort(axis=0)    # Sort axis
two_d_arr.flatten() # Flatten to 1D
arr.T               # Transpose
arr.reshape(3,4)    # Reshape
arr.resize((5,6))   # Resize (fill new with 0)
```



---

## Adding / Removing Elements

```python
np.append(arr, values)
np.insert(arr, 2, values)
np.delete(arr, 3, axis=0)
np.delete(arr, 4, axis=1)
```



---

## Combining / Splitting

```python
np.concatenate((arr1, arr2), axis=0) # Add rows
np.concatenate((arr1, arr2), axis=1) # Add cols
np.split(arr, 3)   # Split into 3
np.hsplit(arr, 5)  # Horizontal split
```



---

## Indexing / Slicing / Subsetting

```python
arr[5]
arr[2,5]
arr[1] = 4
arr[1,3] = 10
arr[0:3]
arr[0:3, 4]
arr[:2]
arr[:, 1]
```

Boolean indexing:

```python
arr < 5
(arr1 < 3) & (arr2 > 5)
~arr
arr[arr < 5]
```



---

## Vector Math


```python
np.add(arr1, arr2)  # Elementwise add
```


```python
np.subtract(arr1, arr2) # Elementwise subtract
```


```python
np.multiply(arr1, arr2) # Elementwise multiply
```


```python
np.divide(arr1, arr2)   # Elementwise divide
```


```python
np.power(arr1, arr2)    # Elementwise power
```


```python
np.array_equal(arr1, arr2)  # Compare arrays
```


```python
# Elementwise universal functions
np.sqrt(arr)
np.sin(arr)
np.log(arr)
np.abs(arr)
np.ceil(arr)
np.floor(arr)
np.round(arr)
```



---

## Scalar Math

```python
np.add(arr, 1)
np.subtract(arr, 2)
np.multiply(arr, 3)
np.divide(arr, 4)
np.power(arr, 5)
```



---

## Statistics

```python
np.mean(arr, axis=0)
arr.sum()
arr.min()
arr.max(axis=0)
np.var(arr)
np.std(arr, axis=1)
arr.corrcoef()
```



---
