Eine Teilmenge $X \subset V$ eines [[Vektorraum|Vektorraumes]] nennt man **affiner Teilraum**, falls es einen [[Untervektorräume|Unterraum]] $U$ von $V$ gibt, sodass $X = v + U$ für ein $v \in V$, also als [[Summen von Vektorräumen#^ea229e|modifizierte Summe]] dargestellt werden kann.

In der [[Faserung eines Vektorraumes]] haben wir gesehen, dass die Fasern einer linearen Abbildung affine Teilräume von $V$ sind, da sie als Summe des [[Kern einer linearen Abbildung|Kerns]] und eines [[Faser einer linearen Abbildung|Faserelementes]] darstellbar ist.

# Eigenschaften:
Sei $X = v + U = v' + U'$ ein affiner Teilraum von $V$. Dann gilt:
1. $v \in X, v' \in X$ und außerdem $v - v' \in U$
Beweis:
	Die ersten beiden Aussagen folgen aus $o \in U$.
	Die zweite Aussage folgt daraus, dass wenn $x = v + u = v' + u'$ dann $\Leftrightarrow 

# Beispiele:
1. Insbesondere ist jeder [[Untervektorräume|Unterraum]] selbst ein affiner Teilraum mit dem Nullvektor und sich selbst.

2. Betrachte man den $R^3$ über $R$: 
	- Jeder Punkt $M = \{(x, y, z)\}$ ist ein affiner Unterraum, da $M = (x, y, z) + \{o\}$ 
	- Jede Gerade $G = \{(g, p, l) + r \cdot (x, y, z) | r \in R \}$ ist ein affiner Unterraum mit dem Stützvektor und dem Untervektorraum des Richtungsvektors.
	- Jede Ebene $E = \{(g, p, l) + r\cdot (x, y, z) + s \cdot (u, i, e) | r,s \in R \}$ ist ein affiner Unterraum mit dem Stützvektor und dem Untervektorraum der Richtungsvektoren

