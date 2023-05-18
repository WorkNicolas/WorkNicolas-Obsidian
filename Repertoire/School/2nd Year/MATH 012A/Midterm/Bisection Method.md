## Definition

> [!NOTE] Idea
> $f(x) = 0$ is known to have a real root $x = c$ in an interval $[a,b]$

### Procedures
- Bisect the interval $[a,b]$
- Middle Point: $c=\frac{a+b}{2}$
- If $c$ is the root then the procedure has been concluded
- Otherwise, one of the intervals of $[a,c]$ or $[c,b]$ will contain the root
- Find one that contains the root and bisect again
- Continue the process of bisection until the root is trapped in an interval as small warranted by the desired currency (absolute error)


> [!NOTE] Intermediate Mean-Value Theorem
> Helps identify the interval in each iteration.
> 
> Let $f(x)$ be continuous function defined on $ [a,b]$ such that $f(a)$ and $f(b)$ are of opposite signs such that $f(a) * f(b) < 0$. Then, there is a root $x=c$ of $f(x)=0$ in $[a,b]$

## Example
$f(x)=2x^3-2x-5$

**Absolute Error < $0.001$

### Solution

Let $f(x) = 2x^3 - 2x - 5$

| $x$      | $0$    | $1$    | $2$   |
| ------ | ---- | ---- | --- |
| $f(x)$ | $-5$ | $-5$ | $7$    |

$[1,2]$

> [!NOTE] Note
> **Positive:** $b=c$
> **Negative:** $a=c$

**First Iteration**
$[1,2]$

$x_1=c=\frac{a+b}{2}=\frac{1+2}{2}=1.5$

$f(x_1)=f(1.5)=2(1.5)^3-2(1.5)-5=-1.25<0$

Since $f(x_1)$ is negative thus, $[1.5,2]$

**Second Iteration**
$[1.5,2]$

$x_2=\frac{a+b}{2}=\frac{1.5+2}{2}=1.75$

$f(x_2)=f(1.75)=2(1.75)^3-2(1.75)-5=2.21875$

Since $f(x_2)$ is positive thus, $[1.5,1.75]$

**Third Iteration**
$[1.5,1.75]$

$x_3=\frac{1.5+1.75}{2}=1.625$

$f(x_3)=f(1.625)=2(1.625)^3-2(1.625)-5=0.33203125$

Since $f(x_3)$ is positive thus, $[1.5,1.625]$

**Fourth Iteration**
$[1.5,1.625]$

$x_4=\frac{1.5+1.625}{2}=1.5625$

$f(x_4)=f(1.5625)=2(1.5625)^3-2(1.5625)-5=-0.49560547$

Since $f(x_4)$ is negative thus, $[1.5625,1.625]$

**Fifth Iteration**
$[1.5625,1.625]$

$x_5=\frac{1.5625+1.625}{2}=1.59375$

$f(x_5)=f(1.59375)=2(1.59375)^3-2(1.59375)-5=-0.09112549$

Since 