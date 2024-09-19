Eine Permutation ist eine bijektive Abbildung $\pi: X \rightarrow X$.
Man nennt $S_n$ dabei die Menge der Permutationen von $\{1, ..., n\}$, wobei $|S_n| = n! \approx ((\frac{n}{e})^n \sqrt{2 \pi n}$.

## Darstellungsmoeglichkeiten
Man kann diese darstellen als:
### 2-Zeilen-Notation:
$P = \begin{pmatrix}  1 & ... & n \\ a & ... & c\end{pmatrix} \in S_n$
wobei $P(1) = a, ..., P(n) = c$. 
### 1-Zeilen-Notation:
$P = (a, ..., c)$ 
wobei die erste Zeile aus redundanz weggelassen wird.
### Zyklenschreibweise:
In der Zyklenschreibweise wird eine Permutation in Zyklen zerlegt, wobei fuer jeder Zyklus der Laenge $n$ gilt: $\pi^n(a) = a$ und die Zyklen disjunkt sind. Sie ist moeglich, wenn $X$ eine endliche Menge ist sowie $\pi$ injektiv und wohldefiniert ist.

Beweis:
	Ist $\pi$ injektiv, so wird jedes Element auf ein anderes abgebildet, welches ebenfalls wieder durch die wohldefiniertheit auf ein weiteres abgebildet wird. Daraus folgt die Bijektivitaet und aus dieser ebenfalls die moegliche Zyklenzerlegung.

Die Zyklenschreibweise ist dabei eindeutig bis auf Reihenfolge der Zyklen sowie deren Anfangselemente. 

# Zyklenstruktur
## Typ einer Permutation:
Der Typ einer Permutation $\pi \in S_n$ ist der Ausdruck $[1^{\alpha_1} ... n^{\alpha_n}]$, wobei $\alpha_i$ die Anzahl der $i$-Zyklen in der Zyklenanzahl von $\pi$. Dabei gilt offensichtlich $\sum_{i = 1}^n i \alpha_i = n$. 

## Transpositionen von Permutationen:
Eine Transposition ist eine Permutation vom Typ $[1^{n - 2}2^1]$. Sie vertauscht zwei Elemente, wobei man lediglich $(ij)$ fuer die beiden Elemente  $i, j$ schreibt.

Dabei gilt: Jede Permutation kann als Produkt von Transpositionen geschrieben werden. 

Beweis:
	Jede Permutation kann als Produkt von Zyklen geschrieben werden, welche wiederum als Produkte von Transpositionen mit $z = (x_1 x_2 ... x_n) = (x_1 x_2)...(x_n x_1)$ geschrieben werden koennen.

## Gerade und ungerade Transpositionen
Sei $\tau \in S_n$ eine Transposition und $\pi \in S_n$ eine Transposition. Dann gilt:
$z(\tau \cdot \pi) \in \{z(\pi) - 1, z(\pi) + 1\}$.

Beweis:
	 Sei $\tau = (a,b)$. Dann kommen $a$ und $b$ entweder im selben oder im unterschiedlichen Zyklus vor. Kommen sie im selben Zyklus vor, so zerlegt dies den Zyklus in zwei Zyklen, und die Anzahl der Zyklen steigt um 1. Kommen sie in unterschiedlichen Zyklen vor, so faellt die Anzahl um 1.

Die Anzahl der Transpositionen, in derer sich $\pi$ faktorisieren laesst, ist dabei entweder gerade oder ungerade.

### Das Signum

^0c71fb

Sei $\pi \in S_n$ und sei $\pi = \tau_1 \cdot ... \tau_r = \tau_1' \cdot \tau_r'$. Dann sind $r$ und $r'$ entweder beide gerade oder ungerade. ^f3b9ab

Beweis:
	Folgt aus dem Satz zu geraden bzw. ungeraden Transpositionen.

Dies motiviert die wohldefinierte Funktion $sgn(\pi) = (-1)^r$ fuer $\pi = \tau_1 \cdot ... \cdot \tau_r$.
Wobei diese ausserdem einen Gruppenhomomorphismus fuer die symmetrische Gruppe ausmacht.v

## Inversionen:
Eine Inversion von $\pi$ ist ein paar $i, j$ mit $i , j$ und $\pi(i) > \pi(j)$, und stellen konzeptionell Kreuzungen in der 2-Zeilen-Darstellung dar.
Dabei gilt: $sgn(\pi) = (-1)^{Inv(\pi)}$, wobei $Inv(\pi)$ die Anzahl der Inversionen ist.