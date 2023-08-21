Sei $B = (v_1, ..., v_n)$ eine Basis von $v$ und $w = v_1 \lambda_1 + ... + \lambda_n v_n$ mit $\lambda_i \neq 0$ . Dann ist $B' = (w, v_1, ..., v_{i - 1}, v_{i + 1}, ..., v_n)$ eine Basis von $V$ .

## Beweis:
Beweis durch zeigen der [[Basen|Basiseigenschaften]]:
	1. $span(B') = V$:
	Nehme man ein beliebiges $v \in V$. Dann ist:
	$v = \mu_1 v_1 + ... + \mu_i v_i + ... + \mu_n v_n$ 
	Durch $w = v_1 \lambda_1 + ... + \lambda_n v_n$  wissen wir, dass durch $\lambda_i \neq 0$ 
	$v_i = \frac{w}{\lambda_i} - ... - \frac{\lambda_n v_n}{\lambda_i}$ 
	Somit ist $v = \mu_1 v_1 + ... + \mu_i (\frac{w}{\lambda_i} - ... - \frac{\lambda_n v_n}{\lambda_i}) + ... + \mu_n v_n$ 
	Und somit $span(B')$ auch $
