## Definition:
Eine [[Abbildungen|Abbildung]] $F: V \rightarrow W$ zwischen zwei [[Vektorraum|Vektorräumen]] $V, W$ über einem [[Körper]] $K$ nennt man linear, wenn sie **Additiv** und **Homogen** ist:
$F(v + w) = F(v) + F(w)$ und
$F(\lambda \cdot v) = \lambda \cdot F(v)$
$\forall v,w \in V, \lambda \in K$ 

**Bemerkung**: Dies kann zusammengefasst werden zu: $F(\lambda v + w) = \lambda F(v) + F(w)$

Dabei bilden lineare Abbildungen also Vektorraumhomomorphismen, da sie die generelle Vektorraumstruktur sowohl in der Addition als auch der Skalarmultiplikation erhalten, die **Additivität stellt den [[Gruppenhomomorphismen|Gruppenhomomorphismus]]**, die **Homogenität den Skalarhomomorphismus**.

Ist $V = W$, dann nennt man eine lineare Abbildung einen **Endomorphismus**.
Ist $F$ bijektiv, dann nennt man die lineare Abbildungen einen **Vektorraumisomorphismus**.
Gilt beides, so nennt man die lineare Abbildung einen **Automorphismus**.

### Eigenschaften:
1. **$F(o) = o$**
	$F(o + o) = F(o) + F(o) = F(o)$, folgt direkt aus der [[Gruppenhomomorphismen#^9d8893|Gruppenhomomorphismuseigenschaft]]  $\square$ 

2. $F(\lambda_1 \cdot v_1 + ... + \lambda_n \cdot v_n) = \lambda_1 F(v_1) + ... + \lambda_n F(v_n)$
	Folgt aus der Expansion: $F(\lambda_1 \cdot v_1 + ... + \lambda_n v_n) = F(\lambda_1 \cdot (v_1 + ... + \frac{\lambda_n}{\lambda_1} \cdot v_n) = \lambda_1 F(v_1 + (... + \frac{\lambda_n}{\lambda_1} \cdot v_n))$ 
	$= \lambda_1 F(v_1) + \lambda_1 F(... +\frac{\lambda_n}{\lambda_1} \cdot v_n ) = \lambda_1 F(v_1) + F(... +\lambda_n \cdot v_n ) = ... = \lambda_1 F(v_1) + ... + \lambda_n F(v_n)$ $\square$

3. Ist $U$ ein Untervektorraum von $V$, dann ist $F(U)$ ein Untervektorraum von $W$.
	Beweis ist noch zu erbringen

4. Sind $v_1, ..., v_n$ linear abhängig in $V$, dann sind auch $F(v_1), ..., F(v_n)$ linear abhängig in $W$:
	Sind sie linear abhängig in $V$, dann gibt es Koeffizienten $\lambda_1, ..., \lambda_n$ mit mind. einem $\lambda_n \neq 0$ sodass die Linearkombination den Nullvektor ergibt, also:
	$F(\lambda_1 v_1 + ... + \lambda_n v_n) = F(o) = \lambda_1 F(v_1) + ... + \lambda_n F(v_n)$ nach 2.
	Und da wir aus 1. wissen, dass $F(o) = o$ ergibt die Linearkombination von $F(v_1), ..., F(v_n)$ auch hier den Nullvektor, und dies ebenfalls mit nichtrivialen Koeffizienten. $\square$

5.Sei $U$ ein Unterraum von $V$. Dann gilt: $dim(F(U)) \le dim(U)$:
	Beweis ist noch zu erbringen


#### Kompositionen linearer Abbildungen sind linear
Seien $F : V \rightarrow W$, $G: W \rightarrow U$  lineare Abbildungen. Dann ist auch $G \circ F$ linear.
##### Beweis:
Damit $G \circ F = G(F(v))$ linear ist, muss gelten:
$G(F(\lambda v + w)) = \lambda G(F(v)) + G(F(w))$
Durch die Linearität von $F$ wissen wir:
$G(F(\lambda v + w)) = G(\lambda F(v) + F(w))$
Und dann durch die Linearität von $G$:
$G(\lambda F(v) + F(w)) = \lambda G(F(v)) + G(F(w))$ $\square$

#### Vektorraum der Homomorphismen:
Die Menge aller Vektorraumhomomorphismen $Hom(V,W)$ ist ein Untervektorraum von $Abb(V, W) = W^V$  .
##### Beweis:
Hier müssen lediglich die [[Untervektorräume|Untervektorraumaxiome]] gelten:
1. Die Nullabbildung $F(v) = 0$ ist linear, also in $Hom(V,W)$ enthalten.
2. Es ist abgeschlossen, da die Summe zweier linearen Abbildungen ebenfalls linear ist:
	$(F + G)(\lambda v + w) = F(\lambda v + w) + G(\lambda v + w) = \lambda F(v) + F(w) + \lambda G(v) + G(w)$ 
	$= \lambda (F(v) + G(v)) + F(w) + G(w) \lambda (F + G)(v) + (F + G)(w)$
3. 

