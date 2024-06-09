---
id: 1713020438-polinomio-de-lagrange-por-coeficientes-indeterminados
aliases:
  - Polinomio de lagrange por coeficientes indeterminados
tags:
  - cálculo-numérico
---

# Polinomio de lagrange por coeficientes indeterminados

Sabemos que el [polinomio interpolador de Lagrange](1709641715-polinomio-interpolador-de-lagrange) cumple:

$$
P(x_{0}) = f(x_{0}), \ldots, P(x_{N}) = f(x_{N})
$$

Podemos construir el siguiente [sistema de ecuaciones](1709024526-sistema-de-ecuaciones-lineales):

$$
\begin{cases}
a_0 + a_1 x_0 + a_2 x_0^2 + \ldots + a_N x_0^N = f(x_0) \\
a_0 + a_1 x_1 + a_2 x_1^2 + \ldots + a_N x_1^N = f(x_1) \\
\vdots \\
a_0 + a_1 x_N + a_2 x_N^2 + \ldots + a_N x_N^N = f(x_N) \\
\end{cases}
$$

La matriz de este sistema es de tipo Vandermonde con nodos dos a dos distintos y por lo tanto es no singular. Por lo tanto, el sistema tiene solución única.
