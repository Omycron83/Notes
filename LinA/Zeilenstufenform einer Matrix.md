
^7d6af4

Eine [[Matrix]] ist **in Zeilenstufenform**, wenn:
- Es ein $r \in \{0, 1, ..., n \}$ gibt, sodass  $\forall i \in \{1, ..., m\}, j > r: a_{i, j} = 0$
- Es $j_1, ..., j_r$ gibt mit $0 < j_1 ... < j_r$ und $j_i := min\{j | a_{i, j} \neq 0 \}$ 

Dies bedeuted, dass es ein solches Spaltenelement in jeder Zeile gibt, dass alle Elemente links von diesem Null sind, es selbst nicht null ist und es selbst links vom Spaltenelement der oberen Zeile steht. Diese Spaltenelemente bilden damit eine Stufenlinie.
Die Elemente rechts der Spaltenelemente können beliebige Werte annehmen.

# Lemma: Zeilenstufenform ohne Nullzeilen => linear unabhängig:
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

# Satz: Jede Matrix kann in Zeilenstufenform umgeformt werden:
Sei $A$ eine $m \times n$ Matrix mit Zeilen $a_1, ..., a_m$. Diese lässt sich mithilfe der obigen [[Matrizen#^6ef525|Zeilenumformungen]]  eine Matrix $A'$ in [[Matrizen#^7d6af4|Zeilenstufenform]] umformen. Die Zeilen von $A'$, die keine Nullzeilen sind, sind eine Basis des [[Matrizen#^7a07fe|Zeilenraumes]] $ZR(A)$.
Beweis:
	Der Beweis lässt sich erbringen, indem man einen Algorithmus formuliert, welcher systematisch eine Zeilenstufenform erzeugt. Man tue dabei folgendes solange, wie keine [[Matrizen#^7d6af4|Zeilenstufenform]] besteht. Handelt es sich um die Nullmatrix, so ist nichts zu zeigen:
	0. Sonst gibt es eine Zeile $j_1$, die einen Eintrag ungleich 0 besitzt. 
	1. Man tausche die Zeilen so, dass $a_{1, j_1} \neq 0$
	2. Man nutze Umformungen vom Typ 3, so, um alle $a_{i, j_1} = 0, i \neq 1$ zu setzen, indem man auf sie $-\frac{a_{1, j_1}}{a_{i, j_1}} a_1$ addiert.
	Tut man dies bis zum Ende, so besitzt man dadurch bis auf die Nullzeilen auf Grunde der Matrix eine nach dem obigen Lemma linear unabhängige Familie an Zeilenvektoren $a_i$. Da diese durch die Operationen immernoch den selben Zeilenraum besitzen handelt es sich dabei um eine Basis.
