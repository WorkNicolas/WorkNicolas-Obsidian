## Basic Differentiation Formula

| **Rule**                           | **Formula** |
| ---------------------------------- | ----------- |
| Constant Rule                      | $\frac{d}{dx}(c)=0$            |
| Power Rule                         | $\frac{d}{dx}(u)=du$            |
| Constant Multiple Rule             | $\frac{d}{dx}Cu=Cdu$            |
| Product Rule                       | $\frac{d}{dx}(u*v)=udv+vdu$            |
| Quotient Rule                      | $\frac{d}{dx}\frac{C}{u}=\frac{-Cdu}{u^2}$            |
| Identity Rule                      | $\frac{d}{dx}(x)=1$            |
| Sum and Difference Rule            | $\frac{d}{dx}(u+v-w)=du+dv-dw$            |
| Power Rule (Exponents)             | $\frac{d}{dx}(u^n)=nu^{n-1}du$            |
| Quotient Rule (Rational Functions) | $\frac{d}{dx}\frac{u}{v}=\frac{vdu-udv}{v^2}$            |
| Square Root Rule                                   | $\frac{d}{dx}\sqrt(u)=\frac{du}{2\sqrt(u)}$            |

## Chain Rule
$$ \frac{d}{dx}f[g(x)]=f'g(x)*g'(x) $$

### Sample
$y = (x^3+3)^5$
$u=x^3+3$
$du=3x^2$
$y=u^5$
$y’=5u^4du$
$y’=5(x^3+3)^4(3x^2)$
$y'=15x^2(x^3+3)^4$

## Implicit Differentiation
$x^3+y^3=4$
$3x^2+3y^2y’=0$
$3y^2y’=-3x^2$
$y’=\frac{-3x^2}{3y^2}$
$y’=\frac{-x^2}{y^2}$

## Differentiation of Logarithmic and Exponential Functions

| **Direct Differentiation**      | **Chain Rule Counterparts** | **Simplified** |
| ------------------------------- | --------------------------- | -------------- |
| $\frac{d}{dx}e^x=e^x$           | $\frac{d}{dx}e^u=e^u$                            | $e^u du$               |
| $\frac{d}{dx}\ln x=\frac{1}{x}$ | $\frac{d}{dx}\ln u=\frac{1}{u}$                            | $\frac{du}{u}$               |
| $\frac{d}{dx}a^x=a^x\ln a$      | $\frac{d}{dx}a^u=a^u\ln a$                            | $a^u \ln a (du)$               |
| $\frac{d}{dx}\log_a x = \frac{1}{x \ln a}$ | $\frac{d}{dx}\log_a u = \frac{1}{u \ln a}$                            | $\frac{du}{u \ln a}$               |

### Properties of Logarithmic and Exponential Functions
1. $n \ln u = \ln u^n$
Example: $3\ln 2 = \ln 2^3 = ln 8$

2. $\ln e^u=u$
Example: $\ln e^{x^{2}+2x+3} = x^2+2x+3$

3. $\ln(xy)=\ln x + \ln y$
Example:
$\ln (x + 3) + \ln (x-4)$
$\ln (x+3)(x-4)$

4. $\ln \frac{x}{y} = \ln x - \ln y$
Example: $\frac{\ln (x+3)}{\ln (x-4)} = \ln (x+3) - \ln (x-4)$

5. $e^{\ln u} = u$
Example: $e^{\ln x} = x$

## Differentiation of Trigonometric Functions

| **Direct Differentiation**            | **Chain Rule Counterparts** |
| ------------------------------------- | --------------------------- |
| $\frac{d}{dx} \sin x = \cos x$        | $du \cos u$                            |
| $\frac{d}{dx} \cos x = -\sin x$       | $-du \sin u$                            |
| $\frac{d}{dx} \tan x = \sec^2 x$      | $du \sec^2 u$                            |
| $\frac{d}{dx} \cot x = -\csc^2 x$     | $-du \csc^2 u$                            |
| $\frac{d}{dx} \sec x = \sec x \tan x$ | $du \sec u \tan u$                            |
| $\frac{d}{dx} \csc x = -\csc x \cot x$                                      | $-du \csc u \cot u$                            |

