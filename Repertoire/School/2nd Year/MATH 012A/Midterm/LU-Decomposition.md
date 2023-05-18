****
## LU-Factorization

$\begin{bmatrix} a_{11} & 0 & 0\\ a_{21} & a_{22} & 0\\a_{31} & a_{32} & a_{33}\end{bmatrix}$ $\textrm{L}$

$\begin{bmatrix} a_{11} & a_{12} & a_{13}\\ 0 & a_{22} & a_{23}\\ 0 & 0 & a_{33} \end{bmatrix}$ $\textrm{U}$


> [!NOTE] Definition
> $A=LU$

## Example

$$ A = \begin{bmatrix} 1 & -3 & 0\\ 0 & 1 & 3\\ 2 & -10 & 2 \end{bmatrix} $$

Reduce $A$ to $U$ while keeping track of the **Elementary Matrices** used for each row operation

```start-multi-column
ID: ID_49v1
Number of Columns: 3
Largest Column: standard
```

**Matrix**

$U=\begin{bmatrix} 1 & -3 & 0\\ 0 & 1 & 3\\ 0 & -4& 2 \end{bmatrix}$

--- column-end ---

**Elementary Row Operation**
$-2R_1 + R_3 → R_3$

$-2$ in $a_{31}$

--- column-end ---

**Elementary Matrix**
$E_1 = \begin{bmatrix} 1&0&0\\ 0&1&0\\ -2&0&1\end{bmatrix}$

--- column-end ---

=== end-multi-column

```start-multi-column
ID: ID_49v2
Number of Columns: 3
Largest Column: standard
```

**Matrix**

$U=\begin{bmatrix} 1&-3&0\\ 0&1&3\\ 0&0&14\end{bmatrix}$

--- column-end ---

**Elementary Row Operation**

$4R_2+R_3→R_3$

$4$ in $a_{32}$

--- column-end ---

**Elementary Matrix**

$E_2=\begin{bmatrix} 1&0&0\\ 0&1&0\\ 0&4&1\end{bmatrix}$

--- column-end ---

=== end-multi-column

***Notice***

$L \thinspace \textrm{or} \thinspace E_1^{-1}E_2^{-1} = \begin{bmatrix} 1&0&0\\0&1&0\\2&0&1\end{bmatrix} \begin{bmatrix} 1&0&0\\0&1&0\\0&-4&1\end{bmatrix} =\begin{bmatrix} 1&0&0\\ 0&1&0\\ 2&-4&1\end{bmatrix}$

**Steps**

1.  Write $y=Ux$ and $Ly=b$ for $y$
2.  Solve $Ux=y$ for $x$

Conclusion: $Ax = LUx = Ly=b$

### Solve the Linear Equation

$x_1 - 3x_2 = -5\\ x_2 + 3x_3 = -1\\ 2x_1 - 10x_2 + 2x_3= -20\\$

**Get** $A$ **using Elementary Row Operations**

$A=\begin{bmatrix}1&-3&0\\0&1&3\\2&-10&2\end{bmatrix} =\begin{bmatrix}1&0&0\\0&1&0\\2&-4&1\end{bmatrix} \begin{bmatrix}1&-3&0\\0&1&3\\0&0&14\end{bmatrix}$

Let $y = Ux$ and $Ly=b$

$\begin{bmatrix} 1&0&0\\ 0&1&0\\ 2&-4&1\end{bmatrix} \begin{bmatrix} y_1\\ y_2\\ y_3\end{bmatrix}= \begin{bmatrix} -5\\-1\\-20\end{bmatrix}$

$Ly=b$

### Back-Substitution

First Variable
$y_1=-5$

Second Variable
$y_2=-1$

Third Variable
$2y_1-4y_2+y_3=-20$
$y_3 = -20-2(-5)+4(-1)$
$y_3=-14$

Conclusion
$y=\begin{bmatrix} -5\\-1\\-14\end{bmatrix}$

### Solve for $Ux=y$

$\begin{bmatrix} 1&-3&0\\0&1&3\\0&0&14 \end{bmatrix} \begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}=\begin{bmatrix}-5\\-1\\-14\end{bmatrix}$

$Ux=y$

### Back-Substitution

Third Variable
$14x_3=-14$
$\frac{14x_3}{14}=\frac{-14}{14}$
$x_3=-1$

Second Variable
$x_2+3x_3=-1$
$x_2+3(-1)=-1$
$x_2-3=-1$
$x_2=2$

First Variable
$x_1-3x_2=-5$
$x_1-3(2)=-5$
$x_1-6=-5$
$x_1=1$

Conclusion
$x=\begin{bmatrix} 1\\2\\-1\end{bmatrix}$