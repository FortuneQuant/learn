---
title: Linear Algebra
weight: 30
---

Coursera: [HKUST Matrix Algebra](https://www.coursera.org/learn/matrix-algebra-engineers)

## Matrices

**Transpose and inverse**

> Show using the transpose operator that any square matrix A can be written as the sum of a symmetric and a skew-symmetric matrix.

Solution: Since $A+A^T$ is symmetric, $A-A^T$ is skew-symmetric
$$
A=\frac 12(A+A^T)+\frac 12(A-A^T)
$$
**Inner and outer products**

> Prove that $\text{Tr}(A^TA)$ is the sum of the squares of all the elements of A.

Solution: Suppose A is m-by-n matrix
$$
\text{Tr}(A^TA)=\sum_{j=1}^n[A^TA]_{jj}=\sum_{j=1}^n\sum_{i=1}^n[a_{ji}^Ta_{ij}]=\sum_{j=1}^n\sum_{i=1}^na_{ij}^2
$$
