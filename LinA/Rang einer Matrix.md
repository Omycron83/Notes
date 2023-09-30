Sei $A \in K^{m \times n}$ eine [[Matrizen|Matrix]], dann ist der [[Rang einer linearen Abbildung|Rang]] der von $A$ characterisierten [[Lineare Abbildungen|linearen Abbildung]] die Dimension des von den Spalten $a_1, ..., a_n$ von $A$ [[Lineare Erzeugnisse & Unabhängigkeit|erzeugten]] [[Untervektorräume|Untervektorraumes]] von $K^m$, den man auch **Spaltenrang nennt**.
Dies gilt, da $im A = <a_1, ..., a_n>$ .

Beweis:
	$im A \subset <a_1, ..., a_n>$:
	Sei $y \in im A$. Dann gibt es ein $x \in K^n$ mit $y = A \cdot x = a_1 x_1 + ... a_n x_n \in <a_1, ..., a_n>$ 
	$<a_1, ..., a_n> \subset im A$:
	Es ist $a_i \in im A$, da $A \cdot e_i = a_i \in Im A$. Und da dann $a_1, ..., a_n \in Im A$ auch durch Vektorreigenschaft  $<a_1, ..., a_n> \subset im A$.

## Zeilenrang = Spaltenrang:
Wir wissen, dass Spalten $a_1, ..., a_r$ (mit $dim(im(A)) = r$) eine Basis bilden. 