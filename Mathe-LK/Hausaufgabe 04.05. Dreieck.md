# Aufgabe:
Seien $A = (7, -3, 5)$ und $B = (4, 1, 5)$. 

a) Bestimmen sie den Abstand von $A$ und $B$.

b) Bestimmen sie einen Punkt $C$ so, dass das Dreieck $ABC$ gleichschenklig mit Basis $AB$ ist, orthogonal zur x-y-Achse steht und einen Flächeninhalt von $10$ FE besitzt.

# Lösung:
a) Der Abstand entspricht der Norm des Vektors zwischen den beiden Punkten:
$|| A - B|| = ||(3, -4, 0)|| = \sqrt{3^2 + 4^2} = 5$.

b)
Das Dreieck muss dann drei Gleichungen erfüllen:

1) $|| A - C || = || B - C ||$ -> Schenkel gleich lang
2) $MC = (0, 0, z)$  -> Orthogonal = Senkrecht auf, Produkt mit (0, 1, 1)
3) $||MC|| \cdot ||\frac{1}{2} AB|| = 12$ -> Triviale Flächeninhaltsberechnung

Wir wissen dabei, dass $MC = AC - \frac{1}{2} AB$:
![[Pasted image 20230903183114.png]]

Sodass 2) und 3) zu
2) $(c_1 - 7, c_2 + 3, c_3 - 5) - ( , , 0) = (0, 0, z)$
werden