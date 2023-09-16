## Definition
Eine Menge $M$ zusammen mit einer Abbildung bzw. **Verknüpfung** $\circ$ ($\circ : M \times M \rightarrow M$, **Infixnotation**: $\circ(a, b) := a \circ b$) auf dieser Menge eine algebraische Struktur $(M, \circ)$ die man **Gruppe** nennt, wenn:
1. Die Verknüpfung auf der Menge **abgeschlossen und wohldefiniert** ist.
2. Das **Assoziativgesetz** gilt: $a \circ (b \circ c) = (a \circ b) \circ c \,  \forall a,b,c \, \in M$ 
3. Ein eindeutiges (links)**neutrales Element** $e$  gibt, mit $a \circ e = e \circ a = a \, \forall a \in M$
4. Für jedes Element ein (links)**inverses** $a^{-1}$ existiert: $\exists \, a^{-1} \in M \, \forall a \in M:  a^{-1} \circ a = a \circ a^{-1}= e$

Gruppen sind also [[Halbgruppen]] mit inversen Elementen.

Dabei muss das Kommutativgesetz nicht gelten. Das heißt insbesondere, dass die rechtsseitige Verknüpfung i.A. nicht gleich der Linksseitigen ist. 

Ist die Gruppe jedoch **kommutativ**, d.h. gilt es für jede ihrer Elementverknüpfungen, so nennt man diese **abelsche** Gruppe, und die Verknüpfungen sind wieder äquivalent. ^b82401
### Gruppeneigenschaften:
Aus der Gruppendefinition lässt sich herleiten:
- Dass das linksinverse Element gleich dem Rechtsinversen ist:
$a_l^{-1} \circ a = e$
$\Leftrightarrow (a_l^{-1} \circ a) \circ a_r^{-1} = a_r^{-1}$
$\Leftrightarrow a_l^{-1} \circ e = a_r^{-1}$    

- Dass das inverse Element eindeutig ist:
$a_1^{-1} \circ a = a_2^{-1} \circ a$        
$\Leftrightarrow a_1^{-1} \circ a \circ a_2^{-1} = a_2^{-1}$ 
$\Leftrightarrow a_1^{-1} = a_2^{-1}$               

- Dass das linksneutrale Element gleich dem Rechtsneutralen ist:
$a \circ e_r = e_l \circ a$              
$\Leftrightarrow e_r = a^{-1} \circ e_l \circ a$ 
$\Leftrightarrow e_r = e_l \circ (a^{-1} \circ a)$
$\Leftrightarrow e_r = e_l$

- Dass das neutrale Element auch wirklich eindeutig ist:
$e_1 = e_2 \circ e_1 = e_1 \circ e_2 = e_2$

- Dass $(a^{-1})^{-1} = a$:
$(a^{-1})^{-1} \circ a^{-1} = e$    
$\Leftrightarrow (a^{-1})^{-1} = e \circ a$   
$\Leftrightarrow (a^{-1})^{-1} = a$        

- Dass $(a \circ b)^{-1} = b^{-1} \circ a^{-1}$:
$(a \circ b)^{-1} \circ (a \circ b) = e$   
$\Leftrightarrow (a \circ b)^{-1} \circ a = e \circ b^{-1}$ 
$\Leftrightarrow (a \circ b)^{-1} = e \circ b^{-1} \circ a^{-1}$ 
$\Leftrightarrow (a \circ b)^{-1} = b^{-1} \circ a^{-1}$   

- Dass $a \circ b = a \circ c \implies b = c$:
$a \circ b = a \circ c$
$\Leftrightarrow a^{-1} \circ a \circ b = a^{-1} \circ a \circ c$
$\Leftrightarrow e \circ b = e \circ c$
$\Leftrightarrow b = c$  ^c379c5
## Beispiele:
Die Permutationsgruppe $Sym(X)$  enthält als Elemente alle bijektiven Abbildungen auf der Menge $X$ mit der Verknüpfung der Verkettung. Ihre Elemente nennt man auch Permutationen.
	Abgeschlossenheit und Wohldefiniertheit seien klar.
	Das Assoziativgesetz gilt, da Abbildungsverknüpfungen immer assoziativ sind.
	Das neutrale Element ist die Identität.
	Das Inverse ist die inverse Permutation, die existiert da jede bijektive Abbildung eine inverse Abbildung besitzt.
	Übrigens: da es $n!$ Permutationen besitzt, hat die Gruppe $n!$ Elemente.

- Diedergruppe als Symmetriegruppe eines Quadrates:
	![[Pasted image 20230810202617.png]]
	1. Die Untergruppe $D_4$  als Drehungsgruppe eines Quadrates (Drehung um $90, 180, 270, 360/0$ Grad der Ecke $a$ auf $d_a$):
		Abgeschlossenheit und Wohldefiniertheit sind offensichtlich
		Das Assoziativgesetz greift, da die Rotation Ausführungsinvariant ist
		Das neutrale Element ist die Rotation um $0$ bzw. $360$ Grad
		Das Inverse der Rotation um $90$ Grad ist die um $270$ Grad, und das Inverse der $180$ und $0$ Grad sie selbst bzw. umgekehrt
	2. Die Untergruppe $D_4$ als Spiegelungsgruppe der Ecke 0 auf die Ecke a auf $s_a$ (können als Permutationen aufgefasst werden):
		Abgeschlossenheit und Wohldefiniertheit sind offensichtlich
		Das Assoziativgesetz greift, da durch Permutationsabbildungen darstellbar, und Abbildungsverknüpfung immer Assoziativ
		Das neutrale Element ist die Spiegelung $s_0$
		Zur Inversenbetrachtung die Permutationsbetrachtung: $s_0 = (0, 1, 2, 3), s_1 = (1, 0, 3, 2), s_2 = (2, 1, 0, 3), s_3 = (3, 2, 1, 0)$
		Man erkennt: jedes ist sein eigenes Inverses
	3. Die Diedergruppe $D_4$ als Gruppe mit beiden Operationen:
		Die Abgeschlossenheit und Wohldefiniertheit sei wieder offensichtlich
		Die neutralen Elemente und Inversen bleiben gleich
		Es bleibt lediglich die Transitivität zu zeigen:
		Diese wird gilt durch die Permutationsbetrachtung: auch $d_0, d_1, d_2, d_3$ können als Permutationen betrachtet werden:
		$d_0 = (0, 1, 2, 3), d_1 = (1, 2, 3, 0), d_2 = (2, 3, 0, 1), d_3 = (3, 0, 1, 2))$
		Das Assoziativgesetz greift, da durch Permutationsabbildungen darstellbar, und Abbildungsverknüpfung immer Assoziativ



