Das **Bild** $F(V) := imF \{ w \in W | \exists v \in V: f(v) = w \} \subset W$ einer [[Lineare Abbildungen|linearen Abbildung]] $F: V \rightarrow W$ ist die Menge aller angenommenen Abbildungswerte. 

# Eigenschaften
## $imF$ ist ein Untervektorraum
Sei $F$ eine lineare Abbildung. Dann gilt: $im \; F \subset W$ ist ein [[Untervektorräume|Untervektorraum]] von $W$.
	Beweis: Untervektorraumaxiome abklappern: ^235c98
	1. $F(o) = o \in im \; F$
	2. $F(v), F(w) \in im \; F \implies F(v) + F(w) = F(v + w) \in im \; F$ nach linearer Abbildungsdefinition
	3. $\lambda F(v) \in im \; F \implies \lambda F(v) = F(\lambda v) \in im \; F$ nach linearer Abbildungsdefinition

## $F$ surjektiv $\Leftrightarrow imF = W$   
$F$ [[Abbildungen#^4b4823|surjektiv]] $\Leftrightarrow$ $im \; F = W$. 
	Beweis: Per Definition
