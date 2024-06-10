Die Elementarmatrizen sind eine Moeglichkeit, [[Zeilenraum und Zeilenumformungen einer Matrix|Zeilenumformungen]] als Komposition von [[Matrizen als Lineare Abbildungen|Matrizen]] darzustellen. 

Sei dabei $\Delta_{ij}$ die Matrix, die nur an $i,j$ den Wert $1$ und sonst den Wert $0$ besitzt. Sei weiter $i \le m$ und $i \neq j$ sowie $\lambda \in K*$, dann definiert man:
$S_i(\lambda) := I_m + (\lambda - 1)\Delta_{ii}$ 
$Q_i^j := I_m + \Delta_{ij}$
$Q_i^j(\lambda) := I_m + \lambda \Delta_{ij}$ 
$P_i^j := I_m - \Delta_{ii} + \Delta_{ij} - \Delta_{jj} + \Delta_{ij}$

Dabei koennen die vier Zeilenumformungen durch diese sog. Elementarmatrizen bei linksseitiger Multiplikation zu einer Matrix durchgefuehrt werden.

### Fuer Spaltenumformungen
Spaltenumformungen lassen sich analog ueber die rechtsseitige Multiplikation mit der jeweiligen Elementarmatrix darstellen. Dabei ist jedoch die Bedeutung von $i$ und $j$ vertauscht: $Q_i^j$ etwa ist die Addition der $i$-ten Spalte zur $j$-ten Spalte. 

## Darstellung durcheinander:
Dabei ist $Q_i^j(\lambda) = S_i(\lambda^{-1})Q_i^jS_i(\lambda)$ und $P_i^j = S_j(-1)Q_i^jQ_j^i(-1)Q_i^j$.

## Invertierbarkeit der Elementarmatrizen
Die Inversen der Elementarmatrizen sind aehnlich der [[Zeilenraum und Zeilenumformungen einer Matrix|Zeilenumformungen]] darstellbar durch:
$(S_i(\lambda))^{-1} = S_i(\lambda^{-1})$
$(Q_i^j(\lambda))^{-1} = Q_i^j(-\lambda)$
$(P_i^j)^{-1} = P_i^j$
# Darstellbarkeit durch Elementarmatrizen
Jede Matrix $A \in GL(n)$ ist als Produkt von Elementarmatrizen darstellbar.

Bew.:
	Aus $A$ kann durch Zeilenumformungen eine aequivalente Matrix in Zeilenstufenform erzeugt werden, wodurch durch die Invertierbarkeit alle Diagonalkoeffizienten $\neq 0$ sind. Weiter laesst sich durch weitere Umformungen die Identitaetsmatrix erzeugen. So gilt: $T \cdot A = I_n$, woraus durch die Invertierbarkeit der Elementarmatrizen folgt: $A = T^{-1} I_n$, wobei $T$ eine Komposition von Elementarmatrizen darstellt.

