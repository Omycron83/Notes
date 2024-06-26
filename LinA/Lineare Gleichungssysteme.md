Ein lineares Gleichungssystem ist ein Gleichungssystem mit $m$ Gleichungen und $n$ Variablen der Form $x_{1} a_{l, 1}  + ... + x_{n} a_{l, n}  = b_l$, wobei es jeweils gilt eine Lösungsmenge der $x_i$ zu bestimmen.  
Die Lösungsmenge des Gleichungssystems ist dann der Durchschnitt der einzelnen Lösungsmenge.

# Geometrische Darstellung:
Geometrisch lässt sich der Lösungsraum einer jeden solchen linearen Gleichungen als Punktemenge von Punkten von $(n - 1)$-Tupeln darstellen. 
Dies ist Fall, da sich die Punkte als Elemente des Urbildes der [[Abbildungen|Abbildung]] bezüglich $a_{l, 1} = \frac{... + a_{l, n} x_{n} - b_l}{x_{1}}$ auffassen lassen. 
Für eine eindeutige Lösung müsste man genau einen Schnittpunkt der Geraden haben, für unendlich Lösungen eine Linie auf der alle anderen Liegen und für keine müssen verschiedene Geraden verschiedene Schnittpunkte besitzen.

# Darstellung mit Matrizen:
## Darstellung durch Matrixmultiplikation:
Ein lineares Gleichungssystem kann sich einfach mithilfe von [[Matrizen]] darstellen. Sei dabei $x = (x_1, ..., x_n)^T$ der Variablen-Spaltenvektor und $A = \begin{pmatrix} a_{1, 1} & ... & a_{1, n} \\ ...&...&... \\ a_{m, 1} & ... & a_{n, m} \end{pmatrix}$ eine Matrix der Koeffizienten.
Dann lässt sich der Spaltenvektor der Konstanten $y = (b_1, ..., b_m)^T$ darstellen lassen als:
$\begin{pmatrix} a_{1, 1} & ... & a_{1, n} \\ ...&...&... \\ a_{m, 1} & ... & a_{n, m} \end{pmatrix} \cdot (x_1, ..., x_n)^T = (b_1, …, b_n)^T$, d.h. $A \cdot x = y$.
Den Variablen-Vektor kann man dann bestimmen (wenn $m = n$), indem man linksseitig mit der [[Matrizen#^28e346|Inversen]] der Koeffizientenmatrix multipliziert:
$A^{-1} \cdot A \cdot x = x = A^{-1} \cdot y$  

Es gibt also genau dann eine Lösung, wenn die Koeffizientenmatrix invertierbar ist. 

## Darstellung mit Rechtsspalte:
Anstatt der expliziten Darstellung durch eine Matrizenmultiplikation kann man äquivalent das Gleichungssystem darstellen, indem man über jede Spalte der Koeffizienten eine der Variablen $x_i$ schreibt und den Vektor der Lösungen $b_i$ als zusätzliche Spalte (oft mit einem Strich separiert) rechtsseitig anfügt.

Elementare Zeilenumformungen werden dann auf allen Spalten ausgeführt, was der Multiplikation mit der inversen Matrix auf beiden Seiten entspricht.


Die Inversion lässt sich in beiden Fällen über [[Zeilenraum und Zeilenumformungen einer Matrix#^6ef525|elementare Zeilenumformungen]] 
mithilfe des Gauss-Algorithmus durchführen. 

- Gilt dann [[Rang einer Matrix|rg(A)]] $= n$, dann gibt es eine eindeutige Lösung.
- Gilt $rg(A) < n$, dann gibt es unendlich Lösungen mit $n - rg(A)$ freien Variablen.
- Gilt aber $rg(A) \neq rg(A, b)$, dann gibt es keine Lösung, da es eine Zeile $a_{i, 1} 0 + ... + a_{i, n} 0 = b , b \neq 0$ gibt, was nicht möglich ist.


