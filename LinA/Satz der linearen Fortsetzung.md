Seien $v_1, ..., v_r \in V$ eine Basis und $w_1, ..., w_r \in W$ beliebige Vektoren. Dann gilt: Es existiert ein eindeutiges $F \in Hom(V, W)$ mit $F(v_i) = w_i$. Zusätzlich gilt:
	1. $F$ ist injektiv <-> $w_1, ..., w_r$ sind linear unabhängig
	2. $im F = <w_1, ..., w_r>$ 
# Beweis:
## Existenz und Eindeutigkeit:

Sei $v \in V$, dann gilt: $v = \sum_1^r \lambda_i v_i$ nach Basisdefinition.
Definiere man nun $F(v) = F(\sum_1^r \lambda_i v_i):= \sum_1^r \lambda_i w_i$

Man ordnet $v$ also einem $w \in W$ zu, der sich als Linearkombination der $w_i$ mit denselben Koeffizienten wie in der Basisdarstellung von $v$. 

Durch die eindeutigen Koeffizienten ist $f$ dabei wohldefiniert.

Dies erfüllt außerdem $f(v_i) = w_i$, da $f(v_i) = f(0 v_1 + ... + 1 v_i + ... + v_n)$ durch lineare Unabhängigkeit und so $f(v_i) = 1 \cdot F(w_i)$.

Dass diese Abbildung $F$ auch zusätzlich linear, d.h. $\in Hom(V, W)$ ist, gilt es nun nachzuweisen.

Betrachte man dabei beliebige $v, v'$. Dadurch, dass $v_1, ..., v_n$ eine Basis bilden, kann man $v$ wie oben und $v' = \sum_1^r \mu_i v_i$ darstellen. 

**Additivität:**
$F(v + v') = F(\sum_1^r \lambda_i v_i + \sum_1^r \mu_i v_i) = F(\sum_1^r (\lambda_i + \mu_i) v_i)$
Nach der Definition: $F(\sum_1^r (\lambda_i + \mu_i) v_i) = \sum_1^r (\lambda_i + \mu_i)w_i = \sum_1^r \lambda_i w_i + \sum_1^r \mu_i w_i = F(v) + F(v_i)$

**Homogenität:**$F(\mu v) = F(\mu \sum_1^r \lambda_i v_i) = F(\sum_1^r \mu \lambda_i v_i) = \sum_1^r \mu \lambda_i w_i = \mu \sum_1^r \lambda_i w_i = \mu F(v)$

**Eindeutigkeit:**
Angenommen es gibt ein weiteres $G \in Hom(V, W)$ mit $g(v_i) = w_i$ . Dann ist:
$G(v)  = G(\sum_1^r \lambda_i v_i) = \sum_1^r \lambda_i G(v_i) = \sum_1^r \lambda_i w_i = F(v)$.
Dann wäre diese also identisch zu $F$.

## Zusatzaussagen:
1.)
$F$ injektiv $\implies$ linear unabhängig:
Folgt aus [[Lineare Abbildungen#^f38efc|Lineare Abbildungseigenschaft]]

linear unabhängig $\implies$ $F$ injektiv:
Seien die $w_i$ nicht linear unabhängig, dann lässt sich 
$o = \sum_1^r \lambda_i w_i = \sum_1^r \lambda_i F(v_i) = F(\sum_1^r \lambda_i v_i)$ 
nicht-trivial bilden wodurch $ker F \neq \{ o \}$ und so nach [[Lineare Abbildungen#^683b21|Kerneigenschaft keine Injektivität]].

2.)
Es sei klar, dass zumindest $im F \subset <w_1, ..., w_r>$. Sei nun ein beliebiges $w \in <w_1, ..., w_r>$. Dann gilt $w = \sum_1^r \lambda_i w_i = \sum_1^r \lambda_i F(v_i) = F(\sum_1^r \lambda_i v_i)$. Nun muss man lediglich dass aus der Abgeschlossenheit existierende $v = \sum_1^r \lambda_i v_i$ wählen, sodass $F(v) = w$ und $w \in im F$, sodass auch $<w_1, ..., w_r> \subset im F$ 
