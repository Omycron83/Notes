Die Menge aller [[Lineare Abbildungen#^587427|Endomorphismen]] eines Vektorraumes $V$, $End(V) := Hom(V, V)$ ist mit der Addition $+$ und der Komposition $\circ$ ein Ring $(End(V), +, \circ)$.

# Beweis:
Es sind die [[Ringe|Ringaxiome]] nachzuweisen:
1. $(End(V), +)$ ist eine [[Gruppen#^b82401|abel'sche Gruppe]], was aus dem [[Vektorraum der Homomorphismen|Vektorraumbeweis hervorgeht]].
2. Die Abbildungsverkettung ist immer [[Abbildungen#^f64bf0|assoziativ]]
3. Das Distributivgesetz gilt, da für alle $F, G, H \in End(V)$ gilt: $(F \circ (G + H))(v) = F((G + H)(v)) F(G(v) + H(v)) = F(G(v)) + F(H(v))$  $= (F \circ G)(v) + (F \circ H)(v)$ (linksseitige Distributivität) und $((F +G) \circ H)(v) = (F + G)(H(v)) = F(H(v)) + G(H(v)) = (F \circ H)(v) + (G \circ H)(v)$ (rechtsseitige Assozativität)
5. Es ist sogar ein [[Ringe#^ee24a3|Ring mit Eins]], da offensichtlich $id_V \in Hom(V)$.
$\square$

