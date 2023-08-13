Pardé-Approximizations are the Taylor-Series-Equivalent in approximating functions by rational polynomials, which consist of a polynomial of degree $M$ divided by a polynomial of degree $N$. The usual advantage is a better approximation as the distance to the approximated point grows large, as the function doesn't have a limit in infinity, but rather in a real number.
It is convention to let $B_0 = 1$ 
## Constructing a Padé Approximation
1. Find the Taylor-Polynomial of degree $N + M$ for the function: $P_{N + M}(x) = c_0 + c_1x + c_2 x^2 + ... + c_{N + M}x^{N + M}$  
2. Equate that too the rational function $P^N_M (x) = \frac{A_0 + A_1 x + A_2 x^2 + ... + A_Nx^n}{1 + B_1x + B_2 x^2 + ... + B_M x^M} = P_{N + M}(x)$
3. Solve for the numerator by multiplying out the denominator with the Taylor-Approximation, where we can ignore any terms larger than $x^{N + M}$ [1]
4. Solve the resulting equations, where there are $N + M$ equations and $N + M$ unknowns


[1] as those will be encapsulated in the error or "Restglied"