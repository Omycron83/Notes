Äquivalente und ähnliche Matrizen bilden jeweils [[Relationen#^10bc55|Äquivalenzklassen]] bezüglich der [[Matrizen als Lineare Abbildungen|Darstellungen von linearen Abbildungen]].
# Äquivalenz von Matrizen:
Seien $A, B \in K^{m \times n}$ zwei Matrizen über $K$. Dann nennt man diese **äquivalent**, wenn es eine lineare Abbildung $f: K^n \rightarrow K^m$ gibt, sodass $A = _{B_1} M(f)_{C_1}$,  $B = _{B_2} M(f)_{C_2}$, bzw. $A = S \cdot B \cdot T ^{-1}$. 

$A$ und $B$ sind also Darstellungen von $f$ bezüglich unterschiedlicher Basen der beiden [[Vektorraum|Vektorräume]].

# Ähnlichkeit von Matrizen:
Seien $A, B \in K^{n \times n}$ zwei [[Matrizen]] über einem [[Körper]] $K$. Dann nennt man diese **ähnlich**, wenn es eine [[Gruppe der invertierbaren Matrizen#^4f6aa3|invertierbare Matrix]] $S \in K^{n \times n}$ gibt, sodass
$B = S^{-1} A S$.

Dies kann dabei so interpretiert werden, dass $S$ einen [[Darstellungslemma von Körpervektorräumen|Automorphismus]] vom $K^n$ darstellt, sodass $A$ und $B$ sonst prinzipiell dieselbe Lineare Abbildung bez. verschiedener Basen im Urbildraum charakterisieren. Dabei lässt sich $S$ als $T_{a \rightarrow b}$ und $S^{-1}$ als $T_{b \rightarrow a}$ interpretieren.

### Ähnliche Matrizen haben dieselbe Determinante

### Ähnliche Matrizen haben dieselben Eigenwerte
