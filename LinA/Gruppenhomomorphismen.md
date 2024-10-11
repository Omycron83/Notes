## Definition & Eigenschaften:
Ein Abbildung $\phi: G \rightarrow H$ zwischen zwei Gruppen [[Gruppen]]  $(G, \circ)$ , $(H, *)$ heißt **Homomorphismus,** wenn:
$\phi(a \circ b) = \phi(a) \, * \, \phi(b) \, \forall a,b \in G$

Dies bedeuted also, dass die Verknüpfung zweier Elemente der einen Gruppe "umgewandelt" in die andere dass gleiche sein muss wie die Verknüpfung der umgewandelten Elemente in der andern.
### Homomorphismuseigenschaften:
1. $\phi(e_G) = e_H$
	$\phi(a) * e_H = \phi(a) = \phi(a \circ e_G) = \phi(a) * \phi(e_G) \implies e_H = \phi(e_G)$ nach [[Gruppen#^c379c5 |Gruppeneigenschaft]] ^9d8893
2. $\phi(a^{-1}) = \phi(a)^{-1}$
	$\phi(a^{-1} \circ a) = e_H = \phi(a^{-1}) * \phi(a) \implies \phi(a^{-1}) = \phi(a)^{-1}$  ^6b6c8b


### Bild und Kern:
$Im(\phi) = \{\phi(a) \forall a \in G \}$ bzw. $= \{h \in H | \exists g \in G: \phi(g) = h \}$
$Ker(\phi) = \{g \in G: \phi(g) = e_H\}$

#### Satz: Kern und Bild sind [[Untergruppen]] von $G$ und $H$:
Beweis: Durchgehen der Unterguppeneigenschaften:
	1. Abgeschlossenheit: 
	Bild: Ist $\phi(a)$ und $\phi(b) \in H$ , dann ist $a,b \in G$ und nach Homomorphismuseigenschaft $\phi(a \circ b) = \phi(a) * \phi(b) \in Im(\phi)$ 
	Kern: $\exists a, b$ mit $\phi(a) = \phi(b) = e_H$ , dann ist $\phi(a \circ b) = \phi(a) * \phi(b) = e_H * e_H = e_H$ und so $a \circ b \in Ker(\phi)$ 
	2. Existenz neutralen Elements:
	Bild: Es gibt immer ein $e_G \in G$, sodass $\phi(e_G \circ e_G) = \phi(e_G) * \phi(e_G) = e_H * e_H = e_H \in Im(\phi)$ nach [[Gruppenhomomorphismen#^9d8893 |Homomorphismuseigenschaft]]
	Kern: Selbiger Beweis. 
	3. Existenz inversen Elements:
	Bild: Für jedes $a \in G \exists a^{-1} \in G$.  So ist auch $\phi(a^{-1} \circ e_G) = \phi(a^{-1}) * \phi(e_G) = \phi(a)^{-1} * e_H = \phi(a)^{-1} \in Im(\phi)$ nach [[Gruppenhomomorphismen#^6b6c8b |Homomorphismuseigenschaft]] 
	Kern: Ist $\phi(a) = e_H$ , dann ist $\phi(a \circ a^{-1}) = \phi(e_G) = \phi(a) * \phi(a^{-1}) = e_H * \phi(a^{-1}) = \phi(a^{-1}) = e_H$  

## Beispiele:
1. Ist $H$ eine Untergruppe von $G$ , dann ist die Einbettung $\phi: H \rightarrow G, \phi(h) = h \forall h \in H$ ein Homomorphismus.
	Der Beweis sei hier nun wirklich offensichtlich.
2. $\phi: (Z, +) \rightarrow (R^+, \cdot), a \mapsto exp(a)$ ist ebenfalls ein Homomorphismus:
	$e^{a + b} = e^{a} \cdot e^{b}$  nach den Potenzgesetzen
3. $\phi: (Z, +) \rightarrow (Z, +), \phi(a) \mapsto m \cdot a$ 
	$m \cdot (a + b) = m \cdot a + m \cdot b \, \forall \, m,a,b \in Z$ eine für Vektorräume interessante Eigenschaft


## Isomorphismen
Ein Homomorphismus ist ein Isomorphismus, wenn dieser bijektiv ist. 
Dies bedeuted also, dass die "Struktur" der Gruppen ähnlich ist: die Verknüpfung jeder zwei Elemente in der einen Gruppe korrespondiert (umgewandelt) zur Verknüpfung ihrer Gegenstücke in der anderen Gruppe. Korrespondierende Elemente werden also gleich verknüpft. 
Jeder Isomorphismus hat einen Umkehrisomorphismus, da alle bijektiven Abbildungen eine Inverse besitzen.
Also bedeuted ein Isomorphismus zwischen zwei Gruppen, dass diese als 'im wesentlichen gleich' zu betrachten sind, d.h. wenn man die Elemente nur entsprechend umebenennen würde wären sie gleich.