Seien $U_1, U_2$ [[Untervektorräume|Unterräume]] eines $K$-[[Vektorraum|Vektorraumes]] $V$. Dann heißt $U_1 + U_2 := \{x + y |x \in U_1, y \in U_2\}$ die **Summe** von $U_1 + U_2$.

Es ist zu notieren, dass man tangential verwandt auch konventionell 
$v + U := \{v + w|w \in U \}$ schreibt. ^ea229e
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
## Dimension des Untervektorraumes
Seien $U_1, U_2$ Untervektorräume von $V$. Dann ist $dim(U_1 + U_2) = dim(U_1) + dim (U_2) - dim(U_1 \cap U_2)$ die [[Dimension|Dimension des Vektorraumes]].

Beweis:
	Sei $b_1, ..., b_r$ eine Basis von $U_1 \cap U_2$. Dann kann man die Familie nach [[Basisaustauschlemma|dem Basisaustauschsatz]] jeweils zu einer Basis von $U_1$ mit $B_1 = b_1, ..., b_r, w_1, ..., w_k$ und von $U_2$ mit $B_2 = b_1, ..., b_r, v_1, ..., v_l$.
	Dann ist $b_1, ..., b_r, w_1, ..., w_k, v_1, ..., v_l$ eine Basis von $U_1 + U_2$, wonach dann die obige Aussage gilt, da $r + k + l = (r + k) + (r + l) - r$:
		Erzeugendensystem: Sei $v + w \in U_1 + U_2$. Dann ist jeweils $v \in <b_1, ..., b_r, w_1, ...., w_k>$ und $w \in <b_1, ..., b_r, v_1, ..., v_l>$ wodurch $v + w \in <b_1, ..., b_r, w_1, ..., w_k, v_1, ..., v_l>$. 
		Linear Unabhängig: Sei $o = \lambda_1 b_1 + ... + \lambda_r b_r + \phi_1 w_1 + ... + \phi_k w_k + \mu_1 v_1 + ... + \mu_l v_l$ 
		Dann ist 
		$\mu_1 v_1 + ... + \mu_l v_l = -(\lambda_1 b_1 + ... + \lambda_r b_r + \phi_1 w_1 + ... \phi_k w_k)$
		Wobei ersterer Term $\in U_2$, zweiterer $\in U_1$ ist, wodurch der linke Term $\in U_1 \cap U_2$ ist.
		Damit ist $\mu_1 v_1 + \mu_l v_l = \xi_1 b_1 + ... + \xi_r b_r \Leftrightarrow \mu_1 v_1 + \mu_l v_l - (\xi_1 b_1 + ... + \xi_r b_r) = o$   
		Da aber $v_1, ..., v_l, b_1, ..., b_r$ Basis von $U_2$ ist, gilt also insbesondere $\mu_1 = ... = \mu_l$.
		Somit ist, wenn man dies in die obere Gleichung einsetzt,
		$o = \lambda_1 b_1 + ... + \lambda_r b_r + \phi_1 w_1 + ... + \phi_k w_k + 0 v_1 + ... + 0 v_l$
		Und dadurch, dass $b_1, ...,b_r, w_1, ..., w_k$ Basis von $U_1$ ist,
		folgt zusätzlich $\lambda_1 = ... = \lambda_r = \phi_1 = ... = \phi_k$ 
		Und somit müssen alle Koeffizienten $0$ sein. $\square$

## Summe und Erzeugnis:
Seien $U_1, U_2$ Untervektorräume von $V$. Dann ist $<U_1, U_2> = U_1 + U_2$, also dass [[Lineare Erzeugnisse & Unabhängigkeit|lineare Erzeugniss]] gleich der Summe.

Beweis:
	Die Inklusion $U_1 + U_2 \subset <U_1, U_2>$ sei trivial.
	Sei $\lambda_1 u_{1,1} + ... + \lambda_r u_{1,r} + \mu_1 u_{1,m} + ... + \mu_m u_{1, m} \in <U_1, U_2>$. Dann ist wegen der Untervektorraumstellung $\lambda_1 u_{1,1} + ... + \lambda_r u_{1,r} \in U_1, \mu_1 u_{1,m} + ... + \mu_m u_{1, m} \in U_2$, sodass $<U_1, U_2> \subset U_1 + U_2$. $\square$


# Beispiele:
- $U + \{o\} = U$ 
- $U + U = U$
- $U + U' = U$, wenn $U'$ Untervektorraum von $U$ ist 
- Sei $V = R^3$ und $U = \{(x, x, 0) | x \in R\}, W = \{(0, y, 0) | y \in R\}$, dann ist $U + W = \{(x, x + y, 0) | x, y \in R \}$ die x-y-Ebene
