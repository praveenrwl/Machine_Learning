Data Science Mentorship Program (DSMP) 2022-23

### Notes on NumPy: A Comprehensive Guide to Understanding the Library

---

**Introduction to NumPy**  
NumPy (Numerical Python) is an essential Python library widely used for numerical computations, data manipulation, and scientific computing. It provides support for multi-dimensional arrays, matrices, and a large collection of mathematical functions to operate on these arrays. 

---

### 1. **Key Features of NumPy**
   - **Efficient Data Structures:** NumPy arrays (ndarrays) are optimized for numerical operations and are more efficient than Python lists.
   - **Multidimensional Array Support:** It supports n-dimensional arrays that allow for efficient operations on data structures like matrices.
   - **Broadcasting:** A mechanism that allows arithmetic operations on arrays of different shapes, making computations more efficient and concise.
   - **Extensive Mathematical Functions:** Includes linear algebra, random number generation, Fourier transforms, and more.
   - **Integration:** Works seamlessly with other libraries like Pandas, Matplotlib, SciPy, and machine learning frameworks.
   - **Interoperability:** Easily integrates with C/C++, Fortran, and other low-level programming languages for faster computations.

---

### 2. **Understanding NumPy Arrays**

#### a. **NumPy Array Basics**
   - **ndarray:** The core object in NumPy is the `ndarray`, a homogeneous multidimensional array.
   - **Advantages Over Python Lists:**
     - Faster computations.
     - Fixed size, which reduces memory overhead.
     - Allows vectorized operations, avoiding the need for explicit loops.
   - **Creating Arrays:**
     - From lists: `np.array([1, 2, 3])`
     - Predefined methods: `np.zeros((2, 2))`, `np.ones((3, 3))`, `np.eye(4)` (identity matrix).

#### b. **Key Properties of Arrays**
   - `shape`: Dimensions of the array.
   - `dtype`: Data type of elements (e.g., `int`, `float`).
   - `size`: Total number of elements in the array.
   - `ndim`: Number of dimensions.

---

### 3. **Array Operations**

#### a. **Arithmetic Operations**
   - Arrays support element-wise addition, subtraction, multiplication, and division:
     ```python
     arr1 = np.array([1, 2, 3])
     arr2 = np.array([4, 5, 6])
     result = arr1 + arr2  # Output: [5, 7, 9]
     ```

#### b. **Indexing and Slicing**
   - Access elements with indices: `arr[0]` for the first element.
   - Slice arrays using ranges: `arr[1:3]`.
   - Multi-dimensional slicing: 
     ```python
     matrix = np.array([[1, 2], [3, 4]])
     print(matrix[0, 1])  # Output: 2
     ```

#### c. **Boolean Indexing**
   - Use conditions to filter elements: `arr[arr > 2]`.

---

### 4. **Broadcasting**
   - Allows NumPy to perform operations on arrays with different shapes without explicitly replicating data.
   - Example:
     ```python
     arr = np.array([1, 2, 3])
     print(arr + 1)  # Output: [2, 3, 4]
     ```

---

### 5. **Mathematical Functions**
   - Common mathematical functions include:
     - `np.sum()`: Sum of array elements.
     - `np.mean()`: Mean of elements.
     - `np.std()`: Standard deviation.
     - `np.exp()`: Exponential function.
     - `np.sin()`, `np.cos()`: Trigonometric functions.

#### Example:
```python
arr = np.array([1, 2, 3])
print(np.sum(arr))  # Output: 6
print(np.mean(arr))  # Output: 2.0
```

---

### 6. **Linear Algebra with NumPy**
   - Functions to perform operations on matrices and solve systems of equations.
     - `np.dot(a, b)`: Dot product.
     - `np.linalg.inv(matrix)`: Inverse of a matrix.
     - `np.linalg.eig(matrix)`: Eigenvalues and eigenvectors.
   - Example:
     ```python
     A = np.array([[1, 2], [3, 4]])
     B = np.array([[5, 6], [7, 8]])
     print(np.dot(A, B))  # Matrix multiplication
     ```

---

### 7. **Random Number Generation**
   - Generate random numbers for simulations, testing, or machine learning:
     - `np.random.rand()`: Uniform distribution.
     - `np.random.randn()`: Normal distribution.
     - `np.random.randint()`: Random integers.
   - Example:
     ```python
     random_array = np.random.rand(3, 3)
     print(random_array)
     ```

---

### 8. **Reshaping and Manipulating Arrays**

#### a. **Reshape**
   - Change the shape of an array:
     ```python
     arr = np.array([1, 2, 3, 4])
     print(arr.reshape(2, 2))
     ```

#### b. **Concatenation and Splitting**
   - Combine arrays: `np.concatenate((arr1, arr2), axis=0)`.
   - Split arrays: `np.split(array, sections)`.

---

### 9. **Handling Missing Values**
   - Replace missing values with `np.nan`.
   - Use functions like `np.isnan()` to detect NaNs.
   - `np.nanmean()`, `np.nanstd()`: Calculate mean or standard deviation while ignoring NaNs.

---

### 10. **Applications of NumPy**
   - **Data Analysis:** Often used for preprocessing and analyzing datasets in combination with libraries like Pandas.
   - **Machine Learning:** Provides foundational support for frameworks like TensorFlow and PyTorch.
   - **Scientific Computing:** Used in domains like physics, chemistry, and engineering for solving complex mathematical problems.
   - **Image Processing:** Libraries like OpenCV and PIL rely on NumPy for pixel array manipulations.

---

### 11. **Performance and Limitations**

#### a. **Performance**
   - **Vectorized Operations:** Faster computations than Python loops.
   - **Memory Efficiency:** Occupies less memory compared to equivalent Python lists.

#### b. **Limitations**
   - Fixed data types: NumPy arrays are homogeneous, meaning all elements must be of the same type.
   - Requires understanding of broadcasting rules for effective use.
   - Not suited for operations on heterogeneous data (use Pandas in such cases).

---

### 12. **Best Practices**
   - Use vectorized operations instead of loops for better performance.
   - Be cautious with array shapes when performing operations to avoid unexpected results.
   - Leverage NumPy's extensive documentation and built-in functions.

---
