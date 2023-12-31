Eine Kombination ist eine **ungeordnete** **Auswahl von k Objekten** aus einer Menge von $n$ Objekten, mit oder ohne Wiederholung. 

## Ohne Wiederholung:
Die Anzahl an Kombinationen von $k$ aus $n$ Objekten ohne Wiederholung ist 
$\frac{n!}{(n - k)! \cdot k!} = \binom{n}{k}$. 

Beweis:
	
## Mit Wiederholung:
Die Anzahl an Kombinationen von $k$ aus $n$ Objekten mit Wiederholung ist
$\frac{(n + k - 1)!}{(n - 1)! \cdot k!}$.

Beweis:
	

## Eigenschaften:

### $\binom{n}{0} = \binom{n}{n} = 1$:
Beweis:
$\binom{n}{0} = \frac{n!}{n! \cdot 0!} = \frac{n!}{0! \cdot n!} = \binom{n}{n} = 1$
### $\binom{n}{k} = \binom{n}{n - k}$:
Beweis:
$\binom{n}{k} = \frac{n!}{(n - k)! \cdot k!} = \frac{n!}{k! \cdot (n - k)!} = \binom{n}{n - k}$
### $\binom{n}{k} + \binom{n}{k + 1} = \binom{n + 1}{k + 1}$:
Beweis:
z.Z.: $\binom{n}{k} + \binom{n}{k + 1} = \binom{n + 1}{k + 1} = \frac{(n + 1)! }{(n - k)! \cdot (k + 1)!}$
$\binom{n}{k} + \binom{n}{k + 1} = \frac{n!}{(n - k)! \cdot k!} + \frac{n!}{(n - k - 1)! \cdot (k + 1)!}$
$= \frac{n!}{(n - k)! \cdot k!} + \frac{n!}{ \frac{(n - k)!}{(n - k)} \cdot (k + 1)!}$
$= \frac{n!}{(n - k)! \cdot k!} + \frac{n! (n - k)}{(n - k)! \cdot (k + 1)!}$
$= \frac{n!(k + 1) + n!(n - k)}{(n - k)! \cdot (k + 1)!}$
$= \frac{n!(n + 1)}{(n - k)! \cdot (k + 1)!}$
$= \frac{(n + 1)!}{(n - k)! \cdot (k + 1)!}$
$= \binom{n + 1}{k + 1} \; \square$
