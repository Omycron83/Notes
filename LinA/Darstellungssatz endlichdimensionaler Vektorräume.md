Seien $V, W$ Vektorräume über demselben Körper $K$ mit Basen $A = v_1, …, v_n$ und $B = w_1, …, w_m$. 
Dann existiert eine eindeutige Matrix $A \in K^{m \times n}$ die man auch **Darstellungsmatrix** der Abbildung $F$ bez. den Basen $A, B$ nennt und $A_F$ schreibt.
Diese Matrix enthält die Koeffiziententupel der Linearkombination der Basisbildvektoren aus den Bildbasen als Linearkombination, sodass
$F(v_j) = \sum_{i = 1}^n a_{i, j} w_i$.
# Beweis:
Durch den [[Fundamentalsatz für endlichdimensionale Vektorräume]] wissen wir, dass sich die beiden Vektorräume $V, W$ jeweils isomorph durch den $K^m$ und den $K^n$ darstellen lassen, jeweils mit Abbildungen $\phi_A : K^n  \rightarrow V, \phi_A(e_i) = v_i$ und $\phi_B : K^m \rightarrow V, \phi_B(e_i) = w_i$. 

Nach dem [[Darstellungslemma von Körpervektorräumen]] wisse man außerdem, dass sich der Homomorphismus zwischen den beiden Tupelkörpern durch eine Matrix $A_F \in K^{m \times n}$ darstelllen lässt.

Damit bildet sich das Diagramm:
![[Pasted image 20230903163303.png]]

Wobei $A_F$ darstellbar ist durch
$A_F(e_j) = \phi^{-1}_B \circ F \circ \phi_A)(e_j) = \phi_B^{-1}(F(\phi_A))$
$= \phi_B^{-1}(F(v_j))$   Nach obiger Definition von $\phi_A$ als Isomorphismus
$= \phi_B^{-1}(\sum_1^n a_{ij} w_i)$  Darstellbarkeit des Bildes durch Linearkombination
$= \sum_1^n a_{ij} \cdot \phi_B^{-1}(w_i)$ Definition lineare Abbildung
$= \sum_1^n a_{ij} \cdot e_i$ Nach obiger Definition von $\phi_B$ als Isomorphismus






