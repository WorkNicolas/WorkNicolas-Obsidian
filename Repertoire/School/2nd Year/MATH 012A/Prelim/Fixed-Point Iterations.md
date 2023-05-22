### Definition
- Known as **One-point iteration** or **Successive Substitution**
- Formula for iterative algorithm can be derived by re-arranging the function $f(x) = 0$
- Converges linearly

### Algorithm
**Step 1:** Write the equation to $x=g(x)$

**Step 2:** Find points $a$ and $b$ such that $a < b$ and $f(a) * f(b) < 0$

**Step 3:** $x_1 = g(x_0) \newline x_2 = g(x_1) \newline x_3 = g(x_2) \newline ...\newline$

Repeat **step 2** and **step 3** until $|x_i - x_{i-1}| \cong 0$

### Example 1

**Query:** $f(x) = x^3 - x - 1$

$|x_i - x_{i-1}| \leq 0.0001$

**Solution:** Finding the interval

| $x$    | $0$   | $1$   | $2$   |
| ------ | --- | --- | --- |
| $f(x)$ | $-1$  | $-1$  | $5$    |

#### Interval
$[1,2]$

Since $f(1) <5$ and $f(1) * f(2) < c$

#### Interval $x_0$ Solution
$x_0 = \frac{1+2}{2} = 1.5$

#### Method 1

Let $x^3-x-1=0$

$x^3 = x + 1$

$x = \sqrt[3]{x+1}$

**1st Iteration**
$x_1 = g(x_0) = \sqrt[3]{1.5 + 1} = 1.35720881$

**2nd Iteration**
$x_2 = g(x_1) = \sqrt[3]{1.35720881 + 1} = 1.33086096$

**3rd Iteration**
$x_3 = g(x_2) = \sqrt[3]{1.33086096 + 1} = 1.32588377$

**4th Iteration**
$x_4 = g(x_3) = \sqrt[3]{1.32588377 + 1} = 1.32493936$

**5th Iteration**
$x_5 = g(x_4) = \sqrt[3]{1.32493936 + 1} = 1.32476001$

**6th Iteration**
$x_6 = g(x_5) = \sqrt[3]{1.32476001 + 1} = 1.32472595$

#### Table

| $n$ | $x_{n-1}$ | $x_n$ | $∣x_i - x_{i - 1}∣$ |
| --- | --- | --- | --- |
| $1$ | $1.5$ | $1.35720881$ | $0.14279119$ |
| $2$ | $1.35720881$ | $1.33086096$ | $0.02634785$ |
| $3$ | $1.33086096$ | $1.32588377$ | $0.00497718$ |
| $4$ | $1.32588377$ | $1.32493936$ | $0.00094441$ |
| $5$ | $1.32493936$ | $1.324760001$ | $0.00017935$ |
| $6$ | $1.32476001$ | $1.32472595$ | $0.00003401$ |

$|x_i - x_{i-1}| = 0.00003401 < 0.0001$

$1.32472595$

#### Method 2

**Query:** $x^3 - x - 1 = 0$

$x = \frac{1}{x^2-1}$

$x_0 = \frac{1 + 2}{2} = 1.5$

**1st Iteration**
$x_1 = g(x_0) = \frac{1}{(1.5)^2 - 1} = 0.8$

**2nd Iteration**
$x_2 = g(x_1) = \frac{1}{(0.8)^2 - 1} = -2.77778$

**3rd Iteration**
$x_3 = g(x_2) = \frac{1}{(-2.77778)^2 - 1} = 0.1489$

**4th Iteration**
$x_4 = g(x_3) = \frac{1}{(0.1489)^2 - } = -1.02267$

### Example 2
**Query:** $e^{-x} * 3 \ln x = 0$

$e^{-x} = 3$

$x = g(x) = e^{(e^{-\frac{x}{3}})}$

#### Assumption
$x_0 = 2$

**1st Iteration**
$x_1 = g(x_0) = e^{(e^{-\frac{2}{3}})} = 1.046144772$

**2nd Iteration**
$x_2 = g(x_1) = e^{(e^{-\frac{1.046144772}{3}})} = 1.124227891$

**3rd Iteration**
$x_3 = g(x_2) = e^{(e^{-\frac{1.124227891}{3}})} = 1.11438321$

**4th Iteration**
$x_4 = g(x_3) = e^{(e^{-\frac{1.11438321}{3}})} = 1.115577861$

**5th Iteration**
$x_5 = g(x_4) = e^{(e^{-\frac{1.115577861}{3}})} = 1.115432194$

#### Table
| $n$ | $x_n - 1$     | $x_n$          | $∣x_i - x_{i - 1}∣$ |
| --- | ------------- | -------------- | ------------------- |
| $1$ | $2$           | $1.046144772$  | $0.95538552284$     |
| $2$ | $1.046144772$ | $1.124227891$  | $0.078083119411$    |
| $3$ | $1.124227891$ | $1.11438321$   | $0.009844680935$    |
| $4$ | $1.11438321$  | $1.1155778611$ | $0.001194651313$    |
| $5$ | $1.115577861$ | $1.115432194$  | $0.000145667133$                    |

Since $|x_i - x_{i-1} = 0.000145667133 < 0.001$ thus, $1.115432194$ is the real root.