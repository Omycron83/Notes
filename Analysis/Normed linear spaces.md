### Intuition through metric spaces:
A normed linear space is a subset of a [[Metric Spaces|Metric Space]] that is also a [[Vektorraum|Vector Space]]. 
### Formal definition:
A normed linear space is a pair of objects $(V, || \;||)$ where the norm $|| \; || : V \times V \rightarrow R$ satisfies:
1. $|| x - y || \ge 0$
2. $||x - y || = 0 \implies x = y$
3. $||\lambda(x - y)|| = |\lambda| \, || x -  y||$ 
4. $||x - z|| \le ||x - z|| + ||y - z||$

See that the third property also implies the third property for metrix spaces: lets assume $\lambda = -1$ , then $||\lambda (x - y) || =  ||-1 (x - y) || =  ||y - x || = |1| || x - y ||$

### $L_1$ and $L_2$ norms:
$L_1 : V  \rightarrow R, L_1(x) = || x ||_1$ is defined as: $||x||_1 = \sum_1^n |x_i|$ 
$L_1 : V  \rightarrow R, L_2(x) = || x ||_2$ is defined as: $||x||_2 = \sqrt{\sum_1^n x_i^2}$ 