# Aufgabe:
Seien $A = (7, -3, 5)$ und $B = (4, 1, 5)$. 

a) Bestimmen sie den Abstand von $A$ und $B$.

b) Bestimmen sie einen Punkt $C$ so, dass das Dreieck $ABC$ gleichschenklig mit Basis $AB$ ist, orthogonal zur x-y-Ebene steht und einen Flächeninhalt von $10$ FE besitzt.
# Lösung:
a) Der Abstand entspricht der Norm des Vektors zwischen den beiden Punkten:
$|| A - B|| = ||(3, -4, 0)|| = \sqrt{3^2 + 4^2} = 5$.

b)
Das Dreieck muss dann drei Gleichungen erfüllen:

1) $|| C - A|| = ||C - B||$ -> Schenkel gleich lang
2) $C = (c_1, c_2, 5)$  -> Orthogonal = Senkrecht auf
3) $||MC|| \cdot ||\frac{1}{2} AB|| = 12$ -> Triviale Flächeninhaltsberechnung

Wir wissen dabei, dass $MC = AC - \frac{1}{2} AB$:
![[Pasted image 20230903183114.png]]

Sodass Bedingungen zu
1) $(c_1 - 7)^2 + (c_2 + 3)^2 = (c_1 - 4)^2 + (c_2 - 1)^2$
2) $c_3 = 5$
3) $||(c_1 - 5.5, c_2 + 1, c_3 - 5)|| \cdot \frac{1}{2}||(-3 , 4, 0)|| = 12$ 

Vereinfache man:
1.)
$\Leftrightarrow c_1^2 - 14c_1 + 49 + c_2^2 + 6c_2 + 9 = c_1^2 - 8c_1 + 16 + c_2^2 - 2c_2 + 1$
$\Leftrightarrow -6 c_1 + 41 = -8c_2$
$\Leftrightarrow c_2 = \frac{6}{8} c_1 - \frac{41}{8}$
$\Leftrightarrow c_2 = \frac{3}{4}c_1 - \frac{41}{8}$

2.) $c_3 = 5$

3.)
$((c_1 - 5.5)^2 + (c_2 + 1)^2 + (c_3 - 5)^2) \cdot \frac{1}{2}(5)= 12$
$c_3 = 5$ einsetzen:
$\Leftrightarrow (c_1^2 - 11c_1 + 30.25 + c_2^2 + 2c_2 + 1 + 0) \cdot (2.5) = 12$
$\Leftrightarrow c_1^2 - 11c_1 + 31.25 + c_2^2 + 2c_2 = 4.8$

Nun kann man die 1. Gleichung in die 2. Einsetzen:
$c_1^2 - 11c_1 + 31.25 + (\frac{6}{8}c_1 - 5.125)^2 + 2(\frac{6}{8}c_1 - 5.125) = 4.8$
$\Leftrightarrow c_1 = 5 \pm \sqrt{3.072} \Leftrightarrow c_{1, 1} \sim 7.253, c_{1, 2} \sim 3.747$

Damit ist $c_{2, 1} \sim 0.3148, c_{2, 2} \sim -2.3146$


Sodass $C = (c_1, c_2, c_3) = ()$
