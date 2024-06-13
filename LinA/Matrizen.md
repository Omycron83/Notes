Eine $m \times n$ Matrix über einem [[Körper]] $K$ ist eine Anordnung von $n \cdot m$ Elementen aus $K$ in einem rechteckigen Schema:

$\begin{pmatrix} a_{1,1}& ... & a_{1, n} \\ ... &... & ...\\ a_{1, m} & ...& a_{n, m}\end{pmatrix}$ 

wobei man die Elemente $a_{i, j}$ **Koeffizienten** der Matrix nennt. Die Menge aller $m \times n$ Matrizen über $K$ bezeichnet man mit $M_K (m, n)$ oder $K^{m \times n}$ .

Als besondere Matrix gilt die Einheitsmatrix $I_n \in K^{n \times n}$, für die gilt:
$I_{i, j} = 0 \text{ wenn } i \neq j, 1 \; \text{sonst}$. 

Matrizen können in der (linearen) Algebra vielseitig interpretiert werden:
- [[Matrizen als Ring]]
- [[Matrizen als Vektorraum]]

Auch kann man auf ihnen verschiedene Eigenschaften beschrieben werden:
- [[Transponierte Matrizen]]
- [[Zeilenstufenform einer Matrix]]
- [[Zeilenraum und Zeilenumformungen einer Matrix]]
# Rechenregeln der Matrizenmultiplikation
^2a0827
Seien $B = (b_{ij}), A = (a_{ij})$ Matrizen, dann ist $C = A \cdot B = (c_{ij})$ definiert mit $c_{ij} = \sum_{k = 1}^n a_{ik} \cdot b_{kj}$.

Dabei gilt:
1. $A \cdot (B + C) = A \cdot B  + A \cdot C$    Dist. 1
2. $(A + C) \cdot B = A \cdot B + C \cdot B$    Dist. 2
3. $A \cdot (\lambda \cdot B) = (\lambda \cdot A) \cdot B = \lambda \cdot (A \cdot B)$   Homogen.
4. $A \cdot (B \cdot C) = (A \cdot B) \cdot C$    Assoz.
5. $I_n \cdot A = A \cdot I_n = A$
6. $(A \cdot B)^T = B^T \cdot A^T$ 

Bew.:
	1. ![[Pasted image 20231031222055.png]]
	2. Ebenso
	3. Einfach einsehbar
	4. Nach der [[Matrizen als Lineare Abbildungen#^4c7df6|Assoziativitaet der Komposition]]
	5. Ebenfalls einfach einsehbar
	6. Laesst sich aus der Invarianz der Reihenfolge Zeilen/Spalten multiplizieren <-> Zeilen/Spalten vertauschen erkennen