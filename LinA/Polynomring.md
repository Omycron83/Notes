Sei $K[x]$ die Menge aller [[Polynome]] mit Koeffizienten in $K$ in in der Unbestimmten $x$. Dann koennen wir die Addition zwischen zwei Polynomen $f = \sum_{k = 0}^n a_k \cdot x^k, g = \sum_{k = 0}^n b_k \cdot x^k$ als $f + g := \sum_{k = 0}^n (a_k + b_k) \cdot x^k$ 
und die Multiplikation als $f \cdot g := \sum_{k = 0}^{n + m}(a_0 \cdot b_k + a_1 b_{k - 1} +... + a_k b_0) \cdot x^k$ 
definieren.

Dann ist $(K[x], +, \cdot)$ ein [[Ringe#^ee24a3|kommutativer Ring mit Eins]].

Beweis:
	Die Additionsaxiome induzieren sich aus denen der Koeffizienten.
	Zusaetzlich sind ebenfalls die Assoziativitaet, Kommutativitaet und Eins-Existenz einfach nachzuvollziehen.
	Das Distributivgesetz gilt aus bekannter Begruendung.

## Gradformel:
Seien $f, g \in K[x]$. Dann gilt:
- $deg(f + g) \le max(deg(f), deg(g))$
- $deg(f \cdot g) = deg(f) + deg(g)$
Offensichtlich.
