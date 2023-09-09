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
$A_F(e_j) = (\phi^{-1}_B \circ F \circ \phi_A)(e_j) = \phi_B^{-1}(F(\phi_A))$
$= \phi_B^{-1}(F(v_j))$   Nach obiger Definition von $\phi_A$ als Isomorphismus
$= \phi_B^{-1}(\sum_1^n a_{ij} w_i)$  Darstellbarkeit des Bildes durch Linearkombination
$= \sum_1^n a_{ij} \cdot \phi_B^{-1}(w_i)$ Definition lineare Abbildung
$= \sum_1^n a_{ij} \cdot e_i$ Nach obiger Definition von $\phi_B$ als Isomorphismus

Betrachte man nun entgegengesetzt, wie man $F$ aus $A_F$ darstellen kann:
$F(v) = F(\lambda_1 v_1 + … + \lambda_n v_n) = (\phi_B \circ A_F \circ \phi_A^{-1})(\lambda_1 v_1 + … + \lambda_n v_n)$
$= $
Nach dem [[Fundamentalsatz für endlichdimensionale Vektorräume]] kann jeder Vektor $v$ bez. einer Basis dargestellt werden durch den Tupelvektor seiner Basislinearkombinationskoeffizienten, d.h. Durch $(\lambda_1, …, \lambda_n)$, sodass
$= (\phi_B \circ A_F)(\lambda_1, …, \lambda_n)$ durch das [[Darstellungslemma von Körpervektorräumen]]
$= \phi_B \circ (\begin{pmatrix} | & … & | \\ F(e_1) & … & F(e_n) \\ | & … & | \end{pmatrix} \begin{pmatrix} \lambda_1 \\ … \\ \lambda_n \end{pmatrix})$
$= \phi_B \circ (\lambda_1 F(e_1) + … + \lambda_n F(e_n))$
Nutze man den [[Fundamentalsatz für endlichdimensionale Vektorräume]] erneut, wobei $\phi_B (F(e_1)) = \phi_B()$
$= \lambda $ 
$= \begin{pmatrix}  \end{pmatrix} \begin{pmatrix} \lambda_1 \\ … \\ \lambda_n \end{pmatrix}$








