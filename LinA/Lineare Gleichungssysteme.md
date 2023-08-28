Ein lineares Gleichungssystem ist ein Gleichungssystem mit $m$ Gleichungen und $n$ Variablen der Form $a_{l, 1} x_{1} + ... + a_{l, n} x_{n} = c_l$, wobei es gilt eine Lösungsmenge der $x_i$ zu bestimmen.  

Geometrisch lässt sich der Lösungsraum einer jeden solchen linearen Gleichungen als Punktemenge von Punkten von $(n - 1)$-Tupeln darstellen. 
Dies ist Fall, da sich die Punkte als Elemente des Urbildes der [[Abbildungen|Abbildung]] bezüglich $a_{l, 1} = \frac{... + a_{l, n} x_{n} - c_l}{x_{1}}$ auffassen lassen.
# Darstellung mit Matrizen:
Ein lineares Gleichungssystem kann sich einfach mithilfe von [[Matrizen]] darstellen. Sei dabei $(x_1, ..., x_n)^T$ der Variablen-Spaltenvektor und $\begin{pmatrix} a_{1, 1} & ... & a_{1, n} \\ ...&...&... \\ a_{m, 1} & ... & a_{n, m} \end{pmatrix}$ eine Matrix der Koeffizienten.
Dann lässt sich der Spaltenvektor der Konstanten $(c_1, ..., c_m)^T$ darstellen lassen als:
$\begin{pmatrix} a_{1, 1} & ... & a_{1, n} \\ ...&...&... \\ a_{m, 1} & ... & a_{n, m} \end{pmatrix} \cdot (x_1, ..., x_n)^T = (c_1, …, c_n)^T$.
Den Variablen-Vektor kann man dann bestimmen, indem man linksseitig mit der [[Matrizen#^28e346|Inversen]] der Koeffizientenmatrix multipliziert:
$

