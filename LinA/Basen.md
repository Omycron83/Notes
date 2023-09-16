## Definition Basis:
Eine Familie an Vektoren $v_1, ..., v_n$ nennt man Basis eines Vektorraumes $V$ wenn gilt:
1. $<v_1, ..., v_n> = V$
2. $v_1, ..., v_n$ sind linear unabhängig

Jeder Vektor in $V$ kann so **eindeutig** als lineares Erzeugniss der Basis geschrieben werden.
### Beweis Eindeutigkeit der Darstellung:
Die eindeutige Darstellbarkeit lässt sich aus der [[Lineare Erzeugnisse & Unabhängigkeit#^b227ab|Äquivalent zur linearer Unabhängigkeit und eindeutiger Darstellbarkeit innerhalb einer linear unabängigen Familie (anstatt hier generellem Vektor) zeigen:]] sei $v \in V$. Dann ist $v = \lambda_1 v_1 + … + \lambda_n v_n = \mu_1 v_1 + … + \mu_n v_n$, sodass $o = (\lambda_1-  \mu_1) v_1 + … +(\lambda_n - \mu_n) v_n$, sodass die Eindeutigkeit der Darstellung äquivalent zur Basis ist (der Status als Erzeugendensystem gilt aus der beliebigen Wahl eines $v \in V$).   

## Weitere Charakterisierung:

### Körperisomorphismus
Bezüglich einer Basis $v_1, ..., v_r$  gibt es also eine Bijektion $\phi: V \rightarrow K^n$ , wobei $\phi(v) = \phi(\lambda_1 v_1 + ... + \lambda_r v_r) = (\lambda_1, ..., \lambda_r)$.
Die sogar strukturerhaltend ist, da diese Abbildung linear und jeder Körper(tupel) ein Vektorraum ist. Die Bijektivität sei offensichtlich, wenn eine Basis gegeben ist. 
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
	Nehme man an, es gäbe ein $B' \subset B, B' \neq B$ für das $span(B') = V$, wobei $B' = v_1, ..., v_l$ und $B = v_1, ..., v_r$ mit $l < r$ :
	Dann könnte man ein $v \in V$ durch geschickte Umbenennung darstellen als:
	$v = \lambda_1 v_1 + ... + \lambda_r v_r = \mu_1 v_1 + ... + \mu_l v_l$ 
	Somit müsste sich also ein $v_r \in B \backslash B'$ darstellen lassen als:
	$v_r = \frac{1}{\lambda_r}(\mu_1 - \lambda_1)v_1 + ... + \frac{1}{\lambda_r}(\mu_l - \lambda_l)v_l + ... + \frac{\lambda_{r-1}}{\lambda_r}v_{r-1}$ 
	Dann wäre aber $B$ nicht linear unabhängig und so keine Basis. Es muss dabei ein $\lambda_r \neq 0$ geben, da sonst $v = 0$ sein müsste, was nicht o.B.d.A. gilt. Und die anderen Koeffizienten müssten $\neq 0$ 
	 sein, da sonst $v  = v_r$ und der Nullvektor nicht in einem linear unabhängigen System existieren kann.
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
	
##### Alternativer Folgende Aussagen sind äquivalent für eine Familie $B = (v_1, ..., v_r)$ eines Vektorraumes von $V$:
1. $B$ ist eine Basis von $V$ 
2. $B$ ist minimal erzeugend, d.h. für $span(B) = V$ und $span(B') \neq V \forall B' \subset B$ mit $B' \neq B$
3. Die Darstellung eines jeden Vektors ist eindeutig, d.h. $\forall v \in V \exists ! \lambda_i \in K; v = \lambda_1 v_1 + … + \lambda _n v_n$
4. $B$ ist maximal linear unabhängig, d.h. $B$ ist linear unabhängig und $B \cup \{v\}$ ist linear unabhängig $\forall v \in V , v\not \in B$ 
Beweis durch Ringschluss:
	$1. \implies 2.:$ Beweis durch Widerspruch: Nehme man an, $B$ wäre eine Basis und gleichzeitig nicht minimal linear erzeugend, und führe dies dann zu einem Widerspruch. Dann gäbe es eine echte Teilmenge $B‘ \subset B: span(B‘) = V$, die ein kleinstes Erzeugendensystem darstellt. Nummeriere man um, sodass $B = v_1, …, v_n$ und $B’ = v_1, …, v_r, r < n$ So gibt es ein $v \in V: v = \lambda_1 v_1 + … +  \lambda_n v_n = \mu_1 v_1 + ….+ \mu_r v_r$ mit $\lambda_r \neq 0$, da o.B.d.A. $v \neq 0$. Somit müsste sich also ein $v_r \in B \backslash B'$ darstellen lassen als:
	$v_r = \frac{1}{\lambda_r}(\mu_1 - \lambda_1)v_1 + ... + \frac{1}{\lambda_r}(\mu_l - \lambda_l)v_l + ... + \frac{\lambda_{r-1}}{\lambda_r}v_{r-1}$ 
	Dann wäre aber $B$ nicht linear unabhängig und so keine Basis.
	$2. \implies 3.:$  
	$3. \implies 4.:$ Nehme man an, die Darstellung wäre eindeutig. Dies würde bedeuten, dass $

## Existenz einer Basis für endlich erzeugbare Vektorräume:
Ist $X \subset V$ ein endliches Erzeugendensystem, dann gibt es eine Basis.

Beweis:
	Jedes Erzeugendensystem beinhaltet ein minimales Erzeugendensystem. Dies ist wie o.g. eine Basis. 

Also besitzt jeder endlich erzeugbarer Vektorraum eine Basis.

