# Inverse Matrizen:

^28e346
Eine Matrix $A^{-1} \in K^{n \times n}$ gilt als (eindeutiges) Inverses einer anderen Matrix $A \in K^{n \times n}$, wenn $A \cdot A^{-1} = A^{-1} \cdot A = I_n$. Damit sind offensichtlich nur quadratische Matrizen invertierbar.

# Gruppe der invertierbaren Matrizen
Die Menge aller invertierbaren quadratischen Matrizen 
$G = \{M \in K^{n \times n} | M$ ist invertierbar$\}$ bildet eine Gruppe mit der Matrizenmultiplikation $(G, \cdot)$.
Beweis:
	Man prüfe die [[Gruppen|Gruppenaxiome]]:
	- Die Assoziativität der Matrizenmultiplikation [[Matrizen als Ring#^b1f482|sei gezeigt]]
	- $I_n \in G$, da die Einheitsmatrix offensichtlich invertierbar ist
	- Durch die Bedingung der invertierbarkeit hat jede Matrix ein inverses
	Es sei nur noch zu zeigen, dass die Verknüpfung abgeschlossen ist, 