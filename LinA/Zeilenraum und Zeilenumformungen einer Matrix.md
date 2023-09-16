# Zeilenraum:

^7a07fe

Der Zeilenraum $ZR(A)$ einer [[Matrix]] $A \in K^{m \times n}$ ist das Erzeugniss der Zeilen $a_i$ von $A$, also $span(a_1, ..., a_n)$, also alle möglichen Linearkombinationen der Zeilenvektoren (wenn [[Matrizen#^2d573a|als Vektorraum interpretiert]]).
# Zeilenumformungen:

^6ef525

Es gibt zwei elementare Zeilenumformungen, die den Zeilenraum erhalten:
#### Typ 1: Zeilenmultiplikation mit $\lambda \neq 0$:
Die $i$'te Zeile wird mit einem Skalar multipliziert. Man schreibt $A \rightarrow A_1$
Beweis Zeilenraumerhaltung:
	$span(a_1, ..., a_m) = \mu_1 a_1 + ... + \mu_i a_i + ... + \mu_m a_m$
	Setzt man nun $\lambda a_i$ ein, so kann man im Fall $\lambda \neq 0$ einfach $\hat{\mu}_i := \frac{\mu_i}{\lambda}$ setzen, sodass
	$\mu_1 a_1 + ... + \hat{\mu}_i (\lambda a_i) + ... + \mu_m a_m = span(a_1, ..., a_m)$ die Linearkombinationen wieder übereinstimmen.
Das bedeuted, dass $ZR(A) = ZR(A_1)$.
#### Typ 2: Addition zweier Zeilen:
Die $j$'te Zeile wird auf die $i$'te Zeile aufaddiert. Man schreibt $A \rightarrow A_2$
Beweis Zeilenraumerhaltung:
$span(a_1, ..., a_m) = \mu_1 a_1 + ... + \mu_j a_j + ... +\mu_i a_i + ... + \mu_m a_m$
	Setzt man nun $a_j + a_i$  ein, so kann man $\hat{\mu}_i_ := 
	So ist $\mu_1 a_1 + .... + \mu_j a_j + ... + \hat{\mu}_i (a_i + a_j) + ... \mu_m a_m = span(a_1, ..., a_m)$ 
	und die Linearkombinationen stimmen überein.
Das bedeuted, dass $ZR(A) = ZR(A_2)$.

#### Typ 3: Addition zweier Zeilen:
Das vielfache der $j$'ten Zeile $\lambda a_j$ wird auf die $i$'te Zeile addiert. 
Beweis Zeilenraumerhaltung:
	Der Beweis folgt daraus, dass $ZR(A) = ZR(A_1)$ und $ZR(A) = ZR(A_2)$ wodurch trivial $ZR(A_3) = ZR(A)$ gilt.

#### Typ 4: Vertauschungen zweier Zeilen:
Die $j$'te Zeile wird mit der $i$'ten Zeile vertauscht.
Beweis Zeilenraumerhaltung:
	Der Beweis ist trivial, da die Linearkombination reihenfolgeninvariant ist.
