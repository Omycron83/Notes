## Definition:
### Herleitung:
Betrachte man einen [[Gruppenhomomorphismen|Homomorphismus]] $\phi: G \rightarrow H$. Dann lässt sich die Äquivalenzrelation $a \sim_\phi b : \phi(a) = \phi(b)$ formulieren. Die Äquivalenzklassen $[a] := \{b \in G | \phi(b) = \phi(a)\}$ sind also jeweils die Mengen aller Elemente von $G$, die durch den Homomorphismus auf dasselbe Element abgebildet werden, also "zum selben Element werden" und "zu viel sind im Strukturanteil". 

Visualisierung:
![[Pasted image 20230811144522.png]]
Im Isomorphismusfall gibt es also z.B. $|G|$ Äquivalenzklassen.

Die Operation sei dabei Äquivalent zu solcher auf einer [[Faktorgruppe#^43cd1a |regulären Faktorgruppe]]
Dies ist wohldefiniert: $[a] \diamond [b] := [a \circ b] = \{g | \phi(g) = \phi(a \circ b) \} = \{g | \phi(g) = \phi(a) * \phi(b) \}$ Gäbe es nun ein weiteres $[a] = [a']$ und $[b] = [b']$, dann wäre $[a'] \diamond [b'] = [a' \circ b'] = \{g | \phi(g) = \phi(a') * \phi(b') \} = [a] \diamond [b]$. $\square$ 
## Satz:
Sei $\phi: G \rightarrow H$ ein Gruppenhomomorphismus, dann ist $G / Ker(\phi)$ eine Gruppe und 
$\phi\tilde : G / Ker(\phi) \rightarrow Im(\phi), \phi\tilde([a]) = \phi(a)$ ein Isomorphismus, d.h. $Im(\phi)$ und $G/Ker(\phi)$ sind strukturgleich und das folgende Diagramm kommutiert:
![[Pasted image 20230811163540.png]]

**Beweis**: 
Dass $Ker(\phi)$ eine Nebenklasse von $G$ darstellt sei dabei  
Die Faktorgruppe $G / Ker(\phi)$ ist hier die Gruppe $\{ \}