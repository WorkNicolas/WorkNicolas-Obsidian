## Linear Equations

```start-multi-column
ID: ID_yr2c
Number of Columns: 2
Largest Column: standard
```

**Equation of the Line in 2D Space**


$a_1 x + a_2 y = b$

**Constants**: $a_1, a_2, \textrm{and} \thinspace b$


--- column-end ---

**Equation of the Line in 3D Space**


$a_1 x + a_2 y + a_3 z = b$

Constants: $a_1, a_2, a_3, \textrm{and} \thinspace b$


--- column-end ---

=== end-multi-column

## Parametric Representation

**Example 1:** $x_1+2x_2=4$

$x_1=4-2x_2$

let $x_2=t$ $\in \mathbb{R}$

$x_1=4 - 2t$ $\in \mathbb{R}$

$x_2=t$

**Example 2:** $3x=3-2y+z$

$3x = 3-2y+z$

$x=1-\frac{2}{3}y = \frac{1}{3}z$

let $z = t$ and $y = s$

$x = 1 - \frac{2}{3}s+\frac{1}{3}t$; $s, t \in \mathbb{R}$

## System of Linear Equations

$a_{12} x_1+a_{21} x_2 + a_{31} x_3 … a_{n1} x_n = b_1$

$a_{12} x_1+a_{22} x_2 + a_{32} x_3 … a_{n2} x_n = b_2$

$a_{13} x_1+a_{23} x_2 + a_{33} x_3 … a_{n3} x_n = b_3$

$a_{1n} x_1+a_{2n} x_2 + a_{3n} x_3 … a_{mn} x_n = b_1$

### Number of Solutions of a System of Linear Equations

**Independent System**
The system has exactly one solution

**Consistent/Dependent System**
The system has infinitely many solutions

**Inconsistent System**
The system has no solution   

## Definition of Matrices

$$ \begin{bmatrix} a_{11} & a_{12} & a_{13} & ... & a_{1n} \\ a_{21} & a_{22} & a_{23} & ... & a_{2n}\\ a_{31} & a_{32} & a_{33} & ... & a_{3n}\\ ... & ... & ... & ... & ...\\ a_{m1} & a_{m2} & a_{m3} & ... & a_{mn} \end{bmatrix} $$

- If $m * n$ are positive then it is a rectangular array
- Denote by capital letters
- Used to represent systems of linear equations

**Augmented Matrix**

Matrix derived from the coefficient and constant terms of a system of linear equations.

**Coefficient Matrix**

Matrix containing only the coefficients of the system

### Example

**System**

$$ x - 4y + 3z = 5\\ -x + 3y - z = -3\\ 2x - 4z = 6\\ $$

**Augmented Matrix**

$$ \begin{bmatrix} 1 & -4 & 3 & 5\\ -1 & 3 & -1 & -3\\ 2 & 0 & -4 & 6\\ \end{bmatrix} $$

**Coefficient Matrix**

$$ \begin{bmatrix} 1 & -4 & 3\\ -1 & 3 & -1\\ 2 & 6 & -4\\ \end{bmatrix} $$

## Gaussian and Gauss-Jordan Elimination

**Procedure**

1. Write the augmented matrix of the system of linear equations
2. Use elementary row operations to rewrite the matrix in row-echelon form
3. Write the system of linear equations corresponding to the matrix in row-echelon form and use back-substitution

**Row Operations**

- $R_x$ ↔ $R_y$
- $R_y$ → $nR_x + R_y$
- $nR_y$

**Solve the System**

$x_2 + x_3 - 2x_4 = -3$
$x_1 + 2x_2 - x_3 =2$
$2x_1 + 4x_2 + x_3 - 3x_4 = -2$
$x_1 -4x_2 - 7x_3 - x_4 = -19$

**Augmented Matrix**

$$ \begin{bmatrix} 0 & 1 & 1 & -2 & -3\\ 1 & 2 & -1 & 0 & 2\\ 2 & 4 & 1 & -3 & -2\\ 1 & -4& -7 & -1 & -19\\ \end{bmatrix} $$

