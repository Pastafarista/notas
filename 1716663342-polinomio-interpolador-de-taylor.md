---
id: 1716663342-polinomio-interpolador-de-taylor
aliases:
  - Polinomio interpolador de Taylor
tags:
  - cálculo-numérico
---

# Polinomio interpolador de Taylor

El **polinomio interpolador de Taylor** es una aproximación de una función en un punto $x_0$ mediante un polinomio de Taylor de grado $n$.

Dada una función $f(x)$, $n$ veces derivable, y un punto $x_0$, el polinomio interpolador de Taylor de grado $n$ es:

$$
P_n(x) = f(x_0) + f'(x_0)(x-x_0) + \frac{f''(x_0)}{2!}(x-x_0)^2 + \ldots + \frac{f^{(n)}(x_0)}{n!}(x-x_0)^n
$$
