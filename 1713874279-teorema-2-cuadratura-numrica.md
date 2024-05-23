---
id: 1713874279-teorema-2-cuadratura-numrica
aliases:
  - Teorema 2 cuadratura numérica
tags:
  - cálculo-numérico
---

# Teorema

Dados $N\ge 0$ y $N+1$ nodos $x_i$ dos a dos distintos, la [[1713865555-reglas-de-cuadratura|reglas de cuadratura]] [[1713873299-mtodo-interpolatorio|interpolatorias]] correspondiente a los nodos,

$$
\mathcal{I}_{N+1}(f) = \alpha_{0}f(x_{0}) + \alpha_{1}f(x_{1}) + \ldots + \alpha_{N}f(x_{N}) \text{ con } \alpha_i = \int_{a}^{b} l_i(x) dx
$$

tiene grado de exactitud $\ge N$.

### Demostración

Si $f$ es un polinomio de grado $\le N$, entonces $f=P$ por ser su [[1709641715-polinomio-interpolador-de-lagrange|polinomio interpolador de Lagrange]] 

$$
\mathcal{I}_{N+1}(f) = \mathcal{I}(P) = \mathcal{I}(f)
$$
