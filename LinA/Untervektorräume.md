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

# Durchschnitte von Untervektorräumen:

Seien $W_1, ..., W_n$ Untervektorräume eines Vektorraumes $V$. Dann ist $W = \bigcap_{i \in \{1, ..., n\}} W_i$ ebenfalls ein Untervektorraum von $V$. 
# Beweis:
Prüfe man die oben gezeigten Untervektorraumaxiome:
1. $o \in W$, da durch Untervektorraumstatus $o \in W_i$
2. $v + w \in W$, da $v, w \in W_i \forall i \in \{1, ..., n\} \implies v + w \in W_i$
3. $\lambda v \in W$, da $v \in W_i \forall i \in \{1, ..., n\} \implies \lambda v \in W_i$

Dadurch, dass alle Untervektorräume die notwendigen Eigenschaften für alle Elemente erfüllen, erfüllt auch der Durchschnitt diese für all diese Elemente. 

Man notiere, dass dies für die Vereinigung nicht i.A. gilt.
Als Beispiel dafür $\{ a\cdot(1, 0)|\forall a \in R\}$ und $\{b \cdot (0, 1) | \forall \in R\}$ als $\subset R^2$ , wo die Addition nicht abgeschlossen ist.