**Column 1**

$\begin{bmatrix} 1 & 2 & -1 & 0 & 2\\ 0 & 1 & 1 & -2 & -3\\ 2 & 4 & 1 & -3 & -2\\ 1 & -4 & -7 & -1 & -19\\ \end{bmatrix}$

$R_1$ ↔ $R_2$

$\begin{bmatrix} 1 & 2 & -1 & 0 & 2\\ 0 & 1 & 1 & -2 & -3\\ 0 & 0 & 3 & -3 & -6\\ 1 & -4 & -7 & -1 & -19 \end{bmatrix}$

$-2R_3 + R_3$ → $R_3$

$\begin{bmatrix} 1 & 2 & -1 & 0 & 2\\ 0 & 1 & 1 & -2 & -3\\ 0 & 0 & 3 & -3 & -6\\ 0 & -6 & -6 & -1 & -21\\ \end{bmatrix}$

$6R_2 + R_4$ → $R_4$


**Column 2**

$\begin{bmatrix} 1 & 2 & -1 & 0 & 2\\ 0 & 1 & 1 & -2 & -3\\ 0 & 0 & 3 & -3 & -6\\ 0 & 0 & 0 & -13 & -39\\ \end{bmatrix}$

$6R_2 + R_4$ → $R_4$

**Column 3**

$\begin{bmatrix} 1 & 2 & -1 & 0 & 2\\ 0 & 1 & 1 & -2 & -3\\ 0 & 0 & 1 & -1 & -2\\ 0 & 0 & 0 & -13 & -39\\ \end{bmatrix}$

$-\frac{1}{3} R_3$ → $R_3$

**Column 4**

$\begin{bmatrix} 1 & 2 & -1 & 0 & 2\\ 0 & 1 & 1 & -2 & -3\\ 0 & 0 & 1 & -1 & -2\\ 0 & 0 & 0 & 1 & 3\\ \end{bmatrix}$

$-\frac{1}{13}R_4$ → $R_4$

### Back-Substitution

First Variable
$x_1 = 2x_2 - x_3 = 2\\x_2 + x_3 - 2x_4 = -3\\x_3 - x_4 = -2\\x_4 = 3$

$x_1 = -1$

$x_1 = 2 - 2(2) + 1$

Second Variable
$x_2 = 2$

$x_2 = -3 - 1 + 2(3)$

Third Variable
$x_3 = 1$

$x_3 = -2 - 3$

Fourth Variable
$x_4=3$

## Gauss-Jordan Elimination

**Lower**

$\begin{bmatrix} 1 & -2 & 3 & 9\\ 0 & 1 & 3 & 5\\ 0 & -1 & -1 & -1\\ \end{bmatrix}$

$2R_2 + R_1$ → $R_1$

$\begin{bmatrix} 1&-2&3&9\\ 0&1&3&5\\ 0&0&2&4 \end{bmatrix}$

$R_2 + R_3$ → $R_3$

$\begin{bmatrix} 1 & -2 & 3 & 9\\ 0 & 1 & 3 & 5\\ 0 & 0 & 1 & 2\\ \end{bmatrix}$

$\frac{1}{2}R_3$ → $R_3$

**Upper**

$\begin{bmatrix} 1&0&9&19\\ 0&1&3&5\\ 0&0&1&2\\ \end{bmatrix}$

$2R_2 + R_1$ → $R_1$

$\begin{bmatrix} 1 & 0 & 9 & 19\\ 0 & 1 & 0 & -1\\ 0 & 0 & 1 & 2\\ \end{bmatrix}$

$-3R_3 + R_2$ → $R_2$

$\begin{bmatrix} 1 & 0 & 0 & 1\\ 0 & 1 & 0 & -1\\ 0 & 0 & 1 & 2\\ \end{bmatrix}$

$-9R_3 + R_1$ → $R_1$