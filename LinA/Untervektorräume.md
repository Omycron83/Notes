## Definition:

^abb4a8

Sei $V$ ein $K$-Vektorraum, dann heißt $W \subset V$ **Untervektorraum** von $V$ wenn:
1. $o \in W$
2. $v + w \in W \forall v,w \in W$
3. $\lambda v \in W \forall v \in W, \lambda \in K$

Äquivalenterweise kann man statt dem 1. Axiom auch annehmen, dass $W \neq \emptyset$:
$W \neq \emptyset \implies o \in W$: $\exists v \in W$, sodass $0 \cdot v = o \in W$ nach 3.
$o \in W \implies W \neq \emptyset:$ Sei dem kompetenten Leser überlassen.

Dabei ist $W$ dann, mit den induzierten Operationen, selbst wieder ein [[Vektorraum]] über $K$.
### Beweis:
$W$ ist immernoch eine abel'sche Gruppe, da es eine [[Untergruppen|Untergruppe]] bildet: das Nullelemente ist enthalten, die Verbindung ist abgeschlossen und durch $-1 \in K$ ist auch immer das Inverse enthalten. Alle weiteren Verbindungseigenschaften werden induziert.