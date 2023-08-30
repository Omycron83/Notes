Seien $v_1, ..., v_r \in V$ eine Basis und $w_1, ..., w_r \in W$. Dann gilt: Es existiert ein eindeutiges $F \in Hom(V, W)$ mit $F(v_i) = w_i$. Zusätzlich gilt:
	1. $F$ ist injektiv <-> $w_1, ..., w_r$ sind linear unabhängig
	2. $im F = <w_1, ..., w_r>$ 

# Beweis:
Sei $v \in V$, dann gilt: $v = \sum_1^r \lambda_i v_i$ nach Basisdefinition.
Definiere man nun $F(v) = F(\sum_1^r \lambda_i v_i) = \sum_1^r \lambda_i F(v_i) := \sum_1^r \lambda_i w_i$

Man ordnet $v$ also einem $w \in W$ zu, der sich als Linearkombination der $w_i$ mit denselben Koeffizienten wie in der Basisdarstellung von $v$.

Dass dabei 

Dass diese Abbildung $F$ auch wirklich linear, d.h. $\in Hom(V, W)$ ist und trotzdem $f(v_i) = w_i$ gilt, kann man aus der Basisdarstellung $F()
