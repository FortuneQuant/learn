---
title: Linear Algebra
weight: 30
math: true
---

MITOCW: [Matrix Methods in Data Analysis, Signal Processing, and Machine Learning](https://ocw.mit.edu/courses/18-065-matrix-methods-in-data-analysis-signal-processing-and-machine-learning-spring-2018/)

Textbook: [Linear Algebra and Learning from Data (2019)](https://www.zotero.org/dafuzhu123/collections/R28S2AQK/items/IQNNZ39I/reader), website click [here](https://math.mit.edu/~gs/learningfromdata/)

## Problems

Section I.1 | 18. If $A = CR$, what are the $C$ and $R$ factors of the matrix $\begin{bmatrix} 
0 & A \\\ 
0 & A 
\end{bmatrix}$?



## Notes

### Factoring matrix $A$

Factorization $A=CR$, $R=\text{rref}(A)=\text{row-reduced echelon form of A}$

row space of A = $C(A^T)$

$A=\mathbf{CMR}\xrightarrow{\mathbf{C^T}A\mathbf{R^T}}\mathbf{M}=\mathbf{(C^T C)^{-1}(C^T} A\mathbf{R^T)(RR^T)^{-1}}$

Insights on **Elimination** $A=LU$
$$
A=\begin{bmatrix}
a_{11} & a_{12} & \cdots & a_{1n}\\\
a_{21} & & & \\\
\vdots & & \cdots & \\\
a_{m1} & & & \\\
\end{bmatrix}
=(\text{col}1)(\text{row}1)+
\begin{bmatrix}
0 & 0 & \cdots & 0\\\
0 & & & \\\
\vdots & & A_2 & \\\
0 & & & \\\
\end{bmatrix}=\cdots
$$

$$
LU=\begin{bmatrix}
\\\
l_1\\\
\\\
\end{bmatrix}
\begin{bmatrix}
& u_1^T &
\end{bmatrix}+
\begin{bmatrix}
\\\
l_2\\\
\\\
\end{bmatrix}
\begin{bmatrix}
& u_2^T &
\end{bmatrix}+\cdots
$$

What makes a space? You can do **linear combinations** here
$$
x,y\text{ in a space}\Leftrightarrow cx, x+y\text{ are also in that space}
$$

- Column space $C(A)$: dim=r

- Row space $C(A^T )$: dim=r
- Nullspace $N(A)$
- Nullspace $N(A^T )$
