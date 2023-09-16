Hier sei gezeigt, dass [[Matrizen]] mit der definierten Matrizenmultiplikation einen [[Ringe|Ring]] ergeben.
# Matrizenmultiplikation:

^bcdd4e

Sei $A \in K^{m \times n}$ und $B \in K^{n \times r}$. Dann ist die Matrizenmultiplikation $K^{m \times n} \times K^{n \times r} \rightarrow K^{m \times r}$ definiert als $A \cdot B \rightarrow C$ mit $c_{i, j} = \sum_{l = 1}^n a_{i, l} \cdot b_{l, j}$.  

# Matrizenmultiplikation ist assoziativ:

^b1f482

Die Matrizenmultiplikation ist Assoziativ, d.h. $A \cdot (B \cdot C) = (A \cdot B) \cdot C = D$.
Beweis:
	Mache man sich zunächst die Dimensionalität klar: wenn $A \in K^{m \times n}$, $B \in K^{n \times r}$ und $C \in K^{r \times g}$ dann ist $B \cdot C \in K^{n \times g}$ und $A \cdot B \in K^{m \times r}$, wodurch die Dimensionen stimmen.
	Zeige man nun, dass $d_{i, j} = \sum_{l = 1}^n a_{i, l} \cdot (\sum_{g = 1}^r b_{l, g} \cdot c_{g, j} )_{l, j} = \sum_{g = 1}^r (\sum_{l = 1}^n a_{i, l} \cdot b_{l, g})_{i,g} \cdot c_{g,j}$    

# Inverse Matrizen:

^28e346

Eine Matrix $A^{-1} \in K^{n \times n}$ gilt als eindeutiges Inverses einer anderen Matrix $A \in K^{n \times n}$, wenn $A \cdot A^{-1} = A^{-1} \cdot A = I_n$ .

# Matrizen als Ring:
Betrachte man die Menge der quadratischen Matrizen $K^{n \times n}$ zusammen mit der Matrizenmultiplikation und der Addition bildet einen [[Ringe|Ring]]: $(K^{n \times n}, +, \cdot)$.
Beweis:
	Prüfe man die Ringaxiome:
	1. Die abelsche Gruppe ist Körperinduziert
	2. Die Assoziativität ist [[Matrizen#^b1f482|gezeigt]]
	3. Das Distributivgesetz ist Körperinduziert (man schaue sich diese lediglich Elementweise an)
