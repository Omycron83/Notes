Eine Variable $X$ nennt man zufällig, wenn ihr tatsächlich eingenommener Wert nicht vorhergesagt werden kann, jedoch alle möglichen Werte bekannt sind. 

Das Manifestieren eines solchen Wertes nennt man **Ereigniss**, und die Menge der möglichen Ereignisse die **Ereignismenge** $\Omega$ .

Die Teilmengen von $\Omega$ nennt man **Ergebnisse**, wobei es offensichtlich $2^{|\Omega|}$ Ergebnisse gibt.

Dabei kann die Wahrscheinlichkeit eines jeden Ereignisses $x_i$ frequentistisch betrachtet werden als das Verhältnis $lim_{n \rightarrow \infty} \frac{\sum_1^n 1_{\{x_i\}}(X)}{n}$, wobei $1$ die Indikatorfunktion darstellt.

Die Wahrscheinlichkeitsverteilungsabbildung $P: \Omega \rightarrow [0; 1]$, $P(x_i) \mapsto lim_{n \rightarrow \infty} \frac{\sum_1^n 1_{\{x_i\}}(X)}{n}$  bildet ein jedes Ereigniss auf seine Wahrscheinlichkeit ab. Dabei ist die Summe der Bildelemente stets $1$.

Der Erwartungswert eines Ereignisses ist dabei:
$E(X) = \sum_{i = 1}^{|\Omega|} P(X) \cdot X(w_i)


