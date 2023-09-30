Die Menge aller [[Lineare Abbildungen|Vektorraumhomomorphismen]] $Hom(V,W)$ ist ein Untervektorraum von $Abb(V, W) = W^V$  .
# Beweis:
Hier müssen lediglich die [[Untervektorräume|Untervektorraumaxiome]] gelten:
1. Die Nullabbildung $F(v) = 0$ ist linear, also in $Hom(V,W)$ enthalten.
2. Abgeschlossen ggü. Addition, da die Summe zweier linearen Abbildungen ebenfalls linear ist:
	$(F + G)(\lambda v + w) = F(\lambda v + w) + G(\lambda v + w) = \lambda F(v) + F(w) + \lambda G(v) + G(w)$ 
	$= \lambda (F(v) + G(v)) + F(w) + G(w) \lambda (F + G)(v) + (F + G)(w)$
3. Abgeschlossen ggü. Skalarmultiplikation, da:
	$(\lambda F)(\mu v + w) = \lambda F(\mu v + w) = \lambda \mu F(v) + \lambda F(w) = \mu (\lambda F(v)) + (\lambda F(w))$ 
