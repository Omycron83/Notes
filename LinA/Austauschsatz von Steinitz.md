Sei $B = (v_1, ..., v_n)$ eine Basis von V und $C = (w_1, ..., w_m)$ eine weitere [[Familien|Familie]] linear unabhängiger Vektoren. Dann kann man $n-m$ Vektoren so wählen, dass $(w_1, ..., w_m, v_{m+1}, ..., v_n)$eine Basis von $V$ ist.

# Beweis:
Per vollständige Induktion:
	I.A.: m = 0 ist trivial
	I.S.: da $(w_1, ..., w_{m-1}) \subset (w_1, ..., w_m)$ linear unabhängig ist, und nach der I.A. bei geeigneter Nummerierung $(w_1, ..., w_{m-1}, v_m, ..., v_n)$ eine Basis ist, kann man nun $w_m$ als $w_m = \lambda_1 w_1 + ... + \lambda_{m-1} w_{m-1} + \lambda_m v_m + ... + \lambda_n v_n$ darstellen.
	
