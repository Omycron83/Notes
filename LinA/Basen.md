## Definition Basis:
Eine Familie an Vektoren $v_1, ..., v_n$ nennt man Basis eines Vektorraumes $V$ wenn gilt:
1. $<v_1, ..., v_n> = V$
2. $v_1, ..., v_n$ sind linear unabhängig

Jeder Vektor in $V$ kann so **eindeutig** als lineares Erzeugniss der Basis geschrieben werden.
### Beweis Eindeutigkeit der Darstellung:
Die eindeutige Darstellbarkeit lässt sich aus der [[Lineare Erzeugnisse & Unabhängigkeit#^b227ab|Äquivalenz zwischen linearer Unabhängigkeit und eindeutiger Darstellbarkeit ablesen]].

## Weitere Charakterisierung:

### Körperisomorphismus
Bezüglich einer Basis $v_1, ..., v_r$  gibt es also eine Bijektion $\phi: V \rightarrow K^n$ , wobei $\phi(v) = \phi(\lambda_1 v_1 + ... + \lambda_r v_r) = (\lambda_1, ..., \lambda_r)$.
Die sogar strukturerhaltend ist, da diese Abbildung linear und jeder Körper(tupel) ein Vektorraum ist. Die Bijektivität sei offensichtlich, wenn die Basis gegeben ist. 
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
	Nehme man an, es gäbe ein $B' \subset B, B' \neq B$ für das $span(B') = V$ , wobei $B' = v_1, ..., v_l$ und $B = v_1, ..., v_r$ mit $l < r$ :
	Dann könnte man ein $v \in V$ durch geschickte Umbenennung darstellen als:
	$v = \lambda_1 v_1 + ... + \lambda_r v_r = \mu_1 v_1 + ... + \mu_l v_l$ 
	Somit müsste sich also ein $v_r \in B \backslash B'$ darstellen lassen als:
	$v_r = \frac{1}{\lambda_r}(\mu_1 - \lambda_1)v_1 + ... + \frac{1}{\lambda_r}(\mu_l - \lambda_l)v_l + ... + \frac{\lambda_{r-1}}{\lambda_r}v_{r-1}$ 
	Dann wäre aber $B$ nicht linear unabhängig und so keine Basis
	$2. \implies 1.$:
	Nehme man an, $B$ ist keine Basis (jedoch erzeugend). Dann ist $B$ auch nicht minimal erzeugend. 
	Somit gäbe es ein $v_i \in B$ mit $v_i = \lambda_1 v_1 + ... + \lambda_{i - 1} v_{i - 1} + \lambda_{i + 1} v_{i + 1} + ... + \lambda_r v_r$ .
	Nehme man nun an, dass ein $v \in span(v_1, ..., v_r)$ ist.
	Dann gilt:
	$v = \mu_1 v_1 + ... + \mu_i v_i + ... + \mu_r v_r$
	Einsetzen:
	$v = \mu_1 v_1 + ... + (\lambda_1 v_1 + ... + \lambda_{i - 1} v_{i - 1} + \lambda_{i + 1} v_{i + 1} + ... + \lambda_r v_r) + ... \mu_r v_r$ 
	$\Leftrightarrow (\mu_1 + \lambda_1) v_1 + ... (\mu_{i-1} + \lambda_{i - 1}) v_{i - 1} + (\mu_{i+1} + \lambda_{i + 1}) v_{i + 1} + ... + (\mu_r + \lambda_r) v_r$ 
	Und somit auch $v \in span(v_1, ..., v_{i-1}, v_{i + 1}, v_r)$ 
	$1. \implies 3.$:
	Da $B$ eine Basis ist, sind alle Basisvektoren linear unabhängig, und ein jedes $v \in V$ wird von ihr erzeugt. Somit ist $v$ durch eine Linearkombination darstellbar, und somit mit der Basis vereinigt nicht linear unabhängig.
	$3. \implies 1.$:
	Nehme man an, $B$ wäre zwar linear unabhängig, aber nicht erzeugend. Dann gibt es ein $v \in V$ mit $v \not \in span(v_1, ..., v_r)$ . Damit wäre dann jedoch $(v, v_1, ..., v_r)$ linear unabhängig. Dann wäre $B$ aber nicht maximal linear unabhängig. ^80a43c

## Existenz einer Basis für endlich erzeugbare Vektorräume:
Ist $X \subset V$ ein endliches Erzeugendensystem, dann gibt es eine Basis.

Beweis:
	Jedes Erzeugendensystem beinhaltet ein minimales Erzeugendensystem. Dies ist wie o.g. eine Basis.

Also besitzt jeder endlich erzeugbarer Vektorraum eine Basis.

