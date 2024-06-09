---
id: 1713020577-polinomio-de-lagrange-por-forma-de-lagrange
aliases:
  - Polinomio de lagrange por forma de lagrange
  - Forma de Lagrange
tags:
  - cálculo-numérico
---

# Polinomio de Lagrange por forma de Lagrange

El [[1709641715-polinomio-interpolador-de-lagrange|polinomio interpolador de Lagrange]] se puede hallar por la forma de Lagrange. La forma de Lagrange es:

$$
P(x) = f(x_0) l_0(x) + f(x_1) l_1(x) + \ldots + f(x_N) l_N(x)
$$

Donde:

$$
l_i(x) = \frac{(x - x_0) \ldots (x - x_{i-1})(x - x_{i+1}) \ldots (x - x_N)}{(x_i - x_0) \ldots (x_i - x_{i-1})(x_i - x_{i+1}) \ldots (x_i - x_N)} = \prod_{j=0, j \neq i}^{N} \frac{x - x_j}{x_i - x_j}
$$
