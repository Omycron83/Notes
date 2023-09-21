# Transpositionierte Matrizen:
Sei $A$ eine [[Matrizen|Matrix]] $\in K^{m \times n}$. Dann nennt man eine Matrix $A^T \in K^{n \times m}$ ihre Transponierte, wenn der Zeilenvektor $a_{i, \cdot}$ gleich dem Spaltenvektor $a_{\cdot, i}$ ist. Dann ist $A^T$ also
$A^T = \begin{pmatrix} a_{1, 1} & ... & a_{1, m} \\ ... & ... & ... \\ a_{1, n} & ... & a_{m, n} \end{pmatrix}$ 
Man 'vertauscht' also Zeilen und Spalten bzw. 'spiegelt' diese an der Hauptdiagonalen.
Man schreibt dabei auch $A^T = (a_{j, i})_{i, j}$.
## Rechenregeln von Transponierten:
Es gilt dabei:
1. $(\lambda A)^T = \lambda A^T$
2. $(A + B)^T = A^T + B^T$
3. $(A^T)^T = A$
Beweis:
	1. Erkennt man leicht.
	2. Sei ebenfalls klar, wenn man sich die individuellen Spalten / Zeilen anschaut.
	3. Sei klar, das Vertauschen ist selbstinvers.


