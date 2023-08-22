Sei $V$ ein $L$-Vektorraum. Dann gibt es eine maximal unabhängige Teilmenge $B \subset V$, also eine Basis. (Unabhängig davon, ob $B$ endlich ist.)

Beweis:
	Sei $M := \{B | B \text{linear unabhängig}\}$. $M$ ist insbesondere $\neq \emptyset$, da $\emptyset \in M$.
	Definiere man auf dieser Menge die [[Halbordnungen|Halbordnung]] $R$ als Inklusion, wobei $a R b$ wenn die Familie $a$ in der Familie $b$ enthalten ist. Nehme man eine [[Ketten|Kette]] $K \subset M$. Dann ist diese Kette [[Ketten#^70320a|induktiv]].
	Denn definiere man $B_0 := \bigcup_{B \in K} B$ . Dann wäre $B_0$ eine potentielle [[Ketten#^70320a|obere Schranke]]. Nun ist die Frage, ob $B_0$ wirklich eine obere Schranke **in $M$** ist. Dazu betrachte man dessen [[Lineare Erzeugnisse & Unabhängigkeit|lineare Unabhängigkeit]]: $o = \lambda_1 b_1 + ... + \lambda_k b_k$ mit $\lambda_i \in L,
	