Eine Abbildung $h$ ist eine [[Relationen|Relation]] zwischen zwei Mengen $M, N$ nennt man Abbildung, wenn sie **wohldefiniert** ist, d.h.:
1. Sie **linksvollständig** ist: $\exists \text{(mind. 1)}(x, z) \in h \forall x \in M$ 
2. Sie **rechtseindeutig** ist: $\exists \text{(max. 1)} (x, z) \in h \forall x \in M$ 

Man schreibt dann anstatt $(x,y) \in h$ auch $h(x) = y$.
Man nennt $M$ den Urbild, $N$ den Bildbereich.

Man nennt eine Abbildung injektiv, wenn $h(x) = h(z) \implies x = z$.
Man nennt eine Abbildung surjektiv, wenn $\{h(x) \forall x \in M\} = N$ 
Man nennt eine Abbildung bijektiv, wenn sie surjektiv und injektiv ist. ^4b4823

# Eigenschaften:

## Assoziativität der Verkettung $\circ$:
Seien $f: A \rightarrow B$ und $g: B \rightarrow C$ sowie $l: C \rightarrow D$ Abbildungen.
Dann gilt $f \circ (g \circ l) = (f \circ g) \circ l$. 
^f64bf0
Beweis:
$f \circ (g \circ l) = f(g \circ l) = f(g(l(c))) = (f \circ g)(l(c)) = (f \circ g) \circ l$ 

## Eindeutiges Inverses bijektiver Abbildungen:
Sei $f: A \rightarrow B$ eine bijektive Funktion. Dann gibt es ein $f^{-1}: B \rightarrow A$ mit $f \circ f^{-1} = id_B$ und $f^{-1} \circ f = id_A$. 

Beweis:
Sei $f(a) = b$. Dann konstruiere man die gewünschte inverse Funktion mit $f^{-1}(b) = a$. Diese ist wohldefiniert, da durch die Injektivität von $f$ nur jeweils ein $a$ auf $b$ abgebildet wird. Durch die Surjektivität ist dann garantiert, dass $f^{-1}$ auf $B$ definiert ist. 
Die Verkettungen sind dann: $f \circ f^{-1} = f(f^{-1}(b)) = f(a) = b \Leftrightarrow f \circ f^{-1} = id_B$ 
$f^{-1} \circ f = f^{-1}(f(a)) = f^{-1}(b) = a \Leftrightarrow f^{-1} \circ f = id_A$.

Bonus: diese Funktion ist sogar surjektiv, da $f$ jedem $a \in A$ ein $b$ zuordnet, und injektiv, da diese zuordnung natürlich eindeutig ist, also insgesamt bijektiv.