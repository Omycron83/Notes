Sei $V$ ein $L$-Vektorraum. Dann gibt es eine maximal unabhängige Teilmenge $B \subset V$, also eine Basis. (Unabhängig davon, ob $B$ endlich ist.)

Beweis:
	Sei $M := \{B | B \text{linear unabhängig}\}$. $M$ ist insbesondere $\neq \emptyset$, da $\emptyset \in M$.
	Definiere man auf dieser Menge die [[Halbordnungen|Halbordnung]] $R$ als Inklusion, wobei $a R b$ wenn die Familie $a$ in der Familie $b$ enthalten ist. Nehme man eine [[Ketten|Kette]] $K \subset M$. Dann ist diese Kette [[Ketten#^70320a|induktiv]]:
	Denn definiere man $B_0 := \bigcup_{B \in K} B$ . Dann wäre $B_0$ eine potentielle [[Ketten#^70320a|obere Schranke]]. Nun ist die Frage, ob $B_0$ wirklich eine obere Schranke **in $M$** ist. 
	Dazu betrachte man dessen [[Lineare Erzeugnisse & Unabhängigkeit|lineare Unabhängigkeit]]: $o = \lambda_1 b_1 + ... + \lambda_n b_n$ mit $\lambda_i \in L, b_i \in B_0$. 
	Und da $B_i \subset B_0$ gibt es $B_i \in K$ mit $b_i \in B_i$ für alle $i = 1,..., n$ . Außerdem ist klar, dass es $j = 1,..., n$ gibt mit $B_i \subset B_j$ , also auch $b_i \in B_j$ , wobei $B_j \in M$ natürlich linear unabhängig ist und so $\implies \lambda_1 = ... = \lambda_n = 0$ . 
	Somit kommt, durch die Existenz einer oberen Schranke $B_0$ und die daraus folgende induktivität, das [[Lemma von Zorn]] zu tragen: es gibt ein maximales Element von $M$, d.h. eine maximal linear unabhängige Familie. $\square$ 