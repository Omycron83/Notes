# Definition:
Eine Abbildung $V^n \rightarrow K, \Delta (a_1, …, a_n) = l \in K$ wird Determinantenabbildung genannt, wenn 
- Sie multilinear ist, d.h. $\Delta(a_1, …,\lambda a + \mu a‘,…, a_n) = \lambda \Delta(a_1, …, a, …, a_n) + \mu \Delta(a_1, …, a‘, …, a_n) \forall a_i \in V$
- Sie alternierend ist, d.h. $\Delta (a_1, …, a, …, a, …, a_n)= 0$

Bemerkung: 
Die Nullabbildung $(a_1, …, a_n) \mapsto 0 \forall a_1, …, a_n \in V$ erfüllt offensichtlich beide Eigenschaften. Man nennt sie auch die **triviale** Determinantenfunktion.

Im Falle $V^n = K^n$ betrachtet man die klassischen [[Determinanten von Matrizen]].
## Eigenschaften:
### Determinantenfunktion <-> Lin. Abh. Familien $\mapsto$ 0
Betrachte man eine multilineare Funktion $\Delta : V^n \rightarrow K$. Dann sind folgende Aussagen äquivalent:
1. $\Delta$ ist außerdem alternierend und somit eine Determinantenfunktion
2. Für jeden n-Tupel [[Lineare Erzeugnisse & Unabhängigkeit#^33f43f|linear abhängiger]] Vektoren $(a_1, …, a_n)$ gilt: $\Delta (a_1,…, a_n) = 0$

Beweis:
	Der Beweis erfolgt durch das zeigen der beidseitigen Implikation:
	$1. \implies 2.:$ Nehme man einen linear abhängigen Tupel
	$\Delta (a_1, …, a_i, …,  a_n) = \Delta(a_1, …, \lambda_1 a_1 + … +\lambda_{i - 1} a_{i-1} + \lambda_{i + 1} a_{i + 1} + … \lambda_na_n, …, a_n)$
	und wende dann die Multilinearität an:
	$\Delta(a_1, …, \lambda_1 a_1 + … + \lambda_{i - 1} a_{i-1} + \lambda_{i + 1} a_{i + 1} + … \lambda_n a_n, …, a_n)$ 
	$= \lambda_1 \Delta(a_1, …, a_1, …, a_n) + ….$ 
	Und dann folgt durch die alternierende Eigenschaft der Determinantenfunktion
	$= \lambda_1 \cdot 0 + … + \lambda_n \cdot 0$ 
	$1. \implies 2.:$ folgt offensichtlich.

### Weitere Eigenschaften
Sei $\Delta$ eine Determinantenfunktion auf $V$. Fuer $a_1, ..., a_n \in V$ gilt:
1. $\Delta(..., a_i, ..., a_j, ...) = -(..., a_j, ..., a_i, ...)$
2. $\Delta(a_{\pi(1)}, ..., a_{\pi(n)}) = sgn_\pi \cdot \Delta(a_1, ..., a_n)$
3. $\Delta(..., a_i + \alpha a_j, ..., a_j, ...) = \Delta(..., a_i, ..., a_j, ...)$

Bew.:
	1. Folgt aus der Null-heit der Addition der beiden Tupel
	2. Folgt aus 1. sowie der Definition des [[Permutationen#^0c71fb|Signums]] als Anzahl der Vertauschungen bzw. Transpositionen.
	3. Folgt, wenn man $a_j$ herausaddiert und $\alpha$ herauszieht 

