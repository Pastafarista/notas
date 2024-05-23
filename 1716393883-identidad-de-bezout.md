---
id: 1716393883-identidad-de-bezout
aliases:
  - Identidad de Bezout
tags:
  - matemática-discreta-II
---

# Identidad de Bezout

## Enunciado

Sean $a,b \in \mathbb{Z}$, si $mcd(a,b) = 1$ entonces $\exists x,y: \quad ax + by = 1$

## Demostración

Si $a = bk + r$. Demostraremos que hay una solución para $rx + by =1$:

- $ax + by = (kb + r)x + by = rx + b(kx + y) = rx + by'$, donde $y' = kx + y$

Entonces, si aplicamos el [[1716392171-teorema-de-euclides|algoritmo de Euclides]] hasta que el resto sea 1:

$$
r_nx_n + 1y_n = 1
$$

Esta ecuación tiene solución $x_n = 1$ y $y_n = 1 - r_n$.
