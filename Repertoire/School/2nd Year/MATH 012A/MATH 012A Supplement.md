# Module 1

> [!TIP]
> Find the interval where $x_i-x_{i-1} ≤ 0.0001$
> $x_0 = \frac{x_i - x_{i -1}}{2}$

## Errors and Error Analysis

## Fixed-Point Iterations

$f(x) = x^3 - x - 1$

Rewrite into $x = \sqrt[3]{x+1}$

**Table**
$n$, $x_{n-1}$, $x_n$, $|x_i - x_{i-1}|$

## Newton-Raphson Method
### Find the Root
**Query**
$f(x) = 3x^3 + 2x^2 + x - 1$

**Find the derivative**
$f’(x) = 3x^2 + 4x + 1$

**Find Next Iteration**
$x_n = x_{n - 1} - \frac{f(x_{n - 1})}{f’(x_{n - 1})}$

**Target**
$|f(x_n)| ≤ 0.0001$

**Solution**

| $x$    | $0$  | $1$ |
| ------ | ---- | --- |
| $f(x)$ | $-1$ | $3$    |

**Table**
$n$, $x_n - 1$, $f(x_n - 1)$, $f’(x_n - 1)$, $x_n$
___
# Module 2

## Bisection Method
$x = x_1 - f(x_1)[\frac{x_1 - x_0}{f(x_1) - f(x_0)}]$

$n$, $x_{n - 2}$, $f(x_{n - 2})$, $x_{n - 1}$, $f(x_{n - 1})$, $x_n$, $f(x_n)$

## Regula-Falsi Method

## Graeffe’s Root-Squaring Method
**Descarte’s Rule of Signs**
Count number of positive signs from $f(x)$

Count number of negative signs from $f(-x)$

**Graeffe’s Root-Squaring Method**
1. Split polynomial
2. Factor out polynomial
3. Let $x^2 = y$
4. Simplify
5. Find Roots: $|\frac{a_i}{a_i - 1}|^\frac{1}{2^m}$

___
# Module 3

## Gaussian and Gauss-Jordan Eliminations
- $R_x$ ↔ $R_y$
- $R_y$ → $nR_x + R_y$
- $nR_y$

## LU-Decomposition

___
# Module 4

## Jacobi and Gauss-Seidel Method

## Newton-Raphson Method for Non-Linear
Find determinant

### Recall
2x2 Matrix = $ad-cb$

3x3 Matrix
Use Basket Method and Co-Factor

### Solution
**Next Iteration**
$x_1 = x_0 + h$
$y_2 = y_0 + h$

$f(x_0 + h_1, y_0 + h_1) = 0$
$g(x_0 + h_1, y_0 + k_1) = 0

**Equate to Zero**
$f(x_0+h_1,y_0+h_1)=0$
$g(x_0+h_1,y_0+k_1)=0$

**Acquire partial derivative of $f(x_0,y_0)$ and $g(x_0,y_0)$**
$f(x_0,y_0)+h(\frac{\partial f}{\partial x}) = 0$
$g(x_0,y_0)+h(\frac{\partial f}{\partial x}) = 0$

$f_0 + h(f_x)_0+k(f_y)_0=0$
$g_0+h(g_x)_0+k(f_y)_0=0$

**Get determinants of $D$, $D_x$, and $D_y$**
$D=\begin{bmatrix}(f_x)_0&(f_y)_0\\(g_x)_0&(g_y)_0\end{bmatrix}$
$D_x=\begin{bmatrix}f_0 & (f_y)_0 \\ g_0&(g_y)_0\end{bmatrix}$
$D_y=\begin{bmatrix} (f_x)_0&f_0\\(g_x)_0&g_0\end{bmatrix}$

___
# Module 5

## Differentiation Using Divided Different Approaches

## Trapezoidal and Simpson’s Rule of Numerical Integrations