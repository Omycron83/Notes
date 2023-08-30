Eine $m \times n$ Matrix über einem [[Körper]] $K$ ist eine Anordnung von $n \cdot m$ Elementen aus $K$ in einem rechteckigen Schema:

$\begin{pmatrix} a_{1,1}& ... & a_{1, n} \\ ... &... & ...\\ a_{1, m} & ...& a_{n, m}\end{pmatrix}$ 

wobei man die Elemente $a_{i, j}$ **Koeffizienten** der Matrix nennt. Die Menge aller $m \times n$ Matrizen über $K$ bezeichnet man mit $M_K (m, n)$ oder $K^{m \times n}$ .

Als besondere Matrix gilt die Einheitsmatrix $I_n \in K^{n \times n}$, für die gilt:
$I_{i, j} = 0 \text{ wenn } i \neq j, 1 \; \text{sonst}$. 
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

#### Lemma: Zeilenstufenform ohne Nullzeilen => linear unabhängig:
Ist $A$ in Zeilenstufenform mit $a_1, ..., a_r$ Zeilen $\neq o$. Dann sind diese linear unabhängig.
Beweis durch direkten Test:
	Sei $o = \lambda_1 a_1 + ... + \lambda_r a_r$.
	Man erinnere sich, dass jede Zeile effektiv ein $n$-Tupel ist.
	Somit muss, da $o = (0, ..., 0)$ der Nullvektor $\in K^n$ ist:
	$0 = \lambda_1 a_{1, j_1} + ... + \lambda_r a_{r, j_1}$  ist dann die Gleichung für den Eintrag in Spalte $j_l$.
	Nun kann man von $j_1$ als Ausgangsfall aus starten. Da wir wissen, das alle Spalteneinträge unter $j_1 = 0$ sein müssen, gilt:
	$0 = \lambda_{1} a_{1, j_1} + ... + \lambda_r 0 =  \lambda_{1} a_{1, j_1} \implies  \lambda_{1} = 0$ . Dann steht $\lambda_1 = 0$ fest.  
	Nehme man nun an, dass bereits $\lambda_{1} = ... = \lambda_{l - 1} = 0$ gezeigt wurden.
	Dann ist $0 = 0 a_{1, j_1} + ... + \lambda_{l} a_{l, j_l} + ... + \lambda_r 0 = \lambda_{j_l} a_{l, j_l}  \implies \lambda_{l} = 0$
	Per vollständiger Induktion ist dann klar, dass $\lambda_{1} = ... = \lambda_{r} = 0$ sein muss, also die Zeilen linear unabhängig sind.
	Man kann sich das auch vereinfacht darstellen: damit die erste Spalte null ist, muss der Koeffizient der 1. Zeile null sein, diese 'scheidet also aus'. Damit kann der erste Eintrag der ersten Zeile garnicht mehr aus den anderen gebildet werden, da alle anderen null sind, und so ist auch ihr Koeffizient null etc. etc.

