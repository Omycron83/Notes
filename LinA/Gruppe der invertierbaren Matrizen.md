# Inverse Matrizen:
^28e346
Eine Matrix $A^{-1} \in K^{n \times n}$ gilt als (eindeutiges) Inverses einer anderen Matrix $A \in K^{n \times n}$, wenn $A \cdot A^{-1} = A^{-1} \cdot A = I_n$. Damit sind offensichtlich nur quadratische Matrizen invertierbar. ^4f6aa3

# Gruppe der invertierbaren Matrizen
Die Menge aller invertierbaren quadratischen Matrizen 
$G = \{M \in K^{n \times n} | M$ ist invertierbar$\}$ bildet eine Gruppe mit der Matrizenmultiplikation $(G, \cdot)$, fuer die man auch $GL(n, K)$ schreibt.
Beweis:
	Man prüfe die [[Gruppen|Gruppenaxiome]]:
	- Die Assoziativität der Matrizenmultiplikation [[Matrizen als Ring#^b1f482|sei gezeigt]]
	- $I_n \in G$, da die Einheitsmatrix offensichtlich invertierbar ist
	- Durch die Bedingung der invertierbarkeit hat jede Matrix ein inverses
	Es sei nur noch zu zeigen, dass die Verknüpfung abgeschlossen ist, also dass $A \in GL \cdot B \in GL = AB \in GL$ herrscht. Dabei laesst sich linksseitig mit $A^{-1}$ und dann mit $B^{-1}$ multiplizieren, sodass $I = A^{-1} \cdot B^{-1} \cdot A \cdot B$ folgt.

# Invertierbarkeitskriterium:
Fuer $A \in K^{n \times n}$ ist aequivalent:
- $A \in GL(n, K)$
- $A^T \in GL(n, K)$
- $rg(A) = n$

Bew.:
	$i) \implies ii)$: $I = I^T = (A \cdot A^{-1})^T = (A^-1)^T \cdot A^T \implies (A^{-1})^T = (A^T)^{-1}$ nach [[Matrizen#^2a0827|Rechenregeln]]
	$ii) \implies i)$: Dasselbe Argument
	$i) \implies iii)$: Ist $A$ invertierbar, so folgt aus dem [[Matrizen als Lineare Abbildungen#^2428c8|Lemma]] $n = rg(I) = rg(A^{-1} \cdot A) \le min\{rg(A^{-1}, rg(A))\}$ durch $rg(A) \ge n$ dann $rg(A) = n$
	$iii) \implies i)$ ist $rg(A) =n$, ist $dim(im(A)) = n$, also ist $A$ surjektiv. Aus der Dimensionsformel folgt der Isomorphismus, also ist $A$ invertierbar.