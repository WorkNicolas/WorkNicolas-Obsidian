## Recall
### Partial Derivative
$f(x,y)=2x^2y+4y^2$
$\frac{\partial f}{\partial x} = 2y*2x+0=4xy$
$\frac{\partial f}{\partial y} = 2x^2+8y$

### Determinants
$2x2 \thinspace \textrm{Matrix}$
$A = \begin{bmatrix} a & b\\c&d\end{bmatrix} = ad-cb$
$3x3 \thinspace \textrm{Matrix}$
$B = \begin{bmatrix}a&b&c\\d&e&f\\g&h&i\end{bmatrix}$
**Basket Method and Co-factor**
$B=\begin{bmatrix}a&b&c&a&b\\d&e&f&d&e\\g&h&i&g&h\end{bmatrix} = aei+bfg+cdb-[gec-hfa-idb]$

## Solutions of Simultaneous Non-Linear Equation Using Newton-Raphson Method
**Non-Linear Equation**
$ax_1 + bx_2 + cx_3 + … + kx_n$
$ay_1 + by_2 + cy_3 + … + ky_n$

**Initial Approximation**
$(x_0,y_0)$

### Next Iteration
$x_1=x_0+h$
$y_2=y_0+h$
$f(x_0+h_1,y_0+h_1)=0$
$g(x_0+h_1,y_0+k_1)=0$

### Steps
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

## Example
### 1st Iteration
$4x^2+2xy+y^2=30$
$2x^2+3xy+y^2=3$
$(x_0,y_0)=-3,2$

**Equate to 0**
$f(x_0,y_0)=4x^2+2xy+y^2-30$
$g(x_0,y_0)=2x^2+3xy+y^2-3$

**Get Partial Derivative**
$f_x=8x+2y$
$f_y=2x+2y$
$g_x=4x+3y$
$g_y=3x+2y$

**Get $(f_x)_0$, $(f_y)_0$, $(g_x)_0$, $(g_y)_0$ by Substitution**
$f_x(-3,2)=8(-3)+2(2)=-20$
$f_y(-3,2)=2(-3)+2(2)=-2$
$g_x(-3,2)=4(-3)+3(2)=-6$
$g_y(-3,2)=3(-3)+2(2)=-5$

$f(-3,2)=4(-3)^2+2(-3)(2)+(2)^2-30=-2$
$g(-3,2)=2(-3)^2+3(-3)(2)+(2)^2-3=1$

**Substitute $D$, $D_x$, and $D_y$**
$D=\begin{bmatrix}(f_x)_0&(f_y)_0\\(g_x)_0&(g_y)_0\end{bmatrix}=\begin{bmatrix}-20&-2\\-6&-5\end{bmatrix}=88$
$D_x=\begin{bmatrix}f_0&(f_y)_0\\g_0&(g_y)_0\end{bmatrix}=\begin{bmatrix}-2&-2\\1&-5\end{bmatrix}=12$
$D_y=\begin{bmatrix}(f_x)_0&f_0\\(g_x)_0&g_0\end{bmatrix}=\begin{bmatrix}-20&-6\\-2&1\end{bmatrix}=-32$

**Get $h$ and $k$**
$h_0=\frac{-D_x}{D}=\frac{-(12)}{88}=-0.136$
$k_0=\frac{-D_y}{D}=\frac{-(-32)}{88}=0.364$

**Get $x_1$ and $y_1$**
$x_1=x_0+h=-3+(-0.136)=-3.136$
$y_1=y_0+k=2+0.364=2.364$

$\epsilon < 0.001$

**Check by Substitution**
$f(x,y)=4(-3.136)^2+2(-3.136)(2.364)+(2.364)^2-30=0.099$
$g(x,y)=2(-3.136)^2+3(-3.136)(2.364)+(2.364)^2-3=0.017$

### 2nd Iteration
$(x_1,y_1)=(-3.136,2.364)$

**Get $(f_x)_1$, $(f_y)_1$, $(g_x)_1$, $(g_y)_1$ by Substitution**
$f_x(-3.136,2.364)=8(-3.136)+2(2.364)-20.36$
$f_y(-3.136,2.364)=2(-3.136)+2(2.364)=-1.544$
$g_x(-3.136,2.364)=4(-3.136)+3(2.364)=-5.452$
$g_y(-3.136,2.364)=3(-3.136)+2(2.364)=-4.68$

$f(-3.136,2.364)=4(-3.136)^2+2(-3.136)(2.364)+(2.364)^2-30=0.099$
$g(-3,2)=2(-3)^2+3(-3)(2)+(2)^2-3=0.017$

**Substitute $D$, $D_x$, and $D_y$**
$D=\begin{bmatrix}(f_x)_0&(f_y)_0\\(g_x)_0&(g_y)_0\end{bmatrix}=\begin{bmatrix}-20.36&-1.544\\-5.452&-4.68\end{bmatrix}=86.867$
$D_x=\begin{bmatrix}f_0&(f_y)_0\\g_0&(g_y)_0\end{bmatrix}=\begin{bmatrix}-0.099&--1.544\\0.017&-4.68\end{bmatrix}=-0.437$
$D_y=\begin{bmatrix}(f_x)_0&f_0\\(g_x)_0&g_0\end{bmatrix}=\begin{bmatrix}-20.36&-0.099\\-5.432&-0.017\end{bmatrix}=0.194$

**Get $h$ and $k$**
$h_1=\frac{-Dx}{D}=\frac{-(-0.437)}{86.867}=0.005$
$k_1=\frac{-D_y}{D}=\frac{-(0.194)}{86.867}=-0.002$

$x_2=x_1+h_1=-3.136+0.005=-3.131$
$y_2=y_1+h_1=2.364-0.002=2.362$

**Check by Substitution**
$f(-3.131,2.362)=4(-3.131)^2+2(-3.131)(2.362)+(2.362)^2-30=0.001$
$g(-3.131,2.362)=2(-3.131)^2+3(-3.131)(2.362)+(2.362)^2-3=-0.009$

Since $\epsilon >0.001$ thus, $(x,y)=(-3.131,2.362)$

