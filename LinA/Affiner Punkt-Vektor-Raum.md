Sei $M$ eine nichtleere Punktmenge, $V$ ein $K$-[[Vektorraum]] und $\phi: M \times M \rightarrow V$ eine injektive [[Abbildungen|Abbildung]]. Dann nennt man $(M, V, \phi)$ **affiner Punkt-Vektor-Raum**, wenn:
- Zu jedem $A \in M$ und zu jedem $x \in V$ genau ein $B \in M$ mit $\phi(A, B) = x := \vec{AB}$ 
- $\forall A, B, C \in M : \phi(A, B) + \phi(B, C) = \phi(A, C)$

Man kann dies als eine Einbettung eines [[Vektorraum|Vektorraumes]] in einen geometrischen Raum verstehen, wobei sich die Interpretation eines Vektors als Punktabbildung von einem Startpunkt $A$ auf einen Endpunkt $B$ anbietet.
# Eigenschaften:
- $\vec{PP} = o$
	$\phi(P, P) + \phi(P, P) = \phi(P, P) \implies \phi(P, P) = o$
- $\phi(P, Q) = o \implies P = Q$
	$\phi(P, Q) = \phi(P, P) \implies P = Q$ aus der Injektivität
- $-\vec{AB} = \vec{BA}$ 
	$\phi(A, B) + \phi(B, A) = \phi(A, A) = o$

