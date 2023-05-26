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

Row1 - Row2 = Row3 ==> &ensp; **Dependent (singular)** 


Consider the matrix below:
```math
$$Matrix~B = \begin{bmatrix}
1 & 0 & 1 \\
0 & 1 & 0 \\
3 & 2 & 3
\end{bmatrix}$$
```
3Row1 + 2Row2 = Row3 ==> &ensp; **Dependent (singular)**


Consider the matrix below:
 ```math
$$Matrix~ C = \begin{bmatrix}
1 & 1 & 1 \\
0 & 0 & 2 \\
0 & 0 & 3
\end{bmatrix}$$
```
No relations ==> &ensp; **Independent (Non-singular)**

The determinant of a 3x3 matrix is:
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

# Solving systems of three equations by hand
Solve this system of equation using elimination
```math
\begin{align}
4a-3b+c &= -10 \quad (1)\\
2a+b+3c &= 0 \quad (2)\\
-a + 2b -5c &= 17 \quad (3)
\end{align}
```
Multiply equation (2) by 2 and subtract from equation (1)

```math
\begin{align}
4a-3b+c &= -10 \qquad \xrightarrow{\text{}}& 4a-3b+c &= -10\\ 
2a+b+3c &= 0 \quad \xrightarrow{\text{multiply (2)}}& 4a+2b+6c &= 0\\
\therefore -5b-5c &= -10 \quad (4)
\end{align}
```
Select equation (2) and equation (3) and eliminate the same variable by multiplying equation 
(3) by 2 and add to equation (2)
```math
\begin{align}
2a+b+3c &= 0 \qquad \xrightarrow{\text{}}& 2a+b+3c &= 0\\ 
-a + 2b -5c &= 17 \quad \xrightarrow{\text{multiply (2)}}& -2a+4b-10c &= 34\\
\therefore 5b-7c &= 34 \quad (5)
\end{align}
```
Solving the system of equations created by equation (4) and (5) by adding equation (4) and (5),
```math
\begin{align}
-5b-5c &= -10 \\ 
(+) \quad 5b-7c &= 34 \\
\implies -12c &= 24 \quad (5) \\
\therefore c = -2
\end{align}
```
From equation (4)
```math
\begin{align}
-5b-5c &= -10 \\ 
-5b &= -10+5c \\
\implies b &= 2 - c \\
\therefore b = 4
\end{align}
```
Substituting the values of b and c in equation (2)
```math
\begin{align}
2a+b+3c &= 0 \\ 
2a &= -b-3c = -(4)-3(-2) \\
\implies 2a &= 2 \\
\therefore a = 1
\end{align}
```
The solution is $a = 1$, $b = 4$, $c = -2$.

# The Rank of a Matrix
The Rank of a matrix is the maximal number of linearly independent columns of A. This, in turn, is identical to the dimension of the vector space spanned by its rows. We can find the rank using reducing to its row echelon form. Consider the matrix A below:
```math
$$A = \begin{bmatrix}
1 & 2 & 1 \\
-2 & -3 & 1 \\
3 & 5 & 0
\end{bmatrix}$$
```
We can put this in reduced row-echelon form by using the following elementary row operations:
```math
$$\begin{align*}
\begin{bmatrix}
1 & 2 & 1 \\
-2 & -3 & 1 \\
3 & 5 & 0
\end{bmatrix} 
&\xrightarrow{\text{2$R_1+R_2 \to R_2$}}
\begin{bmatrix}
1 & 2 & 1 \\
0 & 1 & 3 \\
3 & 5 & 0
\end{bmatrix} 
&\xrightarrow{\text{-3$R_1+R_3 \to R_3$}}
\begin{bmatrix}
1 & 2 & 1 \\
0 & 1 & 3 \\
0 & -1 & -3
\end{bmatrix} \\
&\xrightarrow{\text{$R_2+R_3 \to R_3$}}
\begin{bmatrix}
1 & 2 & 1 \\
0 & 1 & 3 \\
0 & 0 & 0
\end{bmatrix} 
&\xrightarrow{\text{-2$R_2+R_1 \to R_1$}}
\begin{bmatrix}
1 & 0 & 5 \\
0 & 1 & 3 \\
0 & 0 & 0
\end{bmatrix} 
\end{align*}$$
```
The final matrix (in row echelon form) has two non-zero rows and thus the rank of matrix A is 2.


