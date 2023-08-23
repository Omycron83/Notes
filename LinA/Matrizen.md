Eine $m \times n$ Matrix über einem [[Körper]] $K$ ist eine Anordnung von $n \cdot m$ Elementen aus $K$ in einem rechteckigen Schema:

$\begin{pmatrix} a_{1,1}& ... & a_{1, n} \\ ... &... & ...\\ a_{1, m} & ...& a_{n, m}\end{pmatrix}$ 

wobei man die Elemente $a_{i, j}$ **Koeffizienten** der Matrix nennt. Die Menge aller $m \times n$ Matrizen über $K$ bezeichnet man mit $M_K (m, n)$ oder $K^{m \times n}$ .
### Zeilenraum:

^7a07fe

Der Zeilenraum $ZR(A)$ einer Matrix $A \in K^{m \times n}$ ist das Erzeugniss der Zeilen $a_i$ von $A$, also $span(a_1, ..., a_n)$, also alle möglichen Linearkombinationen der Zeilenvektoren (wenn [[Matrizen#^2d573a|als Vektorraum interpretiert]]).
### Zeilenumformungen:

^6ef525

Es gibt zwei elementare Zeilenumformungen, die den Zeilenraum erhalten:
#### Typ 1: Zeilenmultiplikation mit $\lambda \neq 0$:
Die $i$'te Zeile wird mit einem Skalar multipliziert. Man schreibt $A \rightarrow A_1$
Beweis Zeilenraumerhaltung:
	$span(a_1, ..., a_m) = \mu_1 a_1 + ... + \mu_i a_i + ... + \mu_m a_m$
	Setzt man nun $\lambda a_i$ ein, so kann man im Fall $\lambda \neq 0$ einfach $\hat{\mu}_i := \frac{\mu_i}{\lambda}$ setzen, sodass
	$\mu_1 a_1 + ... + \hat{\mu}_i (\lambda a_i) + ... + \mu_m a_m = span(a_1, ..., a_m)$ die Linearkombinationen wieder übereinstimmen.
Das bedeuted, dass $ZR(A) = ZR(A_1)$.
#### Typ 2: Addition zweier Zeilen:
Die $j$'te Zeile wird auf die $i$'te Zeile aufaddiert. Man schreibt $A \rightarrow A_2$
Beweis Zeilenraumerhaltung:
$span(a_1, ..., a_m) = \mu_1 a_1 + ... + \mu_j a_j + ... +\mu_i a_i + ... + \mu_m a_m$
	Setzt man nun $a_j + a_i$  ein, so kann man $\hat{\mu}_i_ := 
	So ist $\mu_1 a_1 + .... + \mu_j a_j + ... + \hat{\mu}_i (a_i + a_j) + ... \mu_m a_m = span(a_1, ..., a_m)$ 
	und die Linearkombinationen stimmen überein.
Das bedeuted, dass $ZR(A) = ZR(A_2)$.

#### Typ 3: Addition zweier Zeilen:
Das vielfache der $j$'ten Zeile $\lambda a_j$ wird auf die $i$'te Zeile addiert. 
Beweis Zeilenraumerhaltung:
	Der Beweis folgt daraus, dass $ZR(A) = ZR(A_1)$ und $ZR(A) = ZR(A_2)$ wodurch trivial $ZR(A_3) = ZR(A)$ gilt.

#### Typ 4: Addition zweier Zeilen:
Die $j$'te Zeile wird mit der $i$'ten Zeile vertauscht.
Beweis Zeilenraumerhaltung:
	Der Beweis ist trivial, da die Linearkombination reihenfolgeninvariant ist.

### Zeilenstufenform:

^7d6af4

Eine Matrix ist **in Zeilenstufenform**, wenn:
- Es ein $r \in \{0, 1, ..., n \}$ gibt, sodass  $\forall i \in \{1, ..., m\}, j > r: a_{i, j} = 0$
- Es $j_1, ..., j_r$ gibt mit $0 < j_1 ... < j_r$ und $j_i := min\{j | a_{i, j} \neq 0 \}$ 

Dies bedeuted, dass es ein solches Spaltenelement in jeder Zeile gibt, dass alle Elemente links von diesem Null sind, es selbst nicht null ist und es selbst links vom Spaltenelement der oberen Zeile steht. Diese Spaltenelemente bilden damit eine Stufenlinie.
Die Elemente rechts der Spaltenelemente können beliebige Werte annehmen.

#### Satz: Jede Matrix kann in Zeilenstufenform umgeformt werden:
Sei $A$ eine $m \times n$ Matrix mit Zeilen $a_1, ..., a_m$. Diese lässt sich mithilfe der obigen [[Matrizen#^6ef525|Zeilenumformungen]]  eine Matrix $A'$ in [[Matrizen#^7d6af4|Zeilenstufenform]] umformen. Die Zeilen von $A'$, die keine Nullzeilen sind, sind eine Basis des [[Matrizen#^7a07fe|Zeilenraumes]] $ZR(A)$.
Beweis:
	Der Beweis lässt sich erbringen, indem man einen Algorithmus formuliert, welcher systematisch eine Zeilenstufenform erzeugt. Man tue dabei folgendes solange, wie keine [[Matrizen#^7d6af4|Zeilenstufenform]] besteht. Handelt es sich um die Nullmatrix, so ist nichts zu zeigen:
	0. Sonst gibt es eine Zeile $j_k$, die einen Eintrag ungleich 0 besitzt. 
	1. Man tausche die Zeilen so, dass $a_{k, j_k} \neq 0$
	2. Man nutze Umformungen vom Typ 3, so, um alle $a_{i, j_1} = 0, i \neq 1$ zu setzen, indem man auf sie $-\frac{a_{1, j_1}}{a_{i, j_1}} a_1$ addiert.
	Tut man dies bis zum Ende, so besitzt man dadurch bis auf die Nullzeilen auf Grunde der Matrix eine linear unabhängige Familie an Zeilenvektoren $a_i$, da jeweils nur ein Zeilenvektor einen Eintrag 
## Matrizen als Vektorraum:

^2d573a

Betrachte man $K^{m \times n}$ zusammen mit der elementweisen Addition und Skalarmultiplikation mit $K$. Dann ist $K^{m \times n}$ ein $K$-[[Vektorraum]]. In diesem Fall kann man Matrizen also als 'umgeschriebene Vektoren' betrachten.

Beweis:
	Da der $K^n$ ein [[Vektorraum#^6e22e7|Vektorraum ist]], und die Tupelanordnung irrelevant ist, ist auch der $K^{m \times n}$ ein Vektorraum.

Eine $1 \times n$ Matrix wäre dann also eine 'Zeilenvektor' (den man normal als $n$-Tupel schreiben kann) und eine $m \times 1$ Matrix ein 'Spaltenvektor'. 
## Matrizen als Ring:
## Matrizenmultiplikation

## Inverse Matrizen

 