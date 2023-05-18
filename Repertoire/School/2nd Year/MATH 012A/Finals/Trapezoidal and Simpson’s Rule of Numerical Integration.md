## Trapezoidal Rule
Rule that evaluates the area under the curve by dividing the total area into trapezoids.


Let $f(x)$ be a continuous function on the interval $[a,b]$. Divide the interval $[a,b]$ into $n$ equal subintervals with each of the width.

$n = \frac{b-a}{n}$, such that $a = x_0 < x_1 < x_2 < … < x_n = b$

Then, the trapezoidal rule formula for the area between the curve $f(x)$ and the x-axis can be obtained by approximating the definite integral.

$\int_a^b f(x) dx \cong T_n = \frac{h}{2} [f(x_0)+2f(x_1)+2f(x_2)+...2f(x_n-1)+f(x_n)$

### Example
Approximate the area under the curve $y=f(x)$ between $x=0$ and $x=8$ using the trapezoidal rule with $n=4$ subintervals. A function $f(x)$ is given in the table values.

| **$x$**    | $0$ | $2$ | $4$  | $6$ | $8$ |
| ---------- | --- | --- | ---- | --- | --- |
| **$f(x)$** | $3$ | $7$ | $11$ | $9$ | $3$    |

$h = \frac{8-0}{4} = 2$

$T_n = \frac{2}{2}[3 + 2(7)+2(11)+2(9) + 3]$
$T_n = 3 + 14 + 22 + 18 + 3$
$T_n = 60$

Calculate $\int_0^10 x^2ax$ by the trapezoidal rule using 10 intervals.

$h=\frac{10-0}{10}=1$


| **$x$**      | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   | 10  |
| ------------ | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **$f(x^2)$** | 0   | 1   | 4   | 9   | 16  | 25  | 36  | 49  | 64  | 81  | 100    |

$T_n = \frac{1}{2}[0 + 2(1) + 2(4) + 2(9) + 2(16) + 2(25) + … + 2(81) + 100]$
$T_n = 335$
