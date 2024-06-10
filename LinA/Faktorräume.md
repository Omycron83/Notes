Sei $V$ ein $K$-[[Vektorraum]] und $U$ ein [[Untervektorräume|Untervektorraum]] von $V$ sowie $\sim$ eine [[Relationen|Relation]] auf $V$, mit $v \sim v' \Leftrightarrow v - v' \in U$, sprich $v$ ist äquivalent zu $v'$ modulo $U$, d.h. es gibt ein $u \in U: u = v - v' \Leftrightarrow v = u + v'$ bzw. $v \in v' + U$ 

Das es sich um eine [[Relationen#^405c4f|Äquivalenzrelation]] handelt kann man leicht nachweisen:
$v - v = o \in U \forall v \in V$, also ist die Relation **reflexiv**
$v - v' \in U \implies -(v - v') = v' - v \in U$, also ist die Relation **symmetrisch**
$v -w \in U \land w - v' \in U \implies (v - w) + (w - v') = v - v' \in U$, also **transitiv**

Mit $V / U$ bezeichnet man dann die Menge der Äquivalenzklassen $[v]_U = v + U$, die man **Faktorraum** nennt. Denn man sagt, dass $V / U$ aus $V$ entsteht, wenn man $U$ 'herausfaktorisiert', also abzieht.

# Faktorräume als $K$-Vektorräume:
Definiere man folgende Operationen:
$+ : V/U \times V/U \rightarrow V/U, [v] + [v'] := [v + v']$ 
$\cdot: K \times [v] \rightarrow V/U, [\lambda \cdot v]$ 

Diese sind wohldefiniert. 
	Betrachte man $[v] = [u], [v'] = [u']$, d.h. $v - u \in U$ und $v' - u' \in U$, also auch $(v - u) + (v' - u') = (v + v') - (u + u') = [v + v'] = [u + u'] \in U$ 
	Außerdem ist dann $\lambda \cdot (v - u) = (\lambda \cdot v - \lambda \cdot u) = \lambda \cdot [v] = [\lambda \cdot v] \in U$

Die Vektorraumaxiome werden dabei aus $V$ induziert, da 'im Herzen' ja mit Differenzen von Vektoren aus $V$ gearbeitet wird. Dabei ist insbesondere $[0]$ das neutrale Element der Addition. Ihre Differenz liegt dann nämlich auf der Linie.

# Quotientenabbildungen:
Die Abbildung $q: V \rightarrow V / U, v \mapsto [v]$ ist linear und surjektiv (die Linearität wurde oben bewiesen, die Surjektivität ist leicht erkennbar).
Weiterhin ist $ker (q) = U$, da sich jeder Vektor in $V / U$ als Summe des Nullvektors mit sich selbst ergibt.

Die Dimension ergibt sich aus der [[Dimensionsformel]] für [[Lineare Abbildungen]]:
$dim V / U = dim(imq) = dim V - dim(ker q) = dim V - dim U$.

Man nennt $q$ die **Quotientenabbildung**.
# Beispiele
- Betrachte man eine Linie im $R^2$, die einen Untervektorraum konstituiert, sowie einen beliebigen Vektor $v$, also Punkt im $R^2$. Dann entspricht $[v]$ der 'Verschiebung' der Linie zu diesem Punkt. Alle Punkte, die in dieser neuen Linie liegen, entsprechen dann einer Äquivalenzklasse.

