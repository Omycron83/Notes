Sei $F : K^n \rightarrow K^m$ eine linear Abbildung. Gibt es genau eine Matrix $A \in K^{m \times n}$ mit $A \cdot x = F(x)$ für alle $x \in K^n$ in Spaltenform bezüglich der trivialen Basis der Einheitsvektoren $e_i$ des $K^n$.
# Beweis:
Es sei klar, dass ein jedes $x \in K^n$ dargestellt werden kann als $x = \lambda_1 e_1 + ... + \lambda_n e_n$. Dann ist $F(x) = F(\lambda_1 e_1 + ... + \lambda_n e_n) = \lambda_1 F(e_1) + ... + \lambda_n F(e_n)$.

Da wir es hier mit einem Körpertupel-Vektorraum zu tun haben, lassen sich die verschiedenen Vektoren als Spaltenvektoren (bzw. Zeilenvektoren) darstellen, auf denen man ebenfalls die [[Matrizen#^bcdd4e|Matrizenmultiplikation]] definieren kann. 

Dann kann man nun darstellen: $F(x) = \lambda_1 F(e_1) + ... + \lambda_n F(e_n) = \begin{pmatrix} \lambda_1 F(e_1)_1 + ... + \lambda_n F(e_n)_1 \\ ... \\ \lambda_1 F(e_1)_n + ... + \lambda_n F(e_n)_n \end{pmatrix}$ 
$= \begin{pmatrix} | & ... & | \\ F(e_1) & ... & F(e_n) \\ | & ... & | \end{pmatrix} \cdot \begin{pmatrix} \lambda_1 \\ ... \\ \lambda_n \end{pmatrix} = \begin{pmatrix} | & ... & | \\ F(e_1) & ... & F(e_n) \\ | & ... & | \end{pmatrix} \cdot x$ 

Wobei die Matrix $\in K^{m \times n}$ und $x \in K^{n \times 1}$, wodurch das Ergebniss richtigerweise $\in K^{m \times 1}$ ist, und, wie gezeigt, der linearen Abbildung äquivalent ist. 
Die Eindeutigkeit folgt aus der Eindeutigkeit der Bildvektoren $F(e_i)$.
