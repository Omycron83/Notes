Sei $F: V \rightarrow W$ linear, wobei $w \in im F$, es also ein $v_0 \in V$ mit $F(v_0) = w$ gibt. Die [[Faser einer linearen Abbildung|Faser]] über $w$ kann dann auch dargestellt werden als:
$F^{-1}(w) = v_0 + ker F = \{v_0 + v | v \in ker F\}$ 

Beweis:
	z.Z.: $\{ v \in V | F(v) = w \} = \{v_0 + v | v \in ker F , F(v_0) = w\}$
	$\{ v \in V | F(v) = w \} \subset \{v_0 + v | v \in ker F , F(v_0) = w\}$:
	Sei $u \in F^{-1}(w)$, d.h. $F(u) = w = F(v_0)$. Dann ist $F(u) - F(v_0) = F(u - v_0) = o$, wodurch also $u - v_0 \in ker F$ und so $u = v_0 + (u - v_0) \in v_0 + ker F$. 
	$\{v_0 + v | v \in ker F , F(v_0) = w\} \subset  \{ v \in V | F(v) = w \}$:
	Sei $F(v_0 + v) = F(v_0) + F(v) = w + o = w$ , also $v_0 + v \in F^{-1} (v)$. 
	