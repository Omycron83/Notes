Da [[Basen haben gleiche Länge|endliche Basen gleiche Kardinalität besitzen]] und Vektorräume in ihrer Gesamtheit durch ihre Basis charakterisiert werden können liegt es nahe, einen Dimensionsbegriff zu formulieren:

$dim_K(V) = n \; \text{(falls V eine Basis mit n Elementen besitzt)}, \infty \, \text{(sonst)}$ 

### Dimensionsüberhöhung $\implies$ lineare Abhängigkeit
Sei $w_1, ..., w_r$ eine Familie mit $r > dim(V)$ . Dann ist diese Familie linear abhängig.

Beweis:
	Nehme man eine Basis $v_1, ..., v_n$ mit $r > n$ .
	Da $w_1, ..., w_r$ linear unabhängig ist, müsste auch $w_1, ..., w_n$ linear unabhängig sein. Und nach [[Basen haben gleiche Länge#^70f7dd|diesem Lemma]] würde diese Teilfamilie dann eine Basis konstituieren. Dann wäre sie aber auch [[Basen#^80a43c|maximal linear unabhängig]] und somit zusammen mit der Gegenf