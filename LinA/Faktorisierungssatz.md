Sei $F: V \rightarrow W$, dann gibt es einen Untervektorraum $U$ von $V$ mit $V = U \oplus ker F$, sodass der Vektorraum als [[Direkte Summen|direkte Summe]] von [[Untervektorräume|Untervektorraum]] und [[Kern einer linearen Abbildung|Kern]] darstellbar ist und es einen [[Lineare Abbildungen#^d82a1b|Isomorphismus]] $F|_U: U \rightarrow im F$ gibt.
# Beweis:
Der Beweis geht aus der [[Dimensionsformel]] hervor: $dim V = dim ker F + dim Im F$. Betrachte man also eine Basis $B = v_1, ..., v_r, u_1, ..., u_k$ von $V$, wobei $v_1, ..., v_r$ eine Basis von $ker F$ ist. Dann kann man $U = <u_1, ..., u_k>$ setzen. Und da dann somit $U$ und $im F$ dieselbe Dimension haben folgt aus dem [[Fundamentalsatz für endlichdimensionale Vektorräume]] die Isomorphie und somit die Existen eines Isomorphismus.
# Beispiel:
- Betrachte man $F(x, y) = (y, y)$: 
	Der Kern der Abbildung ist $(x, 0)$ 
	Wähle man nun $U = \{(0, y)\}$. 
	Dann ist $F|_U (0, y) = (y, y)$ ein Isomorphismus.  
	Achtung!: $U$ ist nicht eindeutig, man hätte auch $W  = \{(y, y)\}$ wählen können.
