## Definition Basis:
Eine Familie an Vektoren $v_1, ..., v_n$ nennt man Basis eines Vektorraumes $V$ wenn gilt:
1. $<v_1, ..., v_n> = V$
2. $v_1, ..., v_n$ sind linear unabhängig

Jeder Vektor in $V$ kann so **eindeutig** als lineares Erzeugniss der Basis geschrieben werden.
### Beweis Eindeutigkeit der Darstellung:
Nehme man an, es gäbe zwei unterschiedliche Linearkombinationen, um ein $v \in V$ darzustellen:
$\lambda_1 v_1 + ... + \lambda_n v_n = \mu_1 v_1 + ... + \mu_n v_n (= v)$ 

## Weitere Charakterisierung:
Bezüglich einer Basis gibt es also eine Bijektion $\phi: V \rightarrow K^n$ , wobei $\phi(v) = \phi(\lambda_1 v_1 + ... + \lambda_r v_r) = (\lambda_1, ..., \lambda_r)$.
Die sogar strukturerhaltend ist, da diese Abbildung linear und jeder Körper ein Vektorraum ist.
	B