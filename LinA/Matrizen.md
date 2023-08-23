Eine $m \times n$ Matrix über einem [[Körper]] $K$ ist eine Anordnung von $n \cdot m$ Elementen aus $K$ in einem rechteckigen Schema:

$\begin{pmatrix} a_{1,1}& ... & a_{1, n} \\ ... &... & ...\\ a_{1, m} & ...& a_{n, m}\end{pmatrix}$ 

wobei man die Elemente $a_{i, j}$ **Koeffizienten** der Matrix nennt. Die Menge aller $m \times n$ Matrizen über $K$ bezeichnet man mit $M_K (m, n)$ oder $K^{m \times n}$ .

## Matrizen als Vektorraum:
Betrachte man $K^{m \times n}$ zusammen mit der elementweisen Addition und Skalarmultiplikation mit $K$. Dann ist $K^{m \times n}$ ein $K$-[[Vektorraum]]. In diesem Fall kann man Matrizen also als 'umgeschriebene Vektoren' betrachten.

Beweis:
	Da der $K^n$ ein [[Vektorraum#^6e22e7|Vektorraum ist]], und die Tupelanordnung irrelevant ist, ist auch der $K^{m \times n}$ ein Vektorraum.

Eine $1 \times n$ Matrix wäre dann also eine 'Zeilenvektor' (den man normal als $n$-Tupel schreiben kann) und eine $m \times 1$ Matrix ein 'Spaltenvektor'. 
### Zeilenstufenform:
Eine Matrix ist **in Zeilenstufenform**, wenn:
- Es ein $r \in \{0, 1, ..., n \}$ gibt, sodass  $\forall i \in \{1, ..., m\}, j > r: a_{i, j} = 0$
- Es $j_1, ..., j_r$ gibt mit $0 < j_1 ... < j_r$ und $j_i := min\{j | a_{i, j} \neq 0 \}$ 

Dies bedeuted, dass es ein solches Spaltenelement in jeder Zeile gibt, dass alle Elemente links von diesem Null sind, es selbst nicht null ist und es selbst links vom Spaltenelement der oberen Zeile steht. Diese Spaltenelemente bilden damit eine Stufenlinie.
Die Elemente rechts der Spaltenelemente können beliebige Werte annehmen.

### Zeilenumformungen:

## Matrizen als Ring:
## Matrizenmultiplikation

## Inverse Matrizen

 