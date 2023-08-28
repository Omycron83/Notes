Ein lineares Gleichungssystem ist ein Gleichungssystem mit $m$ Gleichungen und $n$ Variablen der Form $a_{l, 1} x_{1} + ... + a_{l, n} x_{n} = b_l$, wobei es jeweils gilt eine Lösungsmenge der $x_i$ zu bestimmen.  
Die Lösungsmenge des Gleichungssystems ist dann der Durchschnitt der einzelnen Lösungsmenge.

Geometrisch lässt sich der Lösungsraum einer jeden solchen linearen Gleichungen als Punktemenge von Punkten von $(n - 1)$-Tupeln darstellen. 
Dies ist Fall, da sich die Punkte als Elemente des Urbildes der [[Abbildungen|Abbildung]] bezüglich $a_{l, 1} = \frac{... + a_{l, n} x_{n} - b_l}{x_{1}}$ auffassen lassen.

# Darstellung mit Matrizen:
Ein lineares Gleichungssystem kann sich einfach mithilfe von [[Matrizen]] darstellen. Sei dabei $x = (x_1, ..., x_n)^T$ der Variablen-Spaltenvektor und $A = \begin{pmatrix} a_{1, 1} & ... & a_{1, n} \\ ...&...&... \\ a_{m, 1} & ... & a_{n, m} \end{pmatrix}$ eine Matrix der Koeffizienten.
Dann lässt sich der Spaltenvektor der Konstanten $y = (b_1, ..., b_m)^T$ darstellen lassen als:
$\begin{pmatrix} a_{1, 1} & ... & a_{1, n} \\ ...&...&... \\ a_{m, 1} & ... & a_{n, m} \end{pmatrix} \cdot (x_1, ..., x_n)^T = (b_1, …, b_n)^T$, d.h. $A \cdot x = y$.
Den Variablen-Vektor kann man dann bestimmen, indem man linksseitig mit der [[Matrizen#^28e346|Inversen]] der Koeffizientenmatrix multipliziert:
$A^{-1} \cdot A \cdot x = x = A^{-1} \cdot y$  

Es gibt also genau dann eine Lösung, wenn die Koeffizientenmatrix invertierbar ist.



