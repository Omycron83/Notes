Eine Variable $W$ nennt man zufällig, wenn ihr tatsächlich eingenommener Wert nicht vorhergesagt werden kann, jedoch alle möglichen Werte bekannt sind. 

Das Manifestieren eines solchen Wertes nennt man **Ereigniss**, und die Menge der möglichen Ereignisse die **Ereignismenge** $\Omega$ .

Die Teilmengen von $\Omega$ nennt man **Ergebnisse**, wobei es offensichtlich $2^{|\Omega|}$ Ergebnisse gibt.

Dabei kann die Wahrscheinlichkeit eines jeden Ereignisses $w_i$ frequentistisch betrachtet werden als das Verhältnis $lim_{n \rightarrow \infty} \frac{\sum_1^n 1_{\{w_i\}}(W)}{n}$, wobei $1$ die Indikatorfunktion darstellt.

Die Wahrscheinlichkeitsverteilungsabbildung $P: \Omega \rightarrow [0; 1]$, $P(w_i) \mapsto lim_{n \rightarrow \infty} \frac{\sum_1^n 1_{\{w_i\}}(W)}{n}$  bildet ein jedes Ereigniss auf seine Wahrscheinlichkeit ab. Dabei ist die Summe der Bildelemente stets $1$.

Hat die Variable einen numerisch-relevanten Wert, so kann man außerdem die Zufallsgrößenabbildung $X: \Omega \rightarrow R, w_i \mapsto X(w_i)$ definieren. 

Der Erwartungswert eines Ereignisses ist dabei:
$E(X) = \sum_{i = 1}^{|\Omega|} P(X) \cdot X(w_i)$.




