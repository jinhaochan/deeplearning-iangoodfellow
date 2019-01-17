# Linear Algebra

## 1. Scalars, Vectors, Matrices and Tensors

1. Scalars are single numbers
2. Vectors are an array of numbers
3. Matrices are a 2D array of numbers
4. Tensors are a type of Matrix with more than 2 dimensions

## 2. Matrix Operations

1. Matrix Multiplication

`A * B` 

`A` must have the same number of columns as `B` has rows

## 3. Matrix Inverse and Identity Matrix

An identity matrix does not change any vector when multiplied by it

A matrix multiplied by it's inverse will give you an Identity matrix

## 4. Linear Dependence and Span

**Linear Combination** is multiplying each vector by a scalar coefficient, and adding the results together

The **Span** is a set of points obtained by linear combination of the original vector

Determining if `Ax = b` has a solution, hence involves finding if `b` lies in the span of `A`

A set of vectors are **linearly independent** if no vectors are a linear combination of other vectors

## 5. Normalization

Norms are measuring the size of vectors

Norms map vectors to a non-negative value. Intuitively, the norm of a vector measures the distance from the origin to point `x`

**IMAGE 1**

`L2` norm is the **Euclidean Norm**, which is the Euclidean distance from the origin to point `x`

The squared `L2` norm is easier to work with, and is used more often

In some cases, the squared of `L2` norm increases very slowly near the origin.
This may be undesirable because we want to discriminate elements that are exactly zero, and close to zero

A function that grows at the same rate in all locations is the `L1` norm

**`L1` norms are used when it is important to distinguish zero and non-zero elements**

A **Max Norm** is when `p` = infinitely large. That results in`max(x)`, which returns the largest magnitude in the vector

## 6. Special Matrix and Vectors

1. Diagonal Matrix has mostly nonzero values along the main diagonal (top right to bottom right).

**Non-square Diagonal Matrices do not have an inverse.**

2. Symmetric Matrix is a matrix that is equal to it's transpose

3. A Unit Vector is a vector with `norm = 1`

4. Orthogonal Vectors are `90 degrees` to each other, and their dot product returns `0`.

Symbolically, this means that they have no relationship with each other.

## 7. Eigen-decomposition

Eigen-decomposition is breaking down a matrix to it's constituent parts, that will show us information about their functional properties

The decomposition breaks down a matrix into **Eigen-Vectors** and **Eigen-Values**

Eigen-Vectors of a square matrix `A` is a nonzero vector `v`, such that when `v` is multiplied by `A`, it only alters the scale of `v`

The scalar change when `A` is multiplied by `v` is the Eigen-value

Any symmetric matrix `A` is guaranteed to have an eigen-decomposition, but may not be unique.

A matrix is **singular** iff any of the eigen-values are `0`

## 8. Single Value Decomposition (SVD)

SVD is another way of decomposing matrices to its constituent components

Like eigen-decomposition which gave us eigen-vectors and eigen-values, SVD gives us **singular-vectors** and **singular-values**

Every real matrix has an SVD, but not necessarily an eigen-decomposition

A matrix `A` can be decomposed into `A=U D (V^-1)`

Where `U` and `V` are orthogonal matrices, and `D` is a diagonal matrix that is not necessarily square.

Elements across `D` are the singular-values of matrix `A`

Columns of `U` are the left singular vectors

Columns of `V` are the right singular vectors

## 9. Moore-Penrose Pseudoinverse

Matrix Inversions are undefined for non-square matrices.

MPP performs some matrix manipulation to allow matrix inversions for non-square matrices

## 10. Trace Operator

The trace operator gives us the sum of all diagonal entries of a matrix

## 11. Determinant of a Matrix

The determinant of a square matrix `det(A)` is a function that maps a matrix to a real scalar value.

**The determinant is the product of all eigen-values of matrix `A`**

**The value of the determinant of `A` can be thought of as a measure of how much multiplication of another matrix `B` by matrix `A` expands or contracts `B`**

If `det(A) = 0`, space is contracted completely along at least 1 dimension, losing all it's volume

If `det(A) = 1`, the transformation preserves its volume completely

## 12. Principal Component Analysis (PCA)

PCA encodes points to a lower dimension (dimensionality reduction), trading off precision for lesser memory requirement

For each point `x`, we want to find a vector `c` by finding a PCA encoding function `f()`, such that `f(x) = c`

A correspongind decoding function `g()` can restore the original points `g(f(x)) ~~ x`

