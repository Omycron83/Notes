Sei $V$ ein $K$-Vektorraum mit der Basis $B = (v_1, ..., v_n)$. Dann gibt es einen eindeutigen
Isomorphismus $\phi_B : K^n \rightarrow V, \phi_B(e_i) = v_i$. 
Jeder Vektorraum $V$ ist also strukturell gleich zu seinem $K^n$, und so sind **endlichdimensionale Vektorräume gleicher Dimension isomorph** (dies folgt außerdem aus den Zusätzen des [[Satz der linearen Fortsetzung]]).

# Beweis:
Der Beweis folgt aus dem [[Satz der linearen Fortsetzung]], zumindest was die Eindeutigkeit, Existenz und Injektivität angeht. Daraus, dass die Familie $B$ eine Basis ist und die Einheitsvektoren $e_i$die kanonische Basis des $K^n$ darstellen kann man die Surjektivität zeigen:
Sei $v \in V$ ein beliebiger Vektor. Dann lässt sich dieser aus der Linearkombination der Basisvektoren darstellen: $v = \lambda_1 v_1 + … + \lambda_n v_n = \lambda_1 \phi_B(e_1) + … + \lambda_n \phi_B(e_n) = \phi_B(\lambda_1 e_1 + … + \lambda_n e_n)$.  Da die Basis $e_1, …, e_n$ den gesamten $K^n$ aufspannt ist die Abbildung auch offensichtlich Surjektiv.
Aus der Injektivität und Surjektivität folgt die Bijektivität und so der Isomorphismusstatus des Vektorraumhomomorphismus.

