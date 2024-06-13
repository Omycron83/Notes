Der **Kern** einer [[Lineare Abbildungen|linearen Abbildung]] $ker F = F^{-1} := \{v \in V : F(v) = o \in W\}$ ist die Menge aller Vektoren $\in V$ der [[Abbildungen|Abbildung]] $F: V \rightarrow W$ die auf den Nullvektor abgebildet werden.

# Eigenschaften:
## $ker F$ ist ein Untervektorraum:
$ker \; F \subset W$ ist ein [[Untervektorräume|Untervektorraum]]  von $V$.
	Beweis: Untervektorraumsaxiome abklappern
	1. $F(o) = o \implies o \in ker \; F$
	2. $F(v), F(w) = o \implies F(v) + F(w) = F(v + w) = o$ 
	3. $\lambda F(v) = o \implies  \lambda F(v) = F(\lambda v) = o$ 
## $F$ injektiv $\Leftrightarrow kerF = \{o\}$ 

^f1cf24

$F$ [[Abbildungen#^4b4823|injektiv]] $\Leftrightarrow$ $ker \; F = \{o \}$ 
	Beweis:  ^683b21
	1. Die 'hin' Richtung sei trivial
	2. Nehma man an, der Kern besteht nur aus dem Nullvektor, d.h. es wenn $v \neq v'$ dann gibt es keine $v - v' = o$. Dann ist $F(v - v') \neq o \Leftrightarrow F(v) - F(v') \neq o \Leftrightarrow F(v) \neq F(v')$ $\square$


