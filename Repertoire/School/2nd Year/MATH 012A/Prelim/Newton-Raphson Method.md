### Definition
- Named after Isaac Newton and Joseph Raphson
- Root-finding algorithm which produces successively better approximations to the roots (or zeroes) of a real-valued function
- Most efficient root-finding algorithm available
- Converges quadratically, i.e. error is approximately proportional to the square of the previous error

## Algorithm
**Step 1:** Find $a$ and $b$ such that $a < b$ and $f(a) * f(b) < 0$

**Step 2:** Take the interval $[a,b]$, find the next value

### Example
Find the root of the polynomial
$f(x) = x^3 + 2x^2 + x - 1$

Find the derivative
$f’(x) = 3x^2 + 4x + 1$

Target
$|f(x_n)| ≤ 0.0001$

**Solution**

| $x$    | $0$  | $1$ |
| ------ | ---- | --- |
| $f(x)$ | $-1$ | $3$    |

$x_0 = \frac{0 + 1}{2} = 0.5$

#### Interval
$[-1, 3]$

**1st Iteration**
Find $f(x)$
$f(0.5) = (0.5)^3 + 2(0.5)^2 + (0.5) - 1 = 0.125$

Find $f’(x)$
$f’(0.5) = 3(0.5)^2 + 4(0.5) + 1 = 3.75$

Find $x_1 = x_0 - \frac{f(x_0)}{f’(x_0)}$
$x_1 = 0.5 - \frac{0.125}{3.75} = 0.466666667$

**2nd Iteration**
$f(0.466666667) = (0.466666667)^3 + 2(0.466666667)^2 + (0.466666667) - 1 = 0.00385185$

$f’(0.466666667) = 3(0.466666667)^2 + 4(0.466666667) + 1 = 3.52$

$x_2 = 0.466666667 - \frac{0.00385185}{3.52} = 0.46557239$

**3rd Iteration**
$f(0.46557239) = (0.46557239)^3 + 2(0.46557239)^2 + (0.46557239) - 1 = 0.00000407$

#### Table
| $n$ | $x_{n - 1}$     | $f(x_n - 1)$ | $f’(x_{n - 1})$ | $x_n$         |     |
| --- | ------------- | ------------ | ------------- | ------------- | --- |
| $1$ | $0.5$         | $0.125$      | $3.75$        | $0.466666667$ |     |
| $2$ | $0.466666667$ | $0.00385185$ | $3.52$        | $0.46557239$  |     |
| $3$ | $0.46557239$  | $0.00000407$ | N/A           | N/A              |     |

Since  $0.00000407 < 0.0001$ thus, $0.46557239$ is the one possible real root.

### Example 2
Find the root of an equation
$f(x) = 2 \cos x - x$

Find the derivative
$f’(x) = -2 \sin x - 1$

Target
$|f(x_n)| ≤ 0.0001$

#### Interval
$[1, 2]$

$x_0 = \frac{1 + 2}{2} = 1.5$

**1st Iteration**
$f(x) = 2 \cos (1.5) - 1.5 = -1.3585256$

$f’(x) = -2 \sin (1.5) - 1 = 2.99498997$

$x_1 = 1.5 - \frac{-1.3585256}{2.99498997} = 1.04640062$

**2nd Iteration**
$f(x) = 2 \cos (1.04640062) - 1.04640062 = -0.04502061$

$f’(x) = 2 \sin (1.04640062) - 1 = -2.73125333$

$x_2 = 1.04640062 - \frac{-0.04502061}{-2.73125333} = 1.02991712$

**3rd Iteration**
$f(x) = 2 \cos (1.02991712) - 1.02991712 = -0.00013733$

$f’(x) = 2 \sin (1.02991712) - 1 = -2.71451264$

$x_3 = 1.02991712 - \frac{-0.00013733}{-2.71451264} = 1.02986653$

**4th Iteration**
$f(1.02986653) = 2 \cos (1.02986653) - 1.02986653 = -0.0000000018397$

#### Table
| $n$ | $x_{n - 1}$  | $f(x_{n - 1})$     | $f’(x_{n - 1})$ | $x_n$        |
| --- | ------------ | ------------------ | --------------- | ------------ |
| $1$ | $1.5$        | $-1.3585256$       | $-2.99498997$   | $1.04640062$ |
| $2$ | $1.04640062$ | $-0.04502061$      | $-2.73125333$   | $1.02991712$ |
| $3$ | $1.02991712$ | $-0.00013733$      | $-2.71451264$   | $1.02986653$ |
| $4$ | $1.02986653$ | $-0.0000000018397$ | N/A             | N/A             |

Since $|-0.0000000018397| < 0.0001$ thus, $1.02986653$ is a possible root.