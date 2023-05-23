## The Jacobi Method
### Assumption
$a_{11}x_1+a_{12}x_2+…+a_{1n}x_n = b_1$

$a_{21}x_1+a_{22}x_2+…+a_{2n}x_n=b_2$

$a_{n1}x_1+a_{n2}x_2+…+a_{nn}=b_n$

**Properties**
- One unique solution
- Coefficient matrix $A$ has no zeros on its main diagonal
- If any of the diagonal entries $a_{11}, a_{22}, … , a_{nn}$ are zero then rows or columns must be interchanged to obtain a coefficient matrix that has nonzero entries

### History
-   Named after _**********************************Carl Gustav Jacob Jacobi**********************************_ (1804-1851)

**Solution**
$x_1 = \frac{1}{a_{11}}(b_1 - a_{12}x_2 - a_{13}x_3 - … - a_{1n}x_n)$

$x_2 = \frac{1}{a_{22}}(b_2 - a_{21}x_1 - a_{23}x_3 - … - a_{2n}x_n)$

$x_3 = \frac{1}{a_{33}}(b_3 - a_{31}x_1 - a_{32}x_2 - … - a_{3n}x_n)$

### Assumption
$(x_1, x_2, x_3, …, x_n)$

**Substitute**
Substitute the values of $x$ into the right-hand side of the equation