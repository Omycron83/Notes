Seien $v_1, ..., v_r \in V$ und $w_1, ..., w_r \in W$. Dann gilt:
1. Wenn $v_1, ..., v_r$ linear unabhängig sind, so existiert ein $F \in Hom(V, W)$ mit $F(v_i) = w_i$
2. Wenn $v_1, ..., v_r$ eine Basis von $V$ ist, dann ist diese Darstellung sogar eindeutig. Zusätzlich:
	1. $F$ ist injektiv <-> $w_1, ..., w_r$ sind linear unabhängig
	2. $im F = <w_1, ..., w_r>$ 

# Beweis:
$2. \implies 1.$:
Angenommen, diese sei nicht eindeutig. Dann gäbe es zwei lineare Abbildungen $F, G$ mit $F(v_i) = w_i = G(v_i)$. 
$\Leftrightarrow F(v_i - v_i) = o$
