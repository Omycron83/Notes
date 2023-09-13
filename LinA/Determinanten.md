# Definition:
Eine Abbildung $V^n \rightarrow K, \Delta (a_1, …, a_n) = l \in K$ wird Determinantenabbildung genannt, wenn 
- Sie multilinear ist, d.h. $\Delta(a_1, …,\lambda a + \mu a‘,…, a_n) = \Delta(a_1, …, \lambda a + \mu a‘, …, a_n) \forall a_i \in V$ 
 - Sie alternierend ist, d.h. $\Delta (a_1, …, a, …, a, …, a_n)= 0$

Bemerkung: 
Die Nullabbildung $(a_1, …, a_n) \mapsto 0 \forall a_1, …, a_n \in V$ erfüllt offensichtlich beide Eigenschaften. Man nennt sie auch die **triviale** Determinantenfunktion.
## Eigenschaften:

### Determinantenfunktion <-> Lin. Abh. Familien $\mapsto$ 0
Betrachte man eine multilineare Funktion $\Delta : V^n \rightarrow K$. Dann sind folgende Aussagen äquivalent:
1. $\Delta$ ist außerdem alternierend und somit eine Determinantenfunktion
2. Für jeden n-Tupel linear abhängiger Vektoren $(a_1, …, a_n)$ gilt: $\Delta (a_1,…, a_n) = 0$

Beweis:
Da die multilinearität in beiden Fällen gilt, lässt sich durch die lineare Abhängigkeit umschreiben:
$\Delta(a_1, …, a_i, …, a_n) = \Delta (a_1, …, \lambda_1 a_1 + … + \lambda_{i-2})$
### Argumentänderung, Argumentpermutationen, Lineare Invarianz
Sei $\Delta$ eine Determinantenfunktion.
