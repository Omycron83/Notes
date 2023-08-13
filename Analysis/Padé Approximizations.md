Pardé-Approximizations are the Taylor-Series-Equivalent in approximating functions by rational polynomials, which consist of a polynomial of degree $M$ divided by a polynomial of degree $N$. The usual advantage is a better approximation as the distance to the approximated point grows large, as the function doesn't have a limit in infinity, but rather in a real number.
It is convention to let $B_0 = 1$ 
## Constructing a Padé Approximation
1. Find the Taylor-Polynomial of degree $N + M$ for the function: $P_{N + M}(x) = c_0 + c_1x + c_2 x^2 + ... + c_{N + M}x^{N + M}$  
2. Equate that too the rational function $P^N_M (x) = \frac{A_0 + A_1 x + A_2 x^2 + ... + A_Nx^n}{1 + B_1x + B_2 x^2 + ... + B_M x^M} = P_{N + M}(x)$
3. Solve for the numerator by multiplying out the denominator with the Taylor-Approximation, where we can ignore any terms larger than $x^{N + M}$ [1]
4. Solve the resulting equations, where there are $N + M$ equations and $N + M$ unknowns

### Example: Approximating $sin(x)$ at $x = 0$ by a $M = 6$, $N = 2$ Padé:
Lets first construct the Taylor series by figuring out the derivative values at $x = 0$ for the 0'th to 8'th derivative, which are, luckily, easy to calculate as most are sine (thus equating to 0) and the rest being cosine with alternating signs:
$P_{8} = 0 + x - 0 - \frac{x^2}{2} + 0 + \frac{x^4}{4} - 0 - \frac{x^6}{6} + 0 + \frac{x^8}{8}$ 

Now, we can let:
$x - \frac{x^2}{2} + \frac{x^4}{4} - \frac{x^6}{6} + \frac{x^8}{8} = \frac{A_0 + A_1 x + A_2x^2 + A_3 x^3 + A_4 x^4 + A_5 x^5 + A_6 x^6}{1 + B_1 x + B_2 x^2}$ 

Further, we multiply this out:

$A_0 + A_1 x + A_2 x^2 + A_3 x^3 + A_4 x^4 + A_5 x^5 + A_6 x^6 = (x - \frac{x^2}{2} + \frac{x^4}{4} - \frac{x^6}{6} + \frac{x^8}{8} ) (1 + B_1 x + B_2 x^2)$ 
$\Leftrightarrow A_0 + A_1 x + A_2 x^2 + A_3 x^3 + A_4 x^4 + A_5 x^5 + A_6 x^6 = 


[1] as those will be encapsulated in the error or "Restglied"