Je zwei Basen eines endlich-erzeugten Vektorraumes $V$ haben dieselbe Anzahl von Basenelementen. 

# Beweis:
Sei $V$ ein endlichdimensionaler Vektorraum. Nehme man nun zwei Basen $B = (v_1, ..., v_n)$ und $B' = (w_1, ..., w_m)$ mit $m \le n$ . Dann kann man nach dem [[Austauschsatz von Steinitz]], da $B'$ insbesondere linear unabhängig ist, eine Basis $(w_1, ..., w_m, v_{m + 1}, ..., v_n)$ konstruieren. 
Jedoch wissen wir, dass Basen, wie $B'$, [[Basen#^80a43c|unverlängerbar sind]], da sie sonst linear abhängig würden. So muss $m = n$ gelten.

### Linear Unabhängig + Basenlänge <-> Basis

^70f7dd

Sei eine Familie $w_1, ..., w_n$ gleichmächtig einer Basis $v_1, ..., v_n$ und gleichzeitig linear unabhängig. Dann handelt es sich bei dieser Famile ebenfalls um eine Basis.

Beweis:
	Nach dem [[Austauschsatz von Steinitz]] müsste man $n - n = 0$ Basiselemente dazuwählen, damit es sich bei der Familie um eine Basis handelt, wodurch sie eine Basis konstituiert.
