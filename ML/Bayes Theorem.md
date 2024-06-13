Bayes theorem is a theorem in conditional probability theory serving as the basis for [[Bayesian Statistics]]. It is used to form a posterior probability by updating a prior by applying likelihood and normalizing by evidence. 
If the likelihood is equal to the evidence, i.e. the posterior distribution is equal to the prior, then the variables are independent from each other, and knowing one value does not contribute any information.
# Single-variate Bayes:
Given the prior probability $P(A)$ as well as the likelihood $P(B | A)$ and the marginal probability $P(B)$, one can compute the posterior probability $P(A | B)$ by
$P(A | B) = \frac{P(B | A) \cdot P(A)}{P(B)}$
	

Proof:
	We know that $P(A \land B) = P(A | B) \cdot P(B) = P(B | A) \cdot P(A)$. 
	$\Leftrightarrow_{P(B) \neq 0} P(A | B) = \frac{P(B | A) \cdot P(A)}{P(B)}$ 

# Multivariate Bayes:
