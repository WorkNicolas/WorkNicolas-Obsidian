# Module 1

> [!TIP]
> Find the interval where $x_i-x_{i-1} ≤ 0.0001$
> $x_0 = \frac{x_i - x_{i -1}}{2}$

## Errors and Error Analysis

| **Keywords**          | **Definition**                                                                                                     |
| --------------------- | ------------------------------------------------------------------------------------------------------------------ |
| Analytical Methods    | **Approximate values** are always interpreted and treated depending on *how close they are to the value*           |
| Numerical Methods     | Approximate the *exact solution* of the problem using a *numerical method*, and consequently an error is committed |
| Numerical Error       | The difference between the exact solution and the approximate solution                                             |
| Blunder (Gross Error) | Human errors                                                                                                       |
| Modeling Error        | Known as **formulation errors**                                                                                    |
| Data Uncertainty      | Known as **data errors**                                                                                           |
| Discretization Error  | Scientists approximate and replace complex continuous problems with discrete ones                                  |
| Accuracy              | Refers to how close a computed or measured value agrees with the true value                                        |
| Precision             | Refers to how closely individual computed or measured values agree with each other                                                                                                                   |

### Formula
**Error**
$e = x - x^* = 3.14159265389793 - 3.12159265 = 3.589792907376932*10^9$

**Absolute Error**
$ê = |e| = |x-x^*| = |3.14159265389793 - 3.12159265| = 3.589792907376932*10^9$

**Relative Error**
$ẽ = \frac{ẽ}{|x|} = \frac{x-x^*}{|x|} = \frac{3.589792907376932*10^9}{3.14159265389793} = 1.142666571770530*10^9$

## Fixed-Point Iterations
### Definition
- Known as **One-point iteration** or **Successive Substitution**
- Formula for iterative algorithm can be derived by re-arranging the function $f(x) = 0$
- Converges linearly

$f(x) = x^3 - x - 1$

Rewrite into $x = \sqrt[3]{x+1}$

Target
$|x_i - x_{i-1}| \leq 0.0001$

**Table**
$n$, $x_{n-1}$, $x_n$, $|x_i - x_{i-1}|$

## Newton-Raphson Method
### Definition
- Named after Isaac Newton and Joseph Raphson
- Root-finding algorithm which produces successively better approximations to the roots (or zeroes) of a real-valued function
- Most efficient root-finding algorithm available
- Converges quadratically, i.e. error is approximately proportional to the square of the previous error

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

## Secant Method
### Definition
- Similar to the bisection method
- Divides each interval by the secant line connecting the endpoints
- Always converges to a root of $f(x) = 0$ provided that $f(x)$ is continuous $[a,b]$ and $f(a) * f(x) < 0$

Target
$|f(x_n)|≤0.0001$

**Formula**
$$x_{n} = x_{n-1} - f(x_{n-1})[\frac{x_{n-1} - x_{n-2}}{f(x_{n-1}) - f(x_{n-2})}]$$
**Table**
$n$, $x_{n - 2}$, $f(x_{n - 2})$, $x_{n - 1}$, $f(x_{n - 1})$, $x_n$, $f(x_n)$
___
# Module 2

## Bisection Method
### Definition
- Root-finding method that applies to any continuous functions for which one knows two values with opposite signs
- Consists of repeatedly bisecting the interval defined by these values and then selecting the sub-interval in which the function changes sign, and therefore must contain a root

## Regula-Falsi Method
### Definition
- Calculates the new solution estimate as the x-intercept of the line segment joining the endpoints of the function on the current bracketing interval
- Root is being approximated by the actual function by a line segment on the bracketing interval and then using classical double false position formula on that line segment

### Derivation
$y-f(b_n)=\frac{f(b_n)-f(a_n)}{b_n-a_n}(x-b_n)$

$\frac{f(b_n)-f(a_n)}{b_n-a_n}(c_n-b_n)+f(b_n)=0$

