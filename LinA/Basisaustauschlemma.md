Sei $B = (v_1, ..., v_n)$ eine Basis von $V$ und $v = v_1 \lambda_1 + ... + \lambda_n v_n$ mit $\lambda_i \neq 0$ . Dann ist $B' = (v_1, ..., v_{i - 1}, v, v_{i + 1}, ..., v_n)$ eine Basis von $V$ .

## Beweis:
Beweis durch zeigen der [[Basen|Basiseigenschaften]]:
	1. $span(B') = V$:
	Nehme man ein beliebiges $v \in V$. Dann ist:
	$v = \mu_1 v_1 + ... + \mu_i v_i + ... + \mu_n v_n$ 
	Durch $w = v_1 \lambda_1 + ... + \lambda_n v_n$  wissen wir, dass durch $\lambda_i \neq 0$ 
	$v_i = \frac{w}{\lambda_i} - ... - \frac{\lambda_n v_n}{\lambda_i}$ 
	Somit ist $v = \mu_1 v_1 + ... + \mu_i (\frac{w}{\lambda_i} - ... - \frac{\lambda_n v_n}{\lambda_i}) + ... + \mu_n v_n$ 
	Und somit $span(B')$ auch $V$
	2. $B'$ ist linear unabhängig:
	Dann wüsstem man, dass
	$o = \phi_i w + \phi_1 v_1 + ... \phi_n v_n \implies \phi_1 = ... = \phi_n = 0$.
	Nun kann man einsetzen:
	$o = \phi_i (v_1 \lambda_1 + ... + \lambda_n v_n) + \phi_1 v_1 + ... \phi_n v_n \implies \phi_1 = ... = \phi_n = 0$
	$\Leftrightarrow o = \phi_i \lambda_i v_i + (\phi_1 + \phi_i \lambda_1)v_1 + ... (\phi_n + \phi_i \lambda_n) v_n \implies \phi_1 = ... = \phi_n = 0$
	Da $v_1, ..., v_n$ linear unabhängig sind, gilt:
	$\phi_i \lambda_i v_i = (\phi_1 + \phi_i \lambda_1) = ... = (\phi_n + \phi_i \lambda_n) = 0$ 
	Und da $\lambda_i \neq 0$ durch Vorraussetzung:
	$\phi_i = 0$
	und somit auch $\phi_1 = ... = \phi_n = 0$ 




