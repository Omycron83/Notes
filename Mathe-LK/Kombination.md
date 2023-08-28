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

$\binom{n}{k} + \binom{n}{k + 1} = 