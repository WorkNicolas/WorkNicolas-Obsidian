## Algorithm
**Step 1:** Find $a$ and $b$ such that $a < b$ and $f(a) * f(b) < 0$

**Step 2:** Take the interval $[a,b]$, find the next value

### Example
Find the root of the polynomial
$f(x) = x^3 + 2x^2 + x - 1$

$f’(x) = 3x^2 + 4x + 1$

$|f(x_n)| ≤ 0.0001$

**Solution**

| $x$    | $0$  | $1$ |
| ------ | ---- | --- |
| $f(x)$ | $-1$ | $3$    |

**1st Iteration**

#### Table
| $n$ | $x_n - 1$  | $f(x_n - 1)$ | $f’(x_n - 1)$ | $x_n$       |
| --- | ---------- | ------------ | ------------- | ----------- |
| $1$ | $0.5$        | $0.125$        | $3.75$          | $0.466666667$ |
| $2$ | $0.466666667$ | $0.00385185$         | $3.52$    | $0.46557239$            |            |
