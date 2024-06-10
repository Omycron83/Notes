## Definition lineares Erzeugniss:
Seien $v_1, v_2, ..., v_r$ Vektoren des $K$-[[Vektorraum|Vektorraumes]] $V$. 
Dann nennt man $v \in V$ ein **lineares Erzeugniss** von $v_1, v_2, ..., v_r$ wenn es $\lambda_1, \lambda_2, ..., \lambda_r \in K$ gibt sodass $v = \lambda_1 \cdot v_1 + \lambda_2 \cdot v_2 + ... + \lambda_r \cdot v_r$ .

Die Menge aller möglichen Linearkombinationen einer solchen Familie nennt man **lineares Erzeugniss** oder auch **aufgespannter Raum**, wobei man $<v_1, ..., v_r>$ oder $span(v_1, ..., v_r)$ schreibt. 

## Definition lineare Unabhängigkeit:

^33f43f

Eine endliche Familie von Vektoren $v_1, ..., v_r$ wird linear unabhängig genannt, wenn 
$\sum_1^r v_r \lambda_r = o \implies \lambda_1 = ... = \lambda_r = 0$ , d.h. der Nullvektor nur trivial erzeugt werden kann.
Eine unendliche Familie ist dann linear unabhängig, wenn alle endlichen Teilfamilien linear unabhängig sind. ^e183ff

Dies bedeutet dann, dass kein Vektor das lineare Erzeugniss der anderen Vektoren sein kann:
gäbe es eine mögliche Kombination mit einem $\lambda_g \neq 0$ , dann wäre
$\lambda_1 \cdot v_1 + ... + \lambda_g \cdot v_g + .... + \lambda_r \cdot v_r = o$
$\Leftrightarrow \lambda_1 \cdot v_1 + ... + \lambda_r \cdot v_r = -\lambda_g \cdot v_g$
$\Leftrightarrow \frac{-\lambda_1}{\lambda_g} v_1 + .... + \frac{-\lambda_r}{\lambda_g} = v_g$                    Da $\lambda_g \neq 0$ 

Bemerkung: 
- Eine Familie, die den Nullvektor enthält, ist nie linear unabhängig.
- Eine Familie mit nur einem Vektor, ist nur dann linear abhängig, wenn es der Nullvektor ist
## Lineare Unabhängigkeit <-> Eindeutige Linearkombination:

^b227ab

Vektoren $v_1, ..., v_r$ sind genau dann linear unabhängig, wenn sich jedes $v \in <v_1, ..., v_r>$ eindeutig als Linearkombination der Familienmitglieder $v_i$ darstellen lässt.

Beweis:
	Nehme man an, es gäbe zwei unterschiedliche Darstellungen $v = \lambda_1 v_1 + ... + \lambda_r v_r= \mu_1 v_1 + ... \mu_r v_r$ 
	Dann wäre:
	$o = (\lambda_1 v_1 + ... + \lambda_r v_r) - (\mu_1 v_1 + ... + \mu_r v_r)$ 
	Und somit
	$o = (\lambda_1 - \mu_1) v_1 + ... + (\lambda_r - \mu_r) v_r$
	Genau dann, wenn $v_1, ... v_r$ linear unabhängig sind muss [[Lineare Erzeugnisse & Unabhängigkeit#^e183ff|per Definition]] jeweils
	$(\lambda_1 - \mu_1) = ... = (\lambda_r - \mu_r) = 0$
	Und somit
	$\lambda_1 = \mu_1, ..., \lambda_r = \mu_r$ 
	Wodurch die Linearkombination eindeutig ist, genau dann wenn sie linear unabhängig ist.









## $span(v_1, ..., v_n)$ ist ein Untervektorraum von $V$
Sei $span(v_1, ..., v_n)$ das Erzeugniss der mindestens einelementigen Familie $v_i \in V$. Dann konstituiert dieses Erzeugniss einen [[Untervektorräume|Untervektorraum]] von $V$. ^2f6e6d

Beweis:
	1. $o \in span(v_1, ..., v_n)$ sei klar, wenn alle Koeffizienten null gesetzt werden
	2. $v, w \in span(v_1, ..., v_n) \implies v + w = \lambda_1 v_1 + ... + \lambda_n v_n + \mu_1 v_1 + ... + \mu_n v_n$  $= (\lambda_1 + \mu_1) v_1 + ... + (\lambda_n + \mu_n) v_n \in span(v_1, ..., v_n)$ 
	3. $\lambda \in K, v \in span(v_1, ..., v_n) \implies \lambda v = \lambda (\lambda_1 v_1 + ... + \lambda_n v_n)$ $= \lambda \lambda_1 v_1 + ... + \lambda \lambda_n v_n \in span(v_1, ..., v_n)$ 
