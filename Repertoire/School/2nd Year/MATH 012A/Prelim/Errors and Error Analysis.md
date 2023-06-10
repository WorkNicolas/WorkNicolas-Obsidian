## Errors
- Difference between exact values obtained using **analytical methods** and **approximate values** calculated using numerical methods

### Analytical Methods
- Superior to numerical methods
- **Approximate values** are always interpreted and treated depending on *how close they are to the value*

## Error Analysis
### Numerical Methods
- Approximate the *exact solution* of the problem using a *numerical method*, and consequently an error is committed

### Numerical Error
- The difference between the exact solution and the approximate solution

## Source of Error in Numerical Computations
### Blunder (Gross Error)
- Human errors
- Caused by human mistakes and oversight
- Can be minimized
- Will add to the total error of the underlying problem and significantly affect the accuracy of the solution

### Modeling Error
- Arise during the modeling process when scientists ignore effecting factors in the model
- Known as **formulation errors**

### Data Uncertainty
- Uncertainty of the physical problem data
- Known as **data errors**

### Discretisation Error
- Computers represent a function of continuous variable by several discrete values
- Scientists approximate and replace complex continuous problems with discrete ones

## Error Formulas
- $x$ is the exact solution
- $x^*$ is the approximate solution
- $e$ denotes the error

### Numerical Error
$e = x - x^*$

### Absolute Error
$ê = |e| = |x-x^*|$

### Relative Error
$ẽ = \frac{ẽ}{|x|} = \frac{x-x^*}{|x|}, \thinspace x \not= 0$

## Example
### Example 1
$x = 3.14159265389793$ is the value of the constant ratio $\pi$

$x^*=3.14159265$ is the approximation of $x$

### Quantities
**Error**
$e = x - x^* = 3.14159265389793 - 3.12159265 = 3.589792907376932*10^9$

**Absolute Error**
$ê = |e| = |x-x^*| = |3.14159265389793 - 3.12159265| = 3.589792907376932*10^9$

**Relative Error**
$ẽ = \frac{ẽ}{|x|} = \frac{x-x^*}{|x|} = \frac{3.589792907376932*10^9}{3.14159265389793} = 1.142666571770530*10^9$

### Example 2
As a newly hired employee, you were asked by your boss to measure the length of a bridge and a rivet. The measured values of the bridge and the rivets are 9999 cm and 9 cm, respectively. If the true values are 10000 cm and 10 cm respectively, will you decide to report these measurements to your boss already or will you measure the lengths again?

**Solution**

| **Material** | **Measured Values** | **True Value** | **$E_T$** | **%$E_R$%**                                     |
| ------------ | ------------------- | -------------- | --------- | ---------------------------------------- |
| Bridge       | 9999 cm             | 10000 cm       | 1 cm      | $│\frac{10000-9999}{10000}│ * 100%=0.01%$ |
| Rivet        | 9 cm                | 10 cm          | 1 cm      | $│\frac{10-9}{10}│ * 100% = 10%$ |                                         |

## Accuracy
Refers to how close a computed or measured value agrees with the true value

## Precision
Refers to how closely individual computed or measured values agree with each other

## Roundoff Error and Truncation Errors
1. $x_1= 1.34579$
2. $x_2 = 1.34679$
3. $x_3 = 1.34479$
4. $x_4 = 3.34379$
5. $x_5 = 2.34579$

### Example 3
**Rounding**
1. $x_1 = 1.35$
2. $x_2 = 1.35$
3. $x_3 = 1.34$
4. $x_4 = 3.34$
5. $x_5 = 2.35$

**Chopping**
1. $x_1 = 1.34$
2. $x_2 = 1.34$
3. $x_3 = 1.34$
4. $x_4 = 3.34$
5. $x_5 = 2.34$