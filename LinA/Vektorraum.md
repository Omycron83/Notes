## Definition:
Eine [[Gruppen#^b82401 |abel'sche Gruppe]] $(V, +)$ mit der Addition als Verknüpfung ist ein Vektorraum über einem [[Körper]] $(K, \dotplus, *)$, wenn eine **Skalarmultiplikation** $\cdot : K \times V \rightarrow V, (\lambda, v) \mapsto v$  wohldefiniert ist und:
1. Das **Distributivgesetz für Skalare** gilt: $(\lambda \dotplus \mu) \cdot v = \lambda \cdot v + \mu \cdot v$  
2. Das **Distributivgesetz für Vektoren** gilt: $\lambda \cdot (v + w) = \lambda \cdot v + \lambda \cdot v$ 
3. Das **Assozativgesetz zwischen Vektoren und Skalaren** gilt: $(\lambda * \mu) \cdot v = \lambda \cdot (\mu \cdot v)$  
4. Das **Eins-Element des Körpers neutral in der Skalarmultiplikation** ist: $1 \cdot v = v$

Dabei nennt man die Körperelemente **Skalare** und die **Gruppenelemente** Vektoren.
### Eigenschaften:
1. $0 \cdot v = o$ : 
	$0 \cdot v = (0 + 0) \cdot v = 0 \cdot v + 0 \cdot v \implies 0 \cdot v = o$  Nur das Neutrale addiert zu sich selbst. $\square$ 
		Alternativer Beweis: $v = 1 \cdot v \Leftrightarrow v = (1 + 0)\cdot v \Leftrightarrow 1 \cdot v + 0 \cdot v = v \Leftrightarrow 0 \cdot v = o$ 
2. $(-1) \cdot v = -v$
	$o = 0 \cdot v = (1 - 1) \cdot v = v + (-1) \cdot v \Leftrightarrow (-1) \cdot v = -v$ $\square$ 
3. $\lambda \cdot o = o$ 
	$\lambda \cdot o = \lambda \cdot (v - v) = \lambda \cdot v - \lambda \cdot v = (\lambda - \lambda) \cdot v = 0 \cdot v = o$  $\square$ 
4. $\lambda \cdot v = o \implies v = o \lor \lambda = 0$
	1. $\lambda \neq 0: \Leftrightarrow \lambda^{-1} * \lambda \cdot v = \lambda^{-1} \cdot o \Leftrightarrow v = o$
	2. $v \neq o :$ Wäre $\lambda \neq 0$, dann könnte man mit dessen inversen Multiplizieren, sodass $v = o$, was i.A. einen Widerspruch bildet. Sodass dann $\lambda = 0$ $\square$ 
## Beispiele:
1. Der $K^n$ als Menge der $n$-Tupel mit der elementweisen Addition und Skalarmultiplikation erfüllt als typischer $n$-Vektorraum aus dem Tupelkörper induziert alle Vektorraumeigenschaften ^6e22e7
2. Jeder Köper ist ein Vektorraum über sich selbst., bzw. über einem seiner beliebigen Untervektorräume.
3. Der $P(R^2)$ mit der symmetrischen Differenz $\Delta$ und der Multiplikation mit $0, 1$ wobei $M \cdot 0 = \emptyset$ und $M \cdot 1 = M$.
4. $\{0\}$ über $R$.
5. 

10 Minuten abstrakter Vektorraum über $R$ vorstellen? 

 Kein Vektorraum: