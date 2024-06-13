Pardé-Approximizations are the Taylor-Series-Equivalent in approximating functions by rational polynomials, which consist of a polynomial of degree $M$ divided by a polynomial of degree $N$. The usual advantage is a better approximation as the distance to the approximated point grows large, as the function doesn't have a limit in infinity, but rather in a real number.
It is convention to let $B_0 = 1$ 
## Constructing a Padé Approximation
1. Find the Taylor-Polynomial of degree $N + M$ for the function: $P_{N + M}(x) = c_0 + c_1x + c_2 x^2 + ... + c_{N + M}x^{N + M}$  
2. Equate that too the rational function $P^N_M (x) = \frac{A_0 + A_1 x + A_2 x^2 + ... + A_Nx^n}{1 + B_1x + B_2 x^2 + ... + B_M x^M} = P_{N + M}(x)$
3. Solve for the numerator by multiplying out the denominator with the Taylor-Approximation, where we can ignore any terms larger than $x^{N + M}$ [1] and have, with the order higher than $N$, the numerator-polynomial equal to 0
4. Solve the resulting equations, where there are $N + M$ equations and $N + M$ unknowns

### Example: Approximating $sin(x)$ at $x = 0$ by a $M = 6$, $N = 2$ Padé:

Lets first construct the Taylor series by figuring out the derivative values at $x = 0$ for the 0'th to 8'th derivative, which are, luckily, easy to calculate as most are sine (thus equating to 0) and the rest being cosine with alternating signs:
$P_{8} = 0 + x - 0 - \frac{x^3}{3} + 0 + \frac{x^5}{5} - 0 - \frac{x^7}{7}$

Now, we can let:
$x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7} = \frac{A_0 + A_1 x + A_2x^2 + A_3 x^3 + A_4 x^4 + A_5 x^5 + A_6 x^6}{1 + B_1 x + B_2 x^2}$ 

Further, we multiply this out:

$A_0 + A_1 x + A_2 x^2 + A_3 x^3 + A_4 x^4 + A_5 x^5 + A_6 x^6 = (x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7}) (1 + B_1 x + B_2 x^2)$ 
$\Leftrightarrow ... = (x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7}) + (x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7})B_1 x + (x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7}) B_2 x^2$
$\Leftrightarrow ... = ... + B_1x^2 - \frac{B_1 x^4}{3} + \frac{B_1 x^6}{5} - \frac{B_1 x^8}{7} + B_2x^3 - \frac{B_2 x^5}{3} + \frac{B_2 x^7}{5} - \frac{B_2 x^9}{7}$ 

Now, we can drop the higher order terms:
$\Leftrightarrow ... = ... + B_1x^2 - \frac{B_1 x^4}{3} + \frac{B_1 x^6}{5} - \frac{B_1 x^8}{7} + B_2x^3 - \frac{B_2 x^5}{3} + \frac{B_2 x^7}{5}$ 

This yields us the following system of equations:
$A_0 = 0$
$A_1 = 1$
$A_2 = B_1$
$A_3 = \frac{-1}{3} + B_2$
$A_4 = \frac{-B_1}{3}$
$A_5 = \frac{1}{5} - \frac{B_2}{3}$
$A_6 = \frac{B_1}{5}$
$0 = \frac{-1}{7} + \frac{B_2}{5} (= A_7)$
$0 = - \frac{B_1}{7} (= A_8)$ 

Now, we have a system of 8 equations with 8 unknowns. 
We get the value of $B_1$ as $0$ and the value of $B_2$ as $\frac{5}{7}$ from the bottom equations.
This means that:
$A_2 = 0$
$A_3 = \frac{-1}{3} + \frac{5}{7} = \frac{8}{21}$
$A_4 = 0$
$A_5 = \frac{1}{5} - \frac{1}{7} = \frac{2}{35}$
$A_6 = 0$.

Thus, we yield the rational polynomial:
$P^N_M(x) = \frac{x + \frac{8}{25}x^3 + \frac{2}{35}x^5}{1 + \frac{5}{7}x^2}$ 

Lets finally plot $sin(x)$, the Taylor approximation and the Padé approximation:
![[Pasted image 20230813163819.png]]
<span style="color:red">rot = sin(x) </span>, <span style="color:green">grün = Taylor </span>, <span style="color:blue">blau = Padé </span>


[1] as those will be encapsulated in the error or "Restglied"