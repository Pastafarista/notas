---
id: 1716491727-teorema-de-bayes
aliases:
 - Teorema de Bayes
---


- Sea $\{A_i\}_{i=1,...,n} \subseteq \mathcal{A}$ una [[1716491727-particin-de-sucesos|Partición de sucesos]] de $\Omega$, entonces para todo [[1716491727-sucesos|suceso]] $B \subseteq \mathcal{A}$ se cumple que
$$P(A_i/B) = \frac{P(B/A_i) \cdot P(A_i)}{P(B)}$$

- Usando el [[1716491727-teorema-de-probabilidad-total|Teorema de probabilidad total]]
$$P(A_i/B) = \frac{P(B/A_i) \cdot P(A_i)}{\sum_{i=1}^n P(B/A_i) \cdot P(A_i)}$$