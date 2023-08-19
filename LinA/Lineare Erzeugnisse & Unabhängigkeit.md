## Definition lineares Erzeugniss:
Seien $v_1, v_2, ..., v_r$ Vektoren des $K$-[[Vektorraum|Vektorraumes]] $V$. 
Dann nennt man $v \in V$ ein **lineares Erzeugniss** von $v_1, v_2, ..., v_r$ wenn es $\lambda_1, \lambda_2, ..., \lambda_r \in K$ gibt sodass $v = \lambda_1 \cdot v_1 + \lambda_2 \cdot v_2 + ... + \lambda_r \cdot v_r$ .

Die Menge aller möglichen Linearkombinationen einer solchen Familie nennt man **lineares Erzeugniss** oder auch **aufgespannter Raum**, wobei man $<v_1, ..., v_r>$ oder $span(v_1, ..., v_r)$ schreibt. 



## Definition lineare Unabhängigkeit:
Eine endliche Familie von Vektoren $v_1, ..., v_r$ wird linear unabhängig genannt, wenn 
$\sum_1^r v_r \lambda_r = o \implies \lambda_1 = ... = \lambda_r = 0$ , d.h. der Nullvektor nur trivial erzeugt werden kann.
Eine unendliche Familie ist dann linear unabhängig, wenn alle endlichen Teilfamilien linear unabhängig sind.

Dies bedeutet dann, dass kein Vektor das lineare Erzeugniss der anderen Vektoren sein kann:
gäbe es eine mögliche Kombination mit einem $\lambda_g \neq 0$ , dann wäre
$\lambda_1 \cdot v_1 + ... + \lambda_g \cdot v_g + .... + \lambda_r \cdot v_r = o$
$\Leftrightarrow \lambda_1 \cdot v_1 + ... + \lambda_r \cdot v_r = -\lambda_g \cdot v_g$
$\Leftrightarrow \frac{-\lambda_1}{\lambda_g} v_1 + .... + \frac{-\lambda_r}{\lambda_g} = v_g$                    Da $\lambda_g \neq 0$ 

### Lineare Unabhängigkeit <-> Eindeutige Linearkombination:
Vektoren $v_1, ..., v_r$ sind genau dann linear unabhängig, wenn sich jedes $v \in \{v_1, ..., v_r\}$ eindeutig als Linearkombination der anderen $v_i$ darstellen lässt.

Beweis:
	Nehme man an, es gäbe zwei unterschiedliche Darstellungen $v_i = \lambda_1 v_1 + ... + \lambda_{i - 1} v_{i - 1} + \lambda_{i + 1} v_{i + 1} + ... + \lambda_r v_r= \mu_1 v_1 + ... + \mu_{i - 1} v_{i - 1} + \mu_{i + 1} v_{i + 1} +... + \mu_r v_r$




