Seien $U_1, U_2$ [[Untervektorräume|Unterräume]] eines $K$-[[Vektorraum|Vektorraumes]] $V$. Dann heißt $U_1 + U_2 := \{x + y |x \in U_1, y \in U_2\}$ die **Summe** von $U_1 + U_2$.

# Eigenschaften:

## $U_1 + U_2$ als kleinster Untervektorraum
Seien $U_1, U_2$ Untervektorräume von $V$. Dann ist $U_1 + U_2$ ist der kleinste Untervektorraum, der $U_1 \cup U_2$ enthält.

Beweis:
	Untervektorraumkriterien: 
	1. $o \in U_1 + U_2$, da $o = o + o \in U_1 + U_2$ 
	2. $x, x' \in U_1, y, y' \in U_2: (x + y) \in U_1 + U_2, (x' + y') \in U_1 + U_2$
	$\implies (x + y) + (x' + y') = (x + x') \in U_1 + (y + y') \in U_2 \in U_1 + U_2$
	3. $x \in U_1, y \in U_2 : (x + y) \in U_1 + U_2, \lambda(x + y) = \lambda x \in U_1 + \lambda y \in U_2 \in U_1 + U_2$
	Kleinster Untervektorraum:
	Sei $G$ ein kleinerer Untervektorraum, der $U_1 \cup U_2$ enthält. Dieser enthält dann ein $v \in V: v = u_1 + u_2, u_1 \in U_1, u_2 \in U_2$ nicht.
	Dann ist er aber kein Untervektorraum, da er $u_1, u_2 \in U_1 \cup U_2$ enthält.

# Beispiele:
- $U + \{o\} = U$ 
- $U + U = U$
- $U + U' = U$, wenn $U'$ Untervektorraum von $U$ ist 
- 