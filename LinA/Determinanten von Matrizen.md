Eine Abbildung $det: M(n \times n, K) \rightarrow K$ ist eine Determinante, wenn gilt:
- $det$ ist multilinear
- $det$ ist alternierend
- $det$ ist normiert, also gilt $det I_n = 1$
Dies ist eine Spezifizierung der [[Determinantenabbildungen]], wobei die Erweiterung der Normiertheit die Eindeutigkeit garantiert.

Dabei gibt es mehrere Moeglichkeiten zur [[Determinantenberechnung]] sowie [[Determinanteninterpretation]]. 

# Existenz und Eindeutigkeit
Die Determinante $det A$ einer Matrix $A \in K^{n \times n}$ ist eindeutig definiert.

Bew.:
	Man betrachte o.B.d.
# Eigenschaften:
Eine Determinante $det$ hat die folgenden Eigenschaften:
1. $\forall \lambda \in K: det(\lambda A) = \lambda^n det(A)$
2. Ist eine Zeile gleich $0$, so ist $det A = 0$
3. Entsteht $B$ durch $A$ durch [[Zeilenraum und Zeilenumformungen einer Matrix#^c76087|Zeilenvertauschung]], so gilt $det(A) = -det(B)$
4. Entsteht $B$ aus $A$ durch [[Zeilenraum und Zeilenumformungen einer Matrix#^ce7e9c|Zeilenumformung 3]], so gilt $det(A) = det(B)$
5. Ist $A$ eine Diagonalmatrix mit $A = \begin{pmatrix} \lambda_1 & .... & 0 \\ ... & ... & ... \\ 0 & ... & \lambda_n \end{pmatrix}$, so gilt $det(A) = \lambda_1 \cdot ... \cdot \lambda_n$
6. Ist $A$ eine Dreiecksmatrix mit $A = \begin{pmatrix} \lambda_1 & .... & c \\ ... & ... & ... \\ 0 & ... & \lambda_n \end{pmatrix}$, so gilt $det(A) = \lambda_1 \cdot ... \cdot \lambda_n$
7. $det A = 0 \Leftrightarrow rg A < n$ 
8. Sei $n \ge 2$ und $A \in M(n \times n, K)$ von der Gestalt $A = \begin{pmatrix} A_1 & C \\ 0 & A_2 \end{pmatrix}$, wobei $A_1$ und $A_2$ quadratisch sind. Dann ist $det A = det(A_1) \cdot det(A_2)$.
9. Es gilt $det(A \cdot B) = det(A) \cdot det(B)$ und insbesondere $det(A^{-1}) = det(A)^{-1}$ fuer $A \in GL(n \times n, K)$.
10. $det(A) = det(A^T)$

Beweis:
	1. Nach mehrmaliger Anwendung von dem ersten Axiom
	2. Weil $det(v_1, ..., v_n) = det(v_1, .., v_n) + det(0, ..., v_n)$ 
	3. $det(v_1, ..., v_n) + det(v_n, ..., v_1) = 0$ 
	4. $det(v_1 + \lambda v_n, ..., v_n) = det(v_1, ..., v_n) + \lambda det(v_n, ..., v_n)$
	5. Durch die multilinearitaet laesst sich jeder Faktor einmal herausziehen, woraus $\lambda_1 \cdot ... \lambda_n \cdot det(I_n) = \lambda_1 \cdot ... \lambda_n$ folgt
	6. Durch 4. laesst sich die Matrix auf 5. zurueckfuehren, falls $\lambda_i \neq 0$. Ist ein $\lambda_i$ ein auesserster Nulleintrag, so lassen sich die restlichen Zeilenelemente durch die $\lambda_{i + 1}, ..., \lambda_n$ ausrauemen, auch durch 2. auch hier die z.Z. Aussage gilt.
	7. Wir bringen die Matrix durch 3. und 4. auf Zeilenstufenform, sodass $det(A') = \pm det(A)$. Weiter ist $rg(A) = rg(A')$, sodass wegen 6. $rg(A) = n \Leftrightarrow \lambda_1 \cdot ... \cdot \lambda_n \neq 0$ gilt.
	8.  Man forme $A_1, A_2$ jeweils auf Zeilenstufenform mit $k$ und $l$ Zeilenvertauschungen um. Dann ist die neue Matrix $B = \begin{pmatrix} A_1' & C' \\ 0 & A_2'  \end{pmatrix}$, sodass $det(B) = det(A_1') \cdot det(A_2')$ nach 6., sodass weiter nach 3. gilt: $det(A) = (-1)^{k + l} det(A_1) det(A_2)$
	9. Folgt direkt aus der Darstellbarkeit mithilfe der [[Elementarmatrizen]], wobei im Falle $rg(A) < n$ auch $rg(A \cdot B) < n$ und so $det(A) = det(A \cdot B) = 0$ nach 7. gelten wuerde, wobei die Elementarmatrizen jeweils offensichtliche Determinanten besitzen
	10. Folgt aus der Definition der Leibnitzformel als Realisierung der Weierstrass-Axiome
o.B.d.A.
## Determinanten von ähnlichen Matrizen
^9a19c3
Seien $A, B$ [[Äquivalenz und Ähnlichkeit von Matrizen|ähnliche Matrizen]], also Matrizen, die dieselbe lineare Abbildung bez. unterschiedlicher Eingangsbasen repraesentieren. Dann gilt: $det (A) = det (B)$.

Beweis:
	Der Beweis folgt direkt aus der Eigenschaft 8. sowie der Definition von [[Äquivalenz und Ähnlichkeit von Matrizen|ähnlichen Matrizen]]: $det(A) = det(S \cdot B \cdot S^{-1}) = det(S) \cdot det(B) \cdot det(S^{-1}) = det(S) \cdot det(S^{-1}) \cdot det(B)$ $= det(S \cdot S^{-1}) \cdot det(B) = det(I_n) \cdot det(B) = det(B)$

