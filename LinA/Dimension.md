Da [[Basen haben gleiche Länge|endliche Basen gleiche Kardinalität besitzen]] und Vektorräume in ihrer Gesamtheit durch ihre Basis charakterisiert werden können liegt es nahe, einen Dimensionsbegriff zu formulieren:

$dim_K(V) = n \; \text{(falls V eine Basis mit n Elementen besitzt)}, \infty \, \text{(sonst)}$ 

### Dimensionsüberhöhung $\implies$ lineare Abhängigkeit
Sei $w_1, ..., w_r$ eine Familie mit $r > dim(V)$ . Dann ist diese Familie linear abhängig.

Beweis:
	Nehme man eine Basis $v_1, ..., v_n$ mit $r > n$ .
	Da $w_1, ..., w_r$ linear unabhängig ist, müsste auch $w_1, ..., w_n$ linear unabhängig sein. Und nach [[Basen haben gleiche Länge#^70f7dd|diesem Lemma]] würde diese Teilfamilie dann eine Basis konstituieren. Dann wäre sie aber auch [[Basen#^80a43c|maximal linear unabhängig]] und somit zusammen mit der Gegenfamilie linear abhängig.

### Dimension von Unterräumen:
Sei $W \subset V$ ein [[Untervektorräume|Untervektorraum]]. Dann gilt:
1. $dim(W) \le dim(V)$ 
2. $dim(W) = dim(V) \Leftrightarrow W = V$ 
Beweis:
	1. Jede mögliche Basis von $W$ kann maximal die Länge einer Basis von $V$ haben, da sie, wenn sie in $W$ linear unabhängig ist, auch in $V$ linear unabhängig ist.
		1. Gehe man davon aus, es gäbe eine Basis $B'$ von $W$ mit $<B'> \neq V$ (notwendig damit der [[Untervektorräume#^abb4a8|Untervektorraum abgeschlossen ist]]. Dann gibt es mindestens ein $v \in V \backslash W \not \in <B'>$ . Somit wäre $B' \cup \{v \}$ linear unabhängig, was jedoch nicht möglich ist da Basen [[Basen#^80a43c|maximal linear unabhängig]] sind und $dim(W) = dim(V)$ ist.