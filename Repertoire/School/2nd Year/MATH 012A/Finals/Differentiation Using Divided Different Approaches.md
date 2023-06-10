## Recall
$\textrm{slope} = \frac{\textrm{rise}}{\textrm{run}}$

$\textrm{Percent Error} = \frac{|\textrm{True Value} - \textrm{Actual Value}|}{\textrm{True Value}}*100\%$

## Numerical Differentiation
Approximation of the derivative for a specific value of $x(x_i)$ by the **slope of the secant line** from values of $x$ close to $x$

### Three Approaches
**Forward Difference Approach (FDA)**
$\textrm{FDA} = \frac{f(x_i+i)-f(x_i)}{h}$

**Backward Difference Approach (BDA)**
$\textrm{BDA} = \frac{f(x_i)-f(x_i-1)}{h}$

**Centered Difference Approach**
$\textrm{CDA} = \frac{f(x_i+1)-f(x_i-1)}{2h}$

#### Note
$x_i+1=x_i+h$
$x_i-1=x_i-h$

## Example
By using FDA, BDA, and CDA; Estimate the first derivative.
$f(x) = e^{\frac{2}{3}*x}-x^2-1$ at $x_1=5.6$ with the step size of $h = 0.25$

### Values
$f(x) = e^{\frac{2}{3}*x}-x^2-1$
$x_1=5.6$
$h = 0.25$

Correct up to 4 Decimals

**True Value**
$f’(x)=\frac{2}{3}e^{\frac{2}{3}*x}-2x$
$f'(x)=\frac{2}{3}e^{\frac{2}{3}*5.6} - 2(5.6)$
$f’(x)=16.6788$

### FDA
$\textrm{FDA} = \frac{f(x_i+i)-f(x_i)}{h}$

**Solution**
$f'(x)=\frac{f(5.6+0.25)-f(5.6)}{0.25}$
$f'(x)=\frac{f(5.85)-f(5.6)}{0.25}$
$f'(x) = \frac{(e^{\frac{2}{3}(5.85)}-(5.85)^2-1)-(e^{\frac{2}{3}(5.6)}-(5.6)^2-1)}{0.25}$
$f’x(x)=18.8867$

**Percent Error**
$\textrm{Percent Error} = \frac{|16.6788-18.8867|}{16.6788}*100\%$
$\textrm{Percent Error} = 13.2378\%$

### BDA
$\textrm{BDA} = \frac{f(x_i)-f(x_i-1)}{h}$

**Solution**
$f'(x)=\frac{f(5.6)-f(5.6-0.25)}{0.25}$
$f'(x)=\frac{f(5.6)-f(5.35)}{0.25}$
$f'(x) = \frac{(e^{\frac{2}{3}(5.6)}-(5.6)^2-1)-(e^{\frac{2}{3}(5.35)}-(5.35)^2-1)}{0.25}$
$f’(x)=14.7295$

**Percent Error**
$\textrm{Percent Error} = \frac{|16.6788-14.7295|}{16.6788}*100\%$
$\textrm{Percent Error} = 11.687\%$

### CDA
$\textrm{CDA} = \frac{f(x_i+1)-f(x_i-1)}{2h}$

**Solution**
$f'(x)=\frac{f(5.6+0.25)-f(5.6-0.25)}{2(0.25)}$
$f'(x)=\frac{f(5.85)-f(5.35)}{2(0.25)}$
$f'(x) = \frac{(e^{\frac{2}{3}(5.85)}-(5.85)^2-1)-(e^{\frac{2}{3}(5.35)}-(5.35)^2-1)}{2(0.25)}$
$f’(x)=16.8081$

**Percent Error**
$\textrm{Percent Error} = \frac{|16.6788-16.8081|}{16.6788}*100\%$
$\textrm{Percent Error} = 0.77\%$