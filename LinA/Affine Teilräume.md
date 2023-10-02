Eine Teilmenge $X \subset V$ eines [[Vektorraum|Vektorraumes]] nennt man **affiner Teilraum**, falls es einen [[Untervektorräume|Unterraum]] $U$ von $V$ gibt, sodass $X = v + U$ für ein $v \in V$, also als [[Summen von Vektorräumen#^ea229e|modifizierte Summe]] dargestellt werden kann.

In der [[Faserung eines Vektorraumes]] haben wir gesehen, dass die Fasern einer linearen Abbildung affine Teilräume von $V$ sind, da sie als Summe des [[Kern einer linearen Abbildung|Kerns]] und eines [[Faser einer linearen Abbildung|Faserelementes]] darstellbar ist.

# Eigenschaften:
Sei $X = v + U = v' + U'$ ein affiner Teilraum von $V$. Dann gilt:
1. $v \in X, v' \in X$, $U = U'$ und außerdem $v - v' \in U$
Beweis:
	Die ersten beiden Aussagen folgen aus $o \in U$.
	Aus der ersten Aussage folgt dann, dass $v \in X \implies v = v' + u'$ sowie $v' \in X \implies v' = v + u$, sodass  $v' - v = u \in U$ und außerdem
	$v = v + u + u' \Leftrightarrow o = u + u' \Leftrightarrow u = -u' \Leftrightarrow u \in U, U' \Leftrightarrow U = U'$

2. $X = x + U \forall x \in X$:
Beweis:
	$x = v + u \forall x \in X \implies x + U = (v + u) + U = v + (u + U) = v+ U = X$ 

## Dimension affiner Teilräume:
Sei $X = v + U$ ein affiner Teilraum von $V$. Dann definiere man
$dim X := dim U$, wobei die wohldefiniertheit aus der ersten Eigenschaft hervorgeht. 

## Komplementäre Unterräume und affine Teilräume:
Seien $U, W$ Untervektorräume von V wobei $V = U \oplus W$. Dann schneidet jeder affine Unterraum $v + U, v \in V$ den komplementären Unterraum $W$ nur im Nullvektor.

Beweis:
	Aus $v \in V = U \oplus W$ wissen wir, dass $v + U = u + w + U = w + U = \{w + u | u \in U \}$ gilt. Nehme man nun an, dass $w + u \in W \implies u \in W \implies u = o$ nach der Definition der [[Direkte Summen|direkten Summe]]. 

# Beispiele:
1. Insbesondere ist jeder [[Untervektorräume|Unterraum]] selbst ein affiner Teilraum mit dem Nullvektor und sich selbst.

2. Betrachte man den $R^3$ über $R$: 
	- Jeder Punkt $M = \{(x, y, z)\}$ ist ein affiner Unterraum, da $M = (x, y, z) + \{o\}$ 
	- Jede Gerade $G = \{(g, p, l) + r \cdot (x, y, z) | r \in R \}$ ist ein affiner Unterraum mit dem Stützvektor und dem Untervektorraum des Richtungsvektors.
	- Jede Ebene $E = \{(g, p, l) + r\cdot (x, y, z) + s \cdot (u, i, e) | r,s \in R \}$ ist ein affiner Unterraum mit dem Stützvektor und dem Untervektorraum der Richtungsvektoren

