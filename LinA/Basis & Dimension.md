## Definition Basis:
Eine Familie an Vektoren $v_1, ..., v_n$ nennt man Basis eines Vektorraumes $V$ wenn gilt:
1. $<v_1, ..., v_n> = V$
2. $v_1, ..., v_n$ sind linear unabhängig

Jeder Vektor in $V$ kann so **eindeutig** als lineares Erzeugniss der Basis geschrieben werden.
### Beweis Eindeutigkeit der Darstellung:
Nehme man an, es gäbe zwei unterschiedliche Linearkombinationen, um ein $v \in V$ darzustellen:
$\lambda_1 v_1 + ... + \lambda_n v_n = \mu_1 v_1 + ... + \mu_n v_n (= v)$ 

## Weitere Charakterisierung:

### Körperisomorphismus
Bezüglich einer Basis $v_1, ..., v_r$  gibt es also eine Bijektion $\phi: V \rightarrow K^n$ , wobei $\phi(v) = \phi(\lambda_1 v_1 + ... + \lambda_r v_r) = (\lambda_1, ..., \lambda_r)$.
Die sogar strukturerhaltend ist, da diese Abbildung linear und jeder Körper(tupel) ein Vektorraum ist.
Beweis:
	Linearität:
	$\phi(\lambda v + w) = \phi(\lambda (\lambda_1 v_1 + ... + \lambda_r v_r) + \mu_1 v_1 + ... + \mu_r v_r) = \phi(\lambda \lambda_1 v_1 + ... + \lambda \lambda_r v_r) + \mu_1 v_1 + ... + \mu_r v_r)$ 
	$= \phi( (\lambda \lambda_1 + \mu_1) v_1  + ... + (\lambda \lambda_r + \mu_r ) v_r) = (\lambda \lambda_1 + \mu_1, ..., \lambda \lambda_r + \mu_r)$ 
	$= \lambda \phi(v) + \phi(w)$ 
	Körper(tupel) sind Vektorräume:
	[[Vektorraum#^6e22e7]]

Somit ist jeder Vektorraum mit einer Basenlänge $n$ isomorph zu seinem $K^n$ .

### Basis = minimal Erzeugend, maximal Unabhängig:
Folgende Aussagen sind äquivalent für eine Familie $B = (v_1, ..., v_r)$ eines Vektorraumes von $V$:
1. $B$ ist eine Basis von $V$ 
2. $B$ ist minimal erzeugend, d.h. für $span(B) = V$ und $span(B') \neq V \forall B' \subset B$ mit $B' \neq B$ 
3. $B$ ist maximal linear unabhängig, d.h. $B$ ist linear unabhängig und $B \cup \{v\}$ ist linear unabhängig $\forall v \in V , v\not \in B$ 
Beweis:
	$1. \implies 2.$:
	Nehme man an, es gäbe ein $B' \subset B, B' \neq B$ für das $span(B') = V$ .
	Dann könnte man ein $v \in V$ darstellen als:
	$v = (\)