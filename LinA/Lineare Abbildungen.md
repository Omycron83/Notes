## Definition:
Eine [[Abbildungen|Abbildung]] $F: V \rightarrow W$ zwischen zwei [[Vektorraum|Vektorräumen]] $V, W$ über einem [[Körper]] $K$ nennt man linear, wenn sie **Additiv** und **Homogen** ist:
$F(v + w) = F(v) + F(w)$ und
$F(\lambda \cdot v) = \lambda \cdot F(v)$
$\forall v,w \in V, \lambda \in K$ 

**Bemerkung**: Dies kann zusammengefasst werden zu: $F(\lambda v + w) = \lambda F(v) + F(w)$

Dabei bilden lineare Abbildungen also Vektorraumhomomorphismen, da sie die generelle Vektorraumstruktur sowohl in der Addition als auch der Skalarmultiplikation erhalten, die **Additivität stellt den [[Gruppenhomomorphismen|Gruppenhomomorphismus]]**, die **Homogenität den Skalarhomomorphismus**. ^587427

Ist $V = W$, dann nennt man eine lineare Abbildung einen **Endomorphismus**.
Ist $F$ bijektiv, dann nennt man die lineare Abbildungen einen **Vektorraumisomorphismus**.
Gilt beides, so nennt man die lineare Abbildung einen **Automorphismus**. ^d82a1b

