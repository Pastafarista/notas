---
id: 1716650816-forma-de-lagrange
aliases:
  - Forma de Lagrange
  - Base de Lagrange
tags:
  - cálculo-numérico
---

# Forma de Lagrange

En la forma de Lagrange, el [[1709641715-polinomio-interpolador-de-lagrange|polinomio interpolador]] tiene la siguiente forma:

$$
P(x) = \sum_{i=0}^{n} f(x_i) l_i(x)
$$

Donde los pesos, $l_i(x)$, son los polinomios de la base de Lagrange:

$$
l_i(x) = \prod_{j=0, j \neq i}^{n} \frac{x - x_j}{x_i - x_j} 
$$

