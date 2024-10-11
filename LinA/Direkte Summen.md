Ein [[Vektorraum]] heißt direkte Summe seiner zwei Untervektorräume $U_1, U_2$, wenn
- $V = U_1 + U_2$
- $U_1 \cap U_2 = \{o\}$ 
und man dann $V = U_1 \oplus U_2$ schreibt.
# Existenz komplementärer Unterräume:
Sei $U$ ein Untervektorraum von $V$. Dann gibt es einen **komplementären Unterraum** $U'$ mit $U \oplus U' = V$. 

Beweis:
	Sei $v_1, ..., v_s$ eine Basis von $U$. Dann kann diese durch $w_1, ..., w_t$ nach dem [[Basisaustauschlemma|Basisaustauschsatz]] zu einer Basis $v_1, ..., v_s, w_1, ..., w_t$ von $U'$ ergänzt werden. Setze man nun $B' = <w_1, ..., w_t>$, sodass offensichtlich $U + U' = V$.
	Und weil $v_1, ..., v_s, w_1, ..., w_t$ linear unabhängig ist, folgt aus $v = \lambda_1 v_1 + ... \lambda_s v_s = \mu_1 w_1 + ... + \mu_t w_t$, also $v \in <B> = U \cap <B>' = U'$, $v = o$.

# Beispiele für direkte Summen:
$R^3 = <e_1> + <e_2> + <e_3>$
$R^3 = \{(a, 0, 0) |a \in R \} \oplus \{(0, b, c) | b,c \in R \}$ 