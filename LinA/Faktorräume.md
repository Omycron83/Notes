Sei $V$ ein $K$-[[Vektorraum]] und $U$ ein [[Untervektorräume|Untervektorraum]] von $V$ sowie $\sim$ eine [[Relationen|Relation]] auf $V$, mit $v \sim v' \Leftrightarrow v - v' \in U$, sprich $v$ ist äquivalent zu $v'$ modulo $U$, d.h. es gibt ein $u \in U: u = v - v' \Leftrightarrow v = u + v'$ bzw. $v \in v' + U$ 

Das es sich um eine [[Relationen#^405c4f|Äquivalenzrelation]] handelt kann man leicht nachweisen:
$v - v = o \in U \forall v \in V$, also ist die Relation **reflexiv**
$v - v' \in U \implies -(v - v') = v' - v \in U$, also ist die Relation **symmetrisch**
$v -w \in U \land w - v' \in U \implies (v - w) + (w - v') = v - v' \in U$, also **transitiv**

Mit $V / U$ bezeichnet man dann die Menge der Äquivalenzklassen $[v]_U = v + U$, die man **Faktorraum** nennt.

# Faktorräume als $K$-Vektorräume:
Definiere man folgende Operationen:
$+ : V/U \times V/U \rightarrow V/U, [v] + [v'] := [v + v']$ 
$\cdot: K \times [v] \rightarrow V/U, [\lambda \cdot v]$ 

Diese sind wohldefiniert. 
	Betrachte man $[v] = [u], [v'] = [u']$, d.h. $v - u \in U$ und $v' - u' \in U$, also auch $(v - u)


 