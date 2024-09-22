Nach dem [[Darstellungssatz endlichdimensionaler Vektorräume]] lässt sich jede lineare Abbildung eindeutig durch eine Matrix charakterisieren, die in den Spalten die Bilder der Darstellungskoeffizienten der Basisbilder besitzt. 
Die zugrundeliegende lineare Abbildung kann dann dargestellt werden als $K^{dimV} \rightarrow K^{dimW}, v \mapsto A \cdot v$, wobei man auf das Argument und den Ergebnisvektor den [[Fundamentalsatz für endlichdimensionale Vektorräume|Körperisomorphismus]] $\phi_B$ anwendet, um mit $u \mapsto \phi_B(A \cdot \phi_B^{-1}(u))$ eine lineare Abbildung von $V \rightarrow W$ zu erhalten.
Für die Menge aller Matrizen, die [[Lineare Abbildungen]] zwischen zwei [[Vektorraum|Vektorräumen]] $V, W$ charakterisieren, schreibt man auch $M(V, W)$. 

Dabei gilt insbesondere insbesondere für $\forall M \in M(V, W) \subset K^{dim V \times dimW}$, dass die Bildvektoren [[Lineare Erzeugnisse & Unabhängigkeit|linear unabhängig]] sind. 

Redo:
# $M(V, W) <-> Hom(V, W)$
Mit dem [[Darstellungssatz endlichdimensionaler Vektorräume]] ist die Injektion gezeigt: es gibt eine Abbildung, die jeder [[Lineare Abbildungen|linearen Abbildung]] genau eine Matrixdarstellung zuordnet. Es bleibt zu zeigen, dass diese außerdem eine Surjektion und somit eine Bijektion darstellt, also auch jeder Matrix eine lineare Abbildung zugeordnet wird, was aus der Definition von $M(V, W)$ folgt.

Somit handelt es sich um eine Bijektion zwischen den Mengen. 

# Bild einer Matrixdarstellung:
Das Bild einer Matrixdarstellung entspricht dem Erzeugniss der Spaltenvektoren, wobei man konventionell linear abhängige Vektoren herauslässt.
# Kern einer Matrixdarstellung:
Der [[Kern einer linearen Abbildung|Kern]] einer Matrixdarstellung bezeichnet alle Vektoren $v \in K^{dimV}$, sodass $A \cdot v = o$. Dies lässt sich über ein [[Lineare Gleichungssysteme|lineares Gleichungssystem]] lösen: 
- Gibt es nur eine Lösung, so ist diese die triviale mit dem Nullvektor
- Gibt es unendlich Lösungen, so gibt es $n > 0$ freie Variablen. Die Dimension des Kerns ist dann $n$. Man kann ihn an der Anzahl der generierbaren Nullzeilen ablesen.
# Rang einer Matrixdarstellung
Sei $A \in K^{m \times n}$ eine [[Matrizen|Matrix]], dann ist der [[Rang einer linearen Abbildung|Rang]] der von $A$ characterisierten [[Lineare Abbildungen|linearen Abbildung]] die Dimension des von den Spalten $a_1, ..., a_n$ von $A$ [[Lineare Erzeugnisse & Unabhängigkeit|erzeugten]] [[Untervektorräume|Untervektorraumes]] von $K^m$, den man auch **Spaltenrang nennt**.
Dies gilt, da $im A = <a_1, ..., a_n>$ .

Beweis:
	$im A \subset <a_1, ..., a_n>$:
	Sei $y \in im A$. Dann gibt es ein $x \in K^n$ mit $y = A \cdot x = a_1 x_1 + ... a_n x_n \in <a_1, ..., a_n>$ 
	$<a_1, ..., a_n> \subset im A$:
	Es ist $a_i \in im A$, da $A \cdot e_i = a_i \in Im A$. Und da dann $a_1, ..., a_n \in Im A$ auch durch Vektorreigenschaft  $<a_1, ..., a_n> \subset im A$.

Dabei ist eine Matrix teil der [[Gruppe der invertierbaren Matrizen]], wenn $rg(A) \neq 0$ und $A \in K^{n \times n}$.

## Zeilenrang = Spaltenrang:
Der Spaltenrang einer Matrix, d.h. die Dimension des von den Spaltenvektoren erzeugten [[Lineare Erzeugnisse & Unabhängigkeit#^2f6e6d|Unterraumes]] ist gleich dem Zeilenrang einer Matrix, d.h. der Dimension des von den Zeilenvektoren erzeugten Unterraumes.

Beweis:
	Ausstehend

# Multiplikation entspricht Komposition
^4c7df6
Seien $A, B$ zwei Matrizen, die lineare Abbildungen $F: V \rightarrow W, G: W \rightarrow L$ darstellen. Dann ist $\phi_B^{-1}((G \circ F)(v)) = G\cdot F\cdot\phi_B(v)$

# Darstellungsmatrizen von Isomorphismen:
^2428c8
Sei $A$ ein Isomorphismus, also eine Matrix, die [[Lineare Abbildungen]] darstellt und zusaetzlich [[Gruppe der invertierbaren Matrizen|invertierbar ist]]. Dann stellt diese auch einen Isomorphismus dar, wobei durch die [[Dimensionsformel]] mit einer weiteren Matrix $B$ gilt:
- $rg(A \cdot B) \leq min(rg(A), rg(B))$
- $rg(A) + rg(B) - n \le rg(A \cdot B)$
