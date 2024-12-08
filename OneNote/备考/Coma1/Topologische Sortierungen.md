# Definition Ordnungen:

![Definition Eine Relation R C S x S heißt partielle Ordnung auf der Menge S, für alle a, b, c S gilt. falls (Reflexivität) (Antisymmetrie) (Transitivität) R heißt totale (oder lineare) Ordnung, falls zusätzlich für alle a, b e S gilt: Notation Statt (a, b) e R schreiben wir auch aRb (z.B. a < b für a, b e R). ](Exported%20image%2020241208232740-0.png)  

Bsp.:

![{ (a, b) e N x N I a < b} ist totale Ordnung auf N. { (a, b) I a > b} ist totale Ordnung auf R. { (a, b) e N I a teilt b} ist partielle Ordnung auf N. bl C12J, b2 ist partielle Ordnung auf R2. bl C12J, b2 ist totale Ordnung auf („lexikographische Ordnung"). Sei G — (V, E) azyklischer gerichteter Graph, d.h. G hat keinen Kreis. R := { (v, w) e V V 1 3v-w-Weg in G} partielle Ordnung auf V Beispiel ](Exported%20image%2020241208232740-1.png)  

# Definition Topologische Sortierung:

![Definition Es sei partielle Ordnung auf endlicher Menge S mit ISI = n. Eine Bijektion 71 : {1, 2, ... , n} + S heißt topologische Sortierung, falls 7T(j) 7T(i) für i < j. Ist totale Ordnung, so ist topologische Sortierung 71 eindeutig. Es gilt 71(1) 71(2) 7t(n). In diesem Fall heißt 71 Sortierung von S. ](Exported%20image%2020241208232745-2.png)  

Bsp.:

![Es sei S Beispiel 1: 12 7, 2, 3, 9, 6, 5} und « die Teilbarkeitsrelation. Topologische Sortierung: Beispiel 2: Azyklischer Graph mit Erreichbarkeitsrelation. 1 7T(i) 5 i 7t(i) 2 3 1 1 3 7 2 2 4 2 3 4 5 6 4 3 6 12 5 5 7 9 6 6 O O Topologische Sortierung: ](Exported%20image%2020241208232745-3.png)  

# Definition allgemeines Sortierproblem:

![Es sei partielle Ordnung auf endlicher Menge S mit ISI = n. Sortierproblem: Gegeben S und 3, bestimme eine topologische Sortierung 71. Dabei sollen sowohl S als auch die topologische Sortierung als Liste/Array dargestellt sein, d.h.: Liste/Array A der Länge n mit Einträgen in S, d.h. Input: S gegeben als „Orakel" (d.h. Funktion, die für Eingabe a, b e S zurück gibt, ob a b) Output: Topologische Sortierung 71 : {0, 1, ... , n 71(i) n(j) 1} + S kodiert als Array/Liste, so dass gilt für i < j. ](Exported%20image%2020241208232747-4.png)