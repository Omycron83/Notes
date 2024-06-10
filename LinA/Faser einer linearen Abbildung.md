Die Faser einer [[Lineare Abbildungen|linearen Abbildung]] über $w \in im \; F$ ist  $F^{-1}(w) := \{v \in V | F(v) = w \}$, also die Menge aller Vektoren die von $F: V \rightarrow W$ auf $w$ abgebildet werden.

# Eigenschaften
## $F^{-1}(w)$ bildet einen Untervektorraum:
Sei $F^{-1}(w)$ die Faser über $w$ einer linearen Abbildung 

## Dimension des Untervektorraumes:
Für jede Faser $F^{-1}(w)$ von $F: V \rightarrow W$ gilt:
$dim(F^{-1}(w)) = dim(v_0 + ker F) = dim(ker F) = dim(V) - dim(im F)$

Beweis:
	Nach der [[Faserung eines Vektorraumes]] ergibt sich die erste Gleichheit.
	Die zweite ergibt sich ebenfalls aus dieser, da $v_0 + ker F = \{v_0 + v | v \in ker F\}$, sodass $v_1, ..., v_r$ genau dann [[Lineare Erzeugnisse & Unabhängigkeit|linear unabhängig]] sind, wenn $\lambda_1 (v_0 + v_1) + ... + \lambda_r (v_0 + v_r) = \lambda_1 v_1 + ... + \lambda_r v_r + (\lambda_1 + ... + \lambda_r) v_0 = 0$
	$\implies \lambda_1 = ... = \lambda_r = 0$. (z.Z.)
	Aus der [[Dimensionsformel]] ergibt sich die letzte Gleichheit.
