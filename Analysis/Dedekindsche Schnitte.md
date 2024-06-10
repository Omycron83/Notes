Seien $A, B \subset R$. Dann nennt man $(A, B)$ **Dedekindschen Schnitt** und schreibt $(A | B)$, wenn gilt:
1. $A, B \neq \emptyset$
2. $A \cup B = R$
3. $\forall a \in A \forall b \in B: b > a$ 

## Lemma: $A$ und $B$ sind disjunkt:
Dabei gilt insbesondere, dass $A \cap B = \emptyset$ gilt, da es sonst ein $c \in A, c \in B$ gibt, jedoch nach Definition dann $c < c$ gelten müsste.
# Trennungszahl:
Ein $t \in R$ heißt Trennungszahl, falls $a \le t \le b \forall a \in A, b \in B$ eines Dedekindschen Schnittes gilt.
# Schnittaxiom:
Jeder Dedekindsche Schnitt $(A|B)$ besitzt genau eine Trennungszahl.
# Form eines Dedekindschen Schnittes:
Für jeden Dedekindschen Schnitt $(A|B)$ gibt es genau ein $t \in R$, sodass $A$ und $B$ genau eine von zwei Formen haben:
1. $A = \{x \in R | x < t\}, B = \{x \in R | x \ge t\}$
2. $A = \{x \in R|x \le t\}, B = \{x \in R| x > t \}$

Beweis:
	Sei $(A|B)$ ein Dedekindscher Schnitt. Das Schnittaxiom besagt, dass $t$ eindeutig ist. Da $t \in R$ und $R = A \cup B$ muss aufgrund der disjunktheit entweder $t \in A$ oder $t \in B$ gelten. Wenn $t \in A$ gilt, so muss insbesondere $b > t \forall b \in B$ gelten, und außerdem $t$ selbst in $A$ enthalten sein, wodurch in $A$ nach Definition $a \le t$ gilt. Selbiges gilt umgekehrt für $t \in B$. 

# Anwendung:
## Erweiterung um irrationale Zahlen:
Betrachte man $A = R_{< 0} \cup \{a \in R_{\ge 0} | a \cdot a \le 2 \}, B = \{b \in R_{\ge 0} | a \cdot a > 2\}$.
Dann muss nach dem Schnittaxiom ebenfalls $a > 0$ mit $a \cdot a = 2$ eine Trennungszahl bilden und so $\in R$ sein. Da wir aus der Schule wissen, dass diese Zahl irrational ist, können wir die reellen Zahlen 'um diese Erweitern'.