## Derivatives of Hyperbolic Functions

| **Direct Differentiation**                                                                 | **Chain Rule Counterparts**                         |
| ------------------------------------------------------------------------------------------ | --------------------------------------------------- |
| $\frac{d}{dx}\sinh x = \cosh x$                                                            | $du \cosh u$                                        |
| $\frac{d}{dx} \cosh x = \sinh x$                                                           | $du \thinspace \sinh u$                             |
| $\frac{d}{dx} \tanh x = \textrm{sech}^2 \thinspace x$                                      | $du \thinspace \textrm{sech}^2 \thinspace u$        |
| $\frac{d}{dx} \coth x = -\textrm{csch}^2 \thinspace x$                                     | $-du \thinspace \textrm{csch}^2 \thinspace u$       |
| $\frac{d}{dx} \thinspace \textrm{sech} \thinspace x = -\textrm{sech} \thinspace x \tan x$  | $-du \thinspace \textrm{sech} \thinspace u \tanh u$ |
| $\frac{d}{dx} \thinspace \textrm{csch} \thinspace x = -\textrm{csch} \thinspace x \coth x$ | $-du \thinspace \textrm{csch} \thinspace u \coth u$                                                    |

## Derivatives of Inverse Trigonometric

| **Direct Differentiation**                                | **Chain Rule Counterpart**     |
| --------------------------------------------------------- | ------------------------------ |
| $\frac{d}{dx} \sin^{-1} x = \frac{1}{\sqrt{1-x^2}}$       | $\frac{du}{\sqrt{1-u^2}}$      |
| $\frac{d}{dx} \cos^{-1} x = -\frac{1}{\sqrt{1-x^2}}$      | $-\frac{du}{\sqrt{1-u^2}}$     |
| $\frac{d}{dx} \tan^{-1} x = \frac{1}{1+x^2}$              | $\frac{du}{1+u^2}$             |
| $\frac{d}{dx} \sec^{-1} x = \frac{1}{｜x｜\sqrt{x^2-1}}$  | $\frac{du}{｜u｜\sqrt{u^2-1}}$ |
| $\frac{d}{dx} \cot^{-1} x = -\frac{1}{1+x^2}$             | $-\frac{du}{1+u^2}$            |
| $\frac{d}{dx} \csc^{-1} x = -\frac{1}{｜x｜\sqrt{x^2-1}}$ | $-\frac{du}{｜u｜\sqrt{u^2-1}}$                               |

## Derivatives of Inverse Hyperbolic Functions

| **Direct Differentiation**                                                               | **Chain Rule Counterpart** |
| ---------------------------------------------------------------------------------------- | -------------------------- |
| $\frac{d}{dx} \sinh^{-1} x = \frac{1}{\sqrt{1+x^2}}$                                     | $\frac{du}{\sqrt{1+u^2}}$  |
| $\frac{d}{dx} \cosh^{-1} x = \frac{1}{\sqrt{x^2-1}}$                                     | $\frac{du}{\sqrt{u^2-1}}$  |
| $\frac{d}{dx} \tanh^{-1} x = \frac{1}{1-x^2}$                                            | $\frac{du}{1-u^2}$         |
| $\frac{d}{dx} \thinspace \textrm{coth}^{-1} x = \frac{1}{1-x^2}$                         | $\frac{du}{1-u^2}$         |
| $\frac{d}{dx} \thinspace \textrm{sech}^{-1} \thinspace x = \frac{1}{x\sqrt{1-x^2}}$      | $\frac{du}{u\sqrt{1-u^2}}$ |
| $\frac{d}{dx} \thinspace \textrm{csch}^{-1} \thinspace x = -\frac{1}{｜x｜\sqrt{1+x^2}}$ | $\frac{du}{｜u｜\sqrt{1+u^2}}$                           |
