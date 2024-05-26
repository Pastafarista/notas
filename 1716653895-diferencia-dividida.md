---
id: 1716653895-diferencia-dividida
aliases:
  - Diferencia dividida
  - Diferencias divididas
tags:
  - cálculo-numérico
---

# Diferencia dividida

La diferencia dividida es una forma de calcular los coeficientes de un polinomio interpolador. Se pueden calcular recursivamente con la siguiente fórmula:

$$
f[x_0, x_1, \ldots, x_n] = \frac{f[x_1, x_2, \ldots, x_n] - f[x_0, x_1, \ldots, x_{n-1}]}{x_n - x_0}
$$