### Eigenschaften:
1. **$F(o) = o$**
	$F(o + o) = F(o) + F(o) = F(o)$, folgt direkt aus der [[Gruppenhomomorphismen#^9d8893|Gruppenhomomorphismuseigenschaft]]  $\square$ 

2. $F(\lambda_1 \cdot v_1 + ... + \lambda_n \cdot v_n) = \lambda_1 F(v_1) + ... + \lambda_n F(v_n)$
	Folgt aus der Expansion: $F(\lambda_1 \cdot v_1 + ... + \lambda_n v_n) = F(\lambda_1 \cdot (v_1 + ... + \frac{\lambda_n}{\lambda_1} \cdot v_n) = \lambda_1 F(v_1 + (... + \frac{\lambda_n}{\lambda_1} \cdot v_n))$ 
	$= \lambda_1 F(v_1) + \lambda_1 F(... +\frac{\lambda_n}{\lambda_1} \cdot v_n ) = \lambda_1 F(v_1) + F(... +\lambda_n \cdot v_n ) = ... = \lambda_1 F(v_1) + ... + \lambda_n F(v_n)$ $\square$

3. Ist $U$ ein Untervektorraum von $V$, dann ist $F(U)$ ein Untervektorraum von $W$.
	Durch die linearität der Abbildung lassen sich die [[Untervektorräume|Untervektorraumkriterien]] von $F(U)$ leicht auf den Untervektorraumstatus von $U$ zurückführen:
	1. Die Teilmengenrelation sei trivial, und da $o \in U$ ist $F(o) = o \in F(U)$
	2. Sei $v, w \in F(U)$, mit $v = F(l), w = F(g), f,g \in U$. Dann ist durch den Untervektorraumstatus von $U$ auch $l + g \in U$, und damit $F(l + g) = F(l) + F(g) = v + w \in F(U)$ im [[Bild einer linearen Abbildung|Bild der Abbildung]]. 
	3. Sei $\lambda \in K, v \in F(U)$, mit $v = F(l), l \in U$. Dann ist durch den Untervektorraumstatus auch $\lambda l \in U$, und damit auch $F(\lambda l) = \lambda F(l) = \lambda v \in F(U)$.

4. Sind $v_1, ..., v_n$ [[Lineare Erzeugnisse & Unabhängigkeit|linear abhängig]] in $V$, dann sind auch $F(v_1), ..., F(v_n)$ linear abhängig in $W$:
	Sind sie linear abhängig in $V$, dann gibt es Koeffizienten $\lambda_1, ..., \lambda_n$ mit mind. einem $\lambda_n \neq 0$ sodass die Linearkombination den Nullvektor ergibt, also:
	$F(\lambda_1 v_1 + ... + \lambda_n v_n) = F(o) = \lambda_1 F(v_1) + ... + \lambda_n F(v_n)$ nach 2.
	Und da wir aus 1. wissen, dass $F(o) = o$ ergibt die Linearkombination von $F(v_1), ..., F(v_n)$ auch hier den Nullvektor, und dies ebenfalls mit nichtrivialen Koeffizienten. $\square$

5. Ist $F$ [[Abbildungen#^4b4823|injektiv]], dann gilt: $v_1, ..., v_n$ [[Lineare Erzeugnisse & Unabhängigkeit|linear unabhängig]] $\implies$ $F(v_1), ..., F(v_n)$ [[Lineare Erzeugnisse & Unabhängigkeit|linear unabhängig]]
	Beweis: Seien $v_1, ..., v_n$ linear unabhängig. Dann ist $\lambda_1 v_1 + ... + \lambda_n v_n = o \implies \lambda_1 = ... = \lambda_n$
	Wir wissen nach obrigem, dass $ker \; F = \{o \} \Leftrightarrow$ Injektivität. So gilt $F(v) = o$ genau dann, wenn $v = o$. Also gilt $F(\lambda_1 v_1 + ... + \lambda_n v_n) = F(o) = o \implies \lambda_1 = ... = \lambda_n$.
	Und dadurch auch $\lambda_1F( v_1) + ... + \lambda_n F( v_n) = o \implies \lambda_1 = ... = \lambda_n$ ^f38efc


6.Sei $U$ ein Unterraum von $V$. Dann gilt: $dim(F(U)) \le dim(U)$:
	$dim(U)$ ist nach der [[Dimension|Dimensionsdefinition]] die [[Basen|maximale Länge linear unabhängiger Familien]] in $U$. Selbiges gilt für $dim(F(U))$ mit $F(U)$. So ist jede Familie mit mehr als $dim(U)$ Mitgliedern linear abhängig in $U$, und somit auch nach 5. ihre jeweiligen Bildvektoren linear abhängig in $F(U)$. Da dies die einzigen Elemente von $F(U)$ kann die Dimension von $F(U)$ maximal so groß sein wie die Dimension von $U$, da jede Familie mit größerer Länge als $dim(U)$ linear abhängig in $F(U)$ ist.  $\square$

7. Wenn $dim V = dim W$, dann ist für $F: V \rightarrow W$ linear äquivalent:
1. $F$ ist injektiv
2. $F$ ist surjektiv
3. $F$ ist injektiv
	Beweis durch beidseitige Implikation der ersten beiden Aussagen, woraus sich die dritte Äquivalent [[Abbildungen#^4b4823|äquivalent ergibt]]:
	$1. \implies 2.:$ $1.$ ist  [[Kern einer linearen Abbildung#^f1cf24|äquivalent zu]] $kerF = \{0\}$. Nach dem [[Dimensionsformel|Dimensionssatz]] gilt: $dim Im F + dim ker F = dim V$, wobei durch $ker F = \{o\}$ $\Leftrightarrow dim ImF = dimV$ und nach der Vorraussetzung $dim Im F = dim W$. Und da jede Basis minimal Erzeugend ist gilt so $\Leftrightarrow F$ surjektiv.
	$2. \implies 1.:$ 2. ist äquivalent zu $dim Im F = dim W$, nach Dimensionsformel also $dim Im F + dim ker F = dim V$, durch Vorraussetzung  $\Leftrightarrow  dim Im F + dim ker F = dim W$, durch Gleichheit
	$\Leftrightarrow dim ker F = 0$, dadurch dass inklusion jeglichen Vektors $\neq o$ zu $dim > 0$ führt
	$\Leftrightarrow ker F = \{o\}$, nach o.g. Äquivalenz:
	$\Leftrightarrow F$ injektiv.
#### Kompositionen linearer Abbildungen sind linear
Seien $F : V \rightarrow W$, $G: W \rightarrow U$  lineare Abbildungen. Dann ist auch $G \circ F$ linear.
##### Beweis:
Damit $G \circ F = G(F(v))$ linear ist, muss gelten:
$G(F(\lambda v + w)) = \lambda G(F(v)) + G(F(w))$
Durch die Linearität von $F$ wissen wir:
$G(F(\lambda v + w)) = G(\lambda F(v) + F(w))$
Und dann durch die Linearität von $G$:
$G(\lambda F(v) + F(w)) = \lambda G(F(v)) + G(F(w))$ $\square$