#### Satz: Jede Matrix kann in Zeilenstufenform umgeformt werden:
Sei $A$ eine $m \times n$ Matrix mit Zeilen $a_1, ..., a_m$. Diese lässt sich mithilfe der obigen [[Matrizen#^6ef525|Zeilenumformungen]]  eine Matrix $A'$ in [[Matrizen#^7d6af4|Zeilenstufenform]] umformen. Die Zeilen von $A'$, die keine Nullzeilen sind, sind eine Basis des [[Matrizen#^7a07fe|Zeilenraumes]] $ZR(A)$.
Beweis:
	Der Beweis lässt sich erbringen, indem man einen Algorithmus formuliert, welcher systematisch eine Zeilenstufenform erzeugt. Man tue dabei folgendes solange, wie keine [[Matrizen#^7d6af4|Zeilenstufenform]] besteht. Handelt es sich um die Nullmatrix, so ist nichts zu zeigen:
	0. Sonst gibt es eine Zeile $j_1$, die einen Eintrag ungleich 0 besitzt. 
	1. Man tausche die Zeilen so, dass $a_{1, j_1} \neq 0$
	2. Man nutze Umformungen vom Typ 3, so, um alle $a_{i, j_1} = 0, i \neq 1$ zu setzen, indem man auf sie $-\frac{a_{1, j_1}}{a_{i, j_1}} a_1$ addiert.
	Tut man dies bis zum Ende, so besitzt man dadurch bis auf die Nullzeilen auf Grunde der Matrix eine nach dem obigen Lemma linear unabhängige Familie an Zeilenvektoren $a_i$. Da diese durch die Operationen immernoch den selben Zeilenraum besitzen handelt es sich dabei um eine Basis.

### Transpositionierte Matrizen:
Sei $A$ eine Matrix $\in K^{m \times n}$. Dann nennt man eine Matrix $A^T \in K^{n \times m}$ ihre Transponierte, wenn der Zeilenvektor $a_{i, \cdot}$ gleich dem Spaltenvektor $a_{\cdot, i}$ ist. Dann ist $A^T$ also
$A^T = \begin{pmatrix} a_{1, 1} & ... & a_{1, m} \\ ... & ... & ... \\ a_{1, n} & ... & a_{m, n} \end{pmatrix}$ 
Man 'vertauscht' also Zeilen und Spalten bzw. 'spiegelt' diese an der Hauptdiagonalen.
Man schreibt dabei auch $A^T = (a_{j, i})_{i, j}$.
#### Rechenregeln von Transponierten:
Es gilt dabei:
1. $(\lambda A)^T = \lambda A^T$
2. $(A + B)^T = A^T + B^T$
3. $(A^T)^T = A$
Beweis:
	1. Erkennt man leicht.
	2. Sei ebenfalls klar, wenn man sich die individuellen Spalten / Zeilen anschaut.
	3. Sei klar, das Vertauschen ist selbstinvers.
### Matrizenmultiplikation:
Sei $A \in K^{m \times n}$ und $B \in K^{n \times r}$. Dann ist die Matrizenmultiplikation $K^{m \times n} \times K^{n \times r} \rightarrow K^{m \times r}$ definiert als $A \cdot B \rightarrow C$ mit $c_{i, j} = \sum_{l = 1}^n a_{i, l} \cdot b_{l, j}$.  

### Matrizenmultiplikation ist Assoziativ:

^b1f482

Die Matrizenmultiplikation ist Assoziativ, d.h. $A \cdot (B \cdot C) = (A \cdot B) \cdot C = D$.
Beweis:
	Mache man sich zunächst die Dimensionalität klar: wenn $A \in K^{m \times n}$, $B \in K^{n \times r}$ und $C \in K^{r \times g}$ dann ist $B \cdot C \in K^{n \times g}$ und $A \cdot B \in K^{m \times r}$, wodurch die Dimensionen stimmen.
	Zeige man nun, dass $d_{i, j} = \sum_{l = 1}^n a_{i, l} \cdot (\sum_{g = 1}^r b_{l, g} \cdot c_{g, j} )_{l, j} = \sum_{g = 1}^r (\sum_{l = 1}^n a_{i, l} \cdot b_{l, g})_{i,g} \cdot c_{g,j}$    

### Inverse Matrizen:

^28e346

Eine Matrix $A^{-1} \in K^{n \times n}$ gilt als eindeutiges Inverses einer anderen Matrix $A \in K^{n \times n}$, wenn $A \cdot A^{-1} = A^{-1} \cdot A = I_n$ .

## Matrizen als Vektorraum:

^2d573a

Betrachte man $K^{m \times n}$ zusammen mit der elementweisen Addition und Skalarmultiplikation mit $K$. Dann ist $K^{m \times n}$ ein $K$-[[Vektorraum]]. In diesem Fall kann man Matrizen also als 'umgeschriebene Vektoren' betrachten.

Beweis:
	Da der $K^n$ ein [[Vektorraum#^6e22e7|Vektorraum ist]], und die Tupelanordnung irrelevant ist, ist auch der $K^{m \times n}$ ein Vektorraum.

Eine $1 \times n$ Matrix wäre dann also eine 'Zeilenvektor' (den man normal als $n$-Tupel schreiben kann) und eine $m \times 1$ Matrix ein 'Spaltenvektor'. 
## Matrizen als Ring:
Betrachte man die Menge der quadratischen Matrizen $K^{n \times n}$ zusammen mit der Matrizenmultiplikation und der Addition bildet einen [[Ringe|Ring]]: $(K^{n \times n}, +, \cdot)$.
Beweis:
	Prüfe man die Ringaxiome:
	1. Die abelsche Gruppe ist Körperinduziert
	2. Die Assoziativität ist [[Matrizen#^b1f482|gezeigt]]
	3. Das Distributivgesetz ist Körperinduziert (man schaue sich diese lediglich Elementweise an)

## Matrizen stellen lineare Abbildungen dar:
#### Herleitung:
Es fällt auf, dass man Matrizen leicht zur Darstellung von Linearkombinationen nutzen lassen kann: $\begin{pmatrix} b_1, & ... & ,b_n \end{pmatrix} \cdot \begin{pmatrix} \lambda_1 \\ ...\\ \lambda_n  \end{pmatrix} = \lambda_1 b_1 + ... + \lambda_n b_n = v$ 
wobei hier die Linearkombination eines Vektors $v$ durch die Basisvektoren dargestellt wird.

Seien $V, W$ nun zwei Vektorräume über demselben Körper $K$, wobei $b_1, ..., b_n$ die Basisvektoren von $V$ und $w_1, ..., w_n$ die Basisvektoren von $W$ sind.


Betrachte man zwei Vektorräume $V, W$ mit Basen $v_1, …, v_r$ und $w_1, …, w_n$. Dann kann jeder Vektor 