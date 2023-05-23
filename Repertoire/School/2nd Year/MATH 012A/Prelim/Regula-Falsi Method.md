## Definition
- Calculates the new solution estimate as the x-intercept of the line segment joining the endpoints of the function on the current bracketing interval
- Root is being approximated by the actual function by a line segment on the bracketing interval and then using classical double false position formula on that line segment

## Derivation
$y-f(b_n)=\frac{f(b_n)-f(a_n)}{b_n-a_n}(x-b_n)$

$\frac{f(b_n)-f(a_n)}{b_n-a_n}(c_n-b_n)+f(b_n)=0$

$c_n=b_n-f(b_n)\frac{b_n-a_n}{f(b_n)-f(a_n)}$

$x_n=b_n-f(b_n)\frac{b_n-a_n}{f(b_n)-f(a_n)}$

## Algorithm

**Step 1:** Find points $a$ and $b$ such that $a<b$ and $f(a)*f(b)<0$

**Step 2:** If $f(x_n)=0$ then $x_n$ is an exact root, else if $f(a)*f(x_2)<0$ then $b=x_2$, else if $f(b)*f(x_2)<0$ then $a=x_2$

**Step 3:** If $f(x_n)=0$ then $x_n$ is an exact root, else if $f(a)*f(x_2)<0 b=x_2$, else if $f(b) f(x_2)<0$ then $a=x_2$

**Step 4:**  Repeat step 2 and 3 until $f(x_n)=0$ or $|f(x_n)| ≤ DOA$

## Example

$f(x)=x^3-x-1$

$|f(x_n)|≤0.001$

### Solution

$x$

$0$

$1$

$2$

$f(x)$

$-1$

$-1$

$5$

******************************First Iteration******************************

$a=1$

$b=2$

$x_1=b-f(b)\frac{b-a}{f(b)-f(a)}$

$x_1=2-(5)\frac{2-1}{(5)-f(-1)}$

$x_1=1.166666667$

Thus,

$f(x_1)=(1.166666667)^3-(1.166666667)-1=-0.578703736934$

Since $f(x_1)$ is negative. Hence $a=x_1$

**Second Iteration**

$a=1.166666667$

$b=2$

$x_2=2-(5)\frac{2-1.166666667}{(5)-(-0578703736934)}$

$x_2=1.253112035$

Thus,

$f(x_2)=(1.253112035)^3-(1.253112035)-1=-0.2853630237<0$

Since $f(x_2)$ is negative. Hence $a=x_2$

********************************Third Iteration********************************

$a=1.253112035$

$b=2$

$x_3=2-(5)\frac{2-1.253112035}{(5)-(-0.2853630237)}$

Thus,

$f(x_4)=(1.311281022)^3-(1.311281022)-1=-0.05658848596<0$

Since $$f(x_4) is negative. Hence $a=x_4$.

******************************Fifth Iteration******************************

$a=1.311281022$

$b=2$

$x_5=2-(5)\frac{2-1.311281022}{(5)-(-0.05658848596)}$

Thus,

$f(x_5)=(1.318988504)^3-(1.318988504)-1=-0.02430374661<0$

Since $f(x_5)$ is negative. Hence $a=x_5$

******************************Sixth Iteration******************************

$n$

$a$

$f(a)$

$b$

$f(b)$

$x_n$

$f(x_n)$

$1$

$1$

$-1$

$2$

$5$

$1.166666667$

$-0.578703736934$

$2$

$1.166666667$

$-0.578703736934$

$2$

$5$

$1.253112035$

$-0.2853630237$

$3$

$1.253112035$

$-0.2853630237$

$2$

$5$

$1.293437403$

$-0.1295420899$

$4$

$1.293437403$

$-0.129542089$

$2$

$5$

$1.311281022$

$-0.05658848596$

$5$

$1.311281022$

$-0.05658848596$

$2$

$5$

$1.318988504$

$-0.02430374661$

$6$

$1.318988504$

$-0.02430374661$

$2$

$5$

$1.322282718$

$-0.01036184982$

$7$

$1.322282718$

$-0.01036184982$

$2$

$5$

$1.323648294$

$-0.00403949777$

$8$

$1.323648294$

$-0.00403949777$

$2$

$5$

$1.324279462$

$-0.00186925833$

$9$

$1.324279462$

$-0.00186925833$

$2$

$5$

$1.324531987$

$⁍45$