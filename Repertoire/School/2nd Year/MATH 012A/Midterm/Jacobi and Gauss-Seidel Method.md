# The Jacobi Method
## History
-   Named after **Carl Gustav Jacob Jacobi** (1804-1851)

### Assumption
$a_{11}x_1+a_{12}x_2+…+a_{1n}x_n = b_1$

$a_{21}x_1+a_{22}x_2+…+a_{2n}x_n=b_2$

$a_{n1}x_1+a_{n2}x_2+…+a_{nn}=b_n$

**Solution**
$x_1 = \frac{1}{a_{11}}(b_1 - a_{12}x_2 - a_{13}x_3 - … - a_{1n}x_n)$

$x_2 = \frac{1}{a_{22}}(b_2 - a_{21}x_1 - a_{23}x_3 - … - a_{2n}x_n)$

$x_3 = \frac{1}{a_{33}}(b_3 - a_{31}x_1 - a_{32}x_2 - … - a_{3n}x_n)$

**Properties**
- One unique solution
- Coefficient matrix $A$ has no zeros on its main diagonal
- If any of the diagonal entries $a_{11}, a_{22}, … , a_{nn}$ are zero then rows or columns must be interchanged to obtain a coefficient matrix that has nonzero entries

### Method
**Step 1:** Arrange the given System of Linear Equation in diagonally dominant ways

**Step 2:** Isolate one unknown in each of the equation

**Step 3:** Initialize a value for the unknowns of zero

**Step 4:** Perform iteration until the value of the unknowns don’t diverge anymore

### Example 1
$5x_1 - 2x_2 + 3x_3 = -1$
$-3x_1 + 9x_2 + x_3 = 2$
$2x_1 - x_2 - 7x_3 = 3$

$|a_{11}| > |a_{12}| + |a_{13}|$
$|a_{22}| > |a_{21}| + |a_{23}|$
$|a_{33}| > |a_{31}| + |a_{32}|$

Rewrite into this form
$x_1 = -\frac{1}{5} + \frac{2}{5}x_2 - \frac{2}{5}x_3$
$x_2 = \frac{2}{9}+\frac{3}{9}x_1-\frac{1}{9}x_3$
$x_3=-\frac{3}{7}+\frac{2}{7}x_1-\frac{1}{7}x_2$

Initial Approximation
$x_1 = 0$
$x_2 = 0$
$x_3 = 0$

**1st Iteration**
$x_1 = -\frac{1}{5} + \frac{2}{5}(0) - \frac{2}{5}(0) = -0.200$
$x_2 = \frac{2}{9}+\frac{3}{9}(0)-\frac{1}{9}(0) = -0.222$
$x_3=-\frac{3}{7}+\frac{2}{7}(0)-\frac{1}{7}(0)$

**2nd Iteration**

#### Table
| $n$   | $0$   | $1$    | $2$   | $3$   | $4$   | $5$   | $6$   | $7$   |
| ----- | ----- | ------ | ----- | ----- | ----- | ----- | ----- | ----- |
| $x_1$ | $0.000$ | $-0.200$ | $0.146$ | $0.192$ | $0.181$ | $0.185$ | $0.186$ | $0.186$ |
| $x_2$  |       |        |       |       |       |       |       |       |

# Gauss-Seidel Method
## History
- Named after **Carl Friedrich Gauss**(1777-1855) and **Philip L. Seidel** (1821-1896)

**1st Iteration**
$x_1 = -\frac{1}{5} + \frac{2}{5}(0) - \frac{2}{5}(0) = -0.200$
$x_2 = \frac{2}{9}+\frac{3}{9}(-0.200)-\frac{1}{9}(0) = 0.156$
$x_3=-\frac{3}{7}+\frac{2}{7}(-0.200)-\frac{1}{7}(0.156)$

**2nd Iteration**

#### Table