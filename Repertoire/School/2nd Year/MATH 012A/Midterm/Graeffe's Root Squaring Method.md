## Procedures

**Polynomial Equation**
$f(x)=x^n+a_1 x^{n-1}+a_2 x^{n-2}+...+a_{n-1} x+ a_n$

**Separation: Even and Odd Powers, Squaring**

$(x^n + a_2 x^{n-2} + a_4 x^{n-4}+…)^2 = a_1 x^{n-1} + a_3 x^{n-3} + a_5 x^{n-5} + …)^2$

**Substitute** $x^2=y$ **and Simplify**
$y^n+b_1 y^{n-1}+…+b_n=0$

$b_1=-a^2_1+2a^2$

$b_2 = a^2_2 - 2_{a_1 a_3} + 2_{a_4}$

$…$

$b_n = (-1)^n a^2_n$

**Roots of Equation 1**
$p_1, p_2, … p_n$

**Roots of Equation 2**
$p^2_1, p^2_2, …, p^2_n$

## Descartes’ Rule of Sign

**Given Polynomial Equation**
$f(x) = x^5+4x^4-3x^2+x-6$

**Coefficients of $f(x)$**
$1 + 4 - 3 + 1 - 6$

**Find Positive Zeros**
Positive → Positive → Negative → Positive → Negative

Number of Positive Zeros: 3 or 1, Odd

**Find Negative Zeros**

Find: $f(-x)$
$f(-x)=(-x)^5+4(-x)^4-3(-x)^2+(-x)-6$

$f(-x)=-x^5+4x^4-3x^2-x-6$

**Count Changes**
Negative → Positive → Negative → Negative → Negative

Number of Negative Zeros: 2 or 0, Even

## Sample

### Polynomial Equation
$x^3-6x^2+11x-6=0$

### Solution

**Descarte’s Rule of Sign**

Positive Real Roots: 3 or 1, Odd

$f(x)=x^3-6x^2+11x-6$

Positive → Negative → Positive → Negative

Negative Real Roots: 0

$f(-x)=-x^3-6x^2-11x-6$

Negative → Negative → Negative → Negative

**Graeffe’s Root-Squaring Method**

$i = 1$
****

$x^3+11x=6x^2+6$

$x(x^2+11)=6x^2+6$

$[x(x^2+11)]^2=[6x^2+6]^2$

$x^2(x^2+11)^2=(6x^2+6)^2$

let $x^2=y$

$y(y+11)^2=(6y+6)^2$

Simplify
$y^3-14y^2+49y-36=0$



$i=2$
****

$y^3+49y=14y^2+36$

$y(y^2+49)=14y^2+36$

$[y(y^2+49)]^2=[14y^2+36]^2$

$[y(y^2+49)]^2=[14y^2+36]^2$

$y^2(y^2+49)^2=(14y^2+36)^2$

let $y^2=z$

$z(z+49)^2=(14z+36)^2$

Simplify
$z^3-98z^2+1393z-1296=0$



$i=3$
****

$z^3+1393z=98z^2+1296$

$z(z^2+1393)=98z^2+1296$

$[z(z^2+1393)]^2=[98z^2+1296]^2$

$z^2(z^2+1393)^2=(98z^2+1296)^2$

let $z^2=u$

$u(u+1393)^2=(98u+1296)^2$

Simplify
$u^3-6818u^2+16864333u-1679616=0$



**Estimate**
$|\frac{a_i}{a{i-1}}|^{\frac{1}{2^m}}, i=1, 2, 3, ..., n$

$n$ is the degree of the polynomial

Required Roots: $x_1,x_2,x_3$

$m = 1$

Find Roots: $y^3-14y^2+49y-36=0$

$|x_1| = (\frac{14}{1})^{\frac{1}{2}} = 3.7417$

$|x_2| = (\frac{40}{14})^{\frac{1}{2}} = 1.8708$

$|x_3| = (\frac{39}{49})^{\frac{1}{2}}=0.85714$

$m = 2$

Find Roots: $z^3-98z^2+1393z-1296=0$

$|x_1| = (\frac{98}{1})^{\frac{1}{4}}=3.1463$

$|x_2|=(\frac{1393}{98})^{\frac{1}{4}}=1.9417$

$|x_3| = (\frac{1296}{1393})^{\frac{1}{4}}=0.9821$

$m=3$

Find Roots: $u^3-6818u^2+16864333u-1679616=0$

$|x_1|=(\frac{6818}{1})^{\frac{1}{8}}=3.0144$

$|x_2|=(\frac{1686433}{6818})^{\frac{1}{8}}=1.99143$

$|x_3| = (\frac{1679616}{1686433})^{\frac{1}{8}}=0.99949$

$x^3-6x^2+11x-6=0$

Exact Roots: $3, 2, 1$