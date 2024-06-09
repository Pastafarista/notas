---
id: 1713211949-error-polinomio-de-lagrange-a-trozos
aliases:
  - Error polinomio de Lagrange a trozos
tags:
  - cálculo-numérico
---

# Error polinomio de Lagrange a trozos

## Enunciado

Para $x\in [x_{i -1}, x_i]$, la función $S$ coincide con el [[1709641715-polinomio-interpolador-de-lagrange|polinomio interpolador de Lagrange]] de grado $\le 1$ que interpola a $f$ en $x_{i-1}$ y $x_{i}$. Por eso, si $f$ tiene derivada segunda en $[a,b]$ acotada en valor absoluto $K_{2}$,

$$
|f(x) - S(x)| \le \frac{(x_{i} - x_{i-1})^2}{8}K_{2}, \quad x\in [x_{i-1}, x_{i}]
$$

## Demostración

Si denotamos por $h$ a la mayor de las cantidades $x_{i} - x_{i-1}, i = 1, \ldots, N$, entonces:

$$
|f(x) - S(x)| \le \frac{h^2}{8}K_{2}, \quad x\in [a,b]
$$

![[Pasted image 20240415223035.png]]