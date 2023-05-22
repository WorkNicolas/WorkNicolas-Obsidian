## Algorithm
**Step 1:** Find points $x_0$ and $x_1$ such that $x_0 < x_1$ and $f(x) * f(x_1) < 0$

**Step 2:** Take the interval $[x_0, x_1]$ and find next value $x_2 = x_1 - f(x_1)[\frac{x_1 - x_0}{f(x_1) - f(x_0)}]$

**Step 3:** If $f(x_2) = 0$ then $x_2$ is an exact else $x_0 = x_1$ and $x_1 = x_2$

**Step 4:** Repeat **step 2** and **step 3** until $f(x_n) = 0$ or $|f(x_n)| ≤ DOA$

### Example
Find the root of the polynomial function
$f(x) = x^5 - 3x^4 - 2x^3 - 2x - 5$

Target
$|f(x_n)|≤0.0001$

#### Formula
$$x = x_1 - f(x_1)[\frac{x_1 - x_0}{f(x_1) - f(x_0)}]$$

**Solution**

| $x$    | $0$  | $1$   | $2$   | $3$   | $4$ |
| ------ | ---- | ----- | ----- | ----- | --- |
| $f(x)$ | $-5$ | $-11$ | $-41$ | $-65$ | 115 |

**1st Iteration**

**2nd Iteration**

**3rd Iteration**

**4th Iteration**

**5th Iteration**

#### Table
| $n$ | $x_{n - 2}$ | $f(x_{n - 2})$ | $x_{n - 1}$ | $f(x_{n - 1})$ | $x_n$ | $f(x_n)$