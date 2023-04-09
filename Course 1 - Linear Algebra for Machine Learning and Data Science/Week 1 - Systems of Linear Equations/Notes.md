# Singular and Non-singular Matrix
A matrix is singular if the determinant of the matrix is zero, and non-singular if the determinant is non-zero.
```math
$$A = \begin{bmatrix}
5 & 1 \\
-1 & 3
\end{bmatrix}$$
```
The determinant is $(5)(3) - (-1)(1) = 15 - -1 = 16$. (Non-singular) \
For a matrix 
```math
$$B = \begin{bmatrix}
2 & -1 \\
-6 & 3
\end{bmatrix}$$
```
The determinant is $(2)(3) - (-1)(-6) = 6 - 6 = 0$. (Singular)

A system of rows of square matrix are *linearly independent* if and only if the determinant of the matrix is not equal to zero. If the determinant of the matrix equals zero, then the rows of square matrix are *linearly dependent*.

# Linear dependence and independence (3x3 matrices)

A two-by-two matrice has linearly dependent rows, if one row is a multiple of the other one.

For larger matrix, if one row can be obtained from the others then the matrices have linearly dependent rows, .


Consider the matrix below:
```math
$$Matrix~ A = \begin{bmatrix}
1 & 1 & 1 \\
1 & 1 & 2 \\
0 & 0 & -1
\end{bmatrix}$$
```
The difference of the first two rows equals the third row i.e., Row3 depends on Row1 and Row2 

$\therefore$ the rows are linearly dependent. The matrix is singular, and the rows are linearly dependent. 

Row1 - Row2 = Row3 &ensp; **Dependent (singular)** 


Consider the matrix below:
```math
$$Matrix~B = \begin{bmatrix}
1 & 0 & 1 \\
0 & 1 & 0 \\
3 & 2 & 3
\end{bmatrix}$$
```
3Row1 + 2Row2 = Row3 &ensp; **Dependent (singular)**


Consider the matrix below:
 ```math
$$Matrix~ C = \begin{bmatrix}
1 & 1 & 1 \\
0 & 0 & 2 \\
0 & 0 & 3
\end{bmatrix}$$
```
No relations &ensp; **Independent (Non-singular)**

The determinant of a three-by-three matrix is:
```math
$$det(A) = 
det \begin{bmatrix}
a & b & c \\
d & e & f \\
g & h & i
\end{bmatrix} = 
a.det\begin{bmatrix}e & f \\
                    h & i
     \end{bmatrix} - b.det\begin{bmatrix}d & f \\
                    g & i
     \end{bmatrix} + c.det\begin{bmatrix}d & e \\
                    g & h
     \end{bmatrix}                       
$$
```