$c_n=b_n-f(b_n)\frac{b_n-a_n}{f(b_n)-f(a_n)}$

$x_n=b_n-f(b_n)\frac{b_n-a_n}{f(b_n)-f(a_n)}$

### Formula
$$x_n=b_n-f(b_n)\frac{b_n-a_n}{f(b_n)-f(a_n)}$$
Substitute $f(x_n)$

**Table**
$n$, $a$, $f(a)$, $b$, $f(b)$, $x_n$, $f(x_n)$

## Graeffe’s Root-Squaring Method
**Descarte’s Rule of Signs**
Count the number of positive signs from $f(x)$

Count the number of negative signs from $f(-x)$

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
### Jacobi Method
#### History
- Named after **Carl Gustav Jacob Jacobi** (1804-1851)

## Newton-Raphson Method for Non-Linear
### Partial Derivative
$f(x,y)=2x^2y+4y^2$
$\frac{\partial f}{\partial x} = 2y*2x+0=4xy$
$\frac{\partial f}{\partial y} = 2x^2+8y$

### Determinants
Find Determinants
$2x2 \thinspace \textrm{Matrix}$
$A = \begin{bmatrix} a & b\\c&d\end{bmatrix} = ad-cb$
$3x3 \thinspace \textrm{Matrix}$
$B = \begin{bmatrix}a&b&c\\d&e&f\\g&h&i\end{bmatrix}$
**Basket Method and Co-factor**
$B=\begin{bmatrix}a&b&c&a&b\\d&e&f&d&e\\g&h&i&g&h\end{bmatrix} = aei+bfg+cdb-[gec-hfa-idb]$

### Solution
**Non-Linear Equation**
$ax_1 + bx_2 + cx_3 + … + kx_n$
$ay_1 + by_2 + cy_3 + … + ky_n$

**Initial Approximation**
$(x_0,y_0)$

**Next Iteration**
$x_1 = x_0 + h$
$y_2 = y_0 + h$

$f(x_0 + h_1, y_0 + h_1) = 0$
$g(x_0 + h_1, y_0 + k_1) = 0$

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
### Recall
$\textrm{slope} = \frac{\textrm{rise}}{\textrm{run}}$

$\textrm{Percent Error} = \frac{|\textrm{True Value} - \textrm{Actual Value}|}{\textrm{True Value}}*100\%$

### Definition
Approximation of the derivative for a specific value of $x(x_i)$ by the **slope of the secant line** from values of $x$ close to $x$

### Three Approaches
**Forward Difference Approach (FDA)**
$\textrm{FDA} = \frac{f(x_i+i)-f(x_i)}{h}$

**Backward Difference Approach (BDA)**
$\textrm{BDA} = \frac{f(x_i)-f(x_i-1)}{h}$

**Centered Difference Approach**
$\textrm{CDA} = \frac{f(x_i+1)-f(x_i-1)}{2h}$

## Trapezoidal and Simpson’s Rule of Numerical Integrations
### Definition
Rule that evaluates the area under the curve by dividing the total area into trapezoids.

Let $f(x)$ be a continuous function on the interval $[a,b]$. Divide the interval $[a,b]$ into $n$ equal subintervals with each of the width.

### Integration
$\int x^n d x= \frac{x^{n+1}}{n+1}+c$

$\int x^2 dx = \frac{x^{2+1}}{{2+1}}+c = \frac{x^3}{3} + c = \frac{1}{3}x^3 + c$

$\int \frac{1}{x^2} dx = \int x^{-2} dx = \frac{x^{-2+1}}{-2+1} + c$

$\int \frac{7}{x^4} dx = \int 7x^{-4}dx = \frac{7x^{-4+1}}{-4+1} + c = \frac{7x^{-3}}{-3} + c = \frac{-7}{3x^3} + c$

### Formula
$\int_a^b f(x) dx \cong T_n = \frac{h}{2} [f(x_0)+2f(x_1)+2f(x_2)+...2f(x_n-1)+f(x_n)$