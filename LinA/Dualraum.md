Sei $V$ ein $K$-[[Vektorraum]]. Eine lineare Abbildung $\alpha: V \rightarrow K$ heisst **Linearform**. $Hom(V, K)$ nennt man weiter den **Dualraum** von $V$, bezeichnet mit $V^*$.

# Duale Abbildung:
Eine lineare Abbildung $F: U \rightarrow V$ definiert eine **duale Abbildung** $F^*: V^* \rightarrow U^*, a \mapsto a \circ F$, sodass das Diagramm ![[Pasted image 20231031223336.png]]
fuer alle $\alpha \in V^*$ kommutiert.

Sei konkret $U = V = K^n$ Spaltenvektoren und $A_F \in K^{n \times n}$ eine [[Matrizen als Lineare Abbildungen|darstellende Matrix]] der linearen Abbildung $F$. Dann ist $\alpha \in K^{1 \times n}$ ein Zeilenvektor und $A_F^*(\alpha) = \alpha \cdot A_F$ wieder eine Zeile.