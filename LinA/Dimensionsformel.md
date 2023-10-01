Seien $V, W$ endlichdimensionale $K$-Vektorräume und $F: V \rightarrow W$ linear. Dann gilt: $dim V = dim(ker F) = dim(im F)$ 
# Beweis:
Sei $w_1, ..., w_r$ Basis von $im F$ sowie $v_1, ..., v_k$ Basis von $ker F$ sowie $F(u_i) = w_i$. Ist $v_1, ..., v_k, u_1, ..., u_r$ Basis von $V$, dann ist $dim V = k + r = dim(im F) + dim(ker F)$.

- $<v_1 , ..., v_k, u_1, ..., u_r > = V$:
	Sei $v \in V$ mit $F(v) = \mu_1 w_1 + ... + \mu_r w_r$ ein Vektor o.B.d.A. und $v' = \mu_1 u_1 + ... + \mu_r u_r \in V$. Dann ist $F(v - v') = o \implies v - v' \in ker F$, sodass $v - v' = \lambda_1 v_1 + ... \lambda_k v_k$
	$\Leftrightarrow v = \lambda_1 v_ 1+ ... \lambda_k v_k + \mu_1 u_1 + ... + \mu_r u_r \in <v_1, ..., v_k, u_1, ..., u_r$ 

- $v_1, ..., v_k, u_1, ..., u_r$ linear unabhängig:
	Sei $\lambda_1 v_1 + ... + \lambda_k v_k + \mu_1 u_1 + ... + \mu_r u_r = o$ $\implies \lambda_1 v_1 + ... + \lambda_k v_k + \mu_1 u_1 + ... + \mu_r u_r \in ker F$
	Dann ist $F(\lambda_1 v_1 + ... + \lambda_k v_k + \mu_1 u_1 + ... + \mu_r u_r) = \lambda_1 0 + ... + \lambda_k 0 + \mu_1 w_1 + ... + \mu_r w_r = o$
	$\implies \mu_1 = ... = \mu_r = 0$ aus der linearen Unabhängigkeit der $w_i$
	Oben eingesetzt:
	$\lambda_1 v_1 + ... \lambda_k v_k + 0 u_1 + ... + 0 u_r = 0 \implies \lambda_1 = ... = \lambda_k = 0$ 
	Aus beiden Implikationen zusammen gewinnt sich dann die lin. Unabh.
  $\square$ 
# Faserfolgerung:
Für jede Faser $F^{-1}(w)$ von $F: V \rightarrow W$ gilt:
$dim(F^{-1}(w)) = dim(v_0 + ker F) = dim(ker F) = dim(V) - dim(im F)$

Beweis:
	Nach der [[Faserung eines Vektorraumes]] ergibt sich die erste Gleichheit.
	Die zweite ergibt sich ebenfalls aus dieser, da $v_0 + ker F = \{v_0 + v | v \in ker F\}$, sodass $v_1, ..., v_r$ genau dann linear unabhängig sind, wenn $\lambda_1 (v_0 + v_1) + ... + \lambda_r (v_0 + v_r) = \lambda_1 v_1 + ... + \lambda_r v_r + (\lambda_1 + ... + \lambda_r) v_0 = 0$
	$\implies \lambda_1 = ... = \lambda_r = 0$.
	

# Endomorphismusrelationen:
