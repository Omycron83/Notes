## Definition:
### Normalteiler:
Eine Untergruppe $(N, \circ) \subset (G, \circ)$ nennt man Normalteiler einer Gruppe $G$, wenn $g \circ N = N \circ g \forall g \in G$, wobei $g \circ N$ auch $gN$ geschrieben und definiert wird als die Menge der linksseitigen Verknüpfungen aus einem $g \in G$ und allen $n \in N$, und korrespondierend $Ng$ die Menge der rechtsseitigen Verknüpfungen, d.h. wenn $e_1, e_2, e_3, ...$ die Elemente aus $N$ sind ist 
$g \circ N := \{g \circ e_1, g \circ e_2, g \circ e_3, ... \}, N \circ g := \{e_1 \circ g, e_2 \circ g, e_3 \circ g, ... \}$ 
Es fällt auf, dass in einer [[Gruppen#^b82401 |abel'schen Gruppe]] alle Untergruppen Normalteiler sind.

### Definition:
Eine Faktorgruppe oder Quotientengruppe ist die Menge der Nebenklassen einer Gruppe $G$ bezüglich eines Normalteilers $N$, und definiert als $G / N := \{g \circ N \, \forall \, g \in G \}$. Es fällt auf, dass alle "Nebenklassenkandidaten" mit $g_1 \circ N = g_2 \circ N$ redundant sind und zu einer Nebenklasse werden. Die Repräsentanten $a$  dieser Nebenklasse kann man als Mitglieder einer Äquivalenzklasse auffassen und als $[a]$ schreiben. 

Definiere man nun $[a] \diamond [b] := [a \circ b]$, also die Operation, bei der die Repräsentanten von zwei Äquivalenzklassen verknüpft werden zum Repräsentanten einer weiteren, die die Verknüpfung der Repräsentanten enthält.   ^43cd1a
## Beispiele:
Betrachte man $Z / 6Z$. Dies ist die Faktorgruppe der ganzen Zahlen mit der Addition bezüglich der Untergruppe der Vielfachen der ganzen Zahlen. Die Nebenklassen sind dabei also: 
$\{\{...0, 6, 12...\}, \{...1, 7, 13...\}, \{...2, 8, 14... \}, \{...3, 9, 15... \}, \{...4, 10, 16... \}, \{5, 11, 17... \}  \}$
Es fällt auf, dass wieder $7 + 6N = 1 + 6N$ wäre, was aus der Unendlichkeit der Menge hervorgeht: das "Verschieben" einer "Sechsfachen-Stelle" hat keine weitere Relevanz. 
So bilden sich die Nebenklassen $[0] := 6Z + 0, [1] := 6Z + 1, [2] := 6Z + 2, [3] := 6Z + 3, [4] := 6Z + 4, [5] := 6Z + 5$ .
Jedes $g \in Z$ wird also lediglich $mod \; 6$ genommen.
Betrachte man nun die Operation auf dieser Faktorgruppe: $[a + b]$ .
Dann wäre z.B. $[5 + 1] = [6] = [0]$, $[4 + 1] = [5]$ oder $[4 + 5] = [9] = [3]$ ihrer jeweiligen Äquivalenzklasse bzw. Nebenklasse zugeordnet.
