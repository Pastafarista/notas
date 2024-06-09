---
id: 1713207677-teorema-diferencias-divididas
aliases:
  - Teorema diferencias divididas
tags:
  - cálculo-numérico
---

# Teorema diferencias divididas

## Enunciado

Si $P$ es el [[1709641715-polinomio-interpolador-de-lagrange|polinomio interpolador de Lagrange]] de grado $\le N$ que interpola a una función $f$ en $N + 1$ nodos $x_{0},\ldots,x_{N}$, entonces para cada nodo $x$ que no coincida con ningún $x_i$ y para el que la función esté definida, se tiene que:

$$
f(x) - P(x) = f[x_{0},\ldots ,x_N,x](x - x_{0}) \dots (x - x_N)
$$

## Demostración

Elijamos un valor de $x$ para el cual deseemos probar la igualdad. Consideremos el polinomio $Q$ de grado $\le N + 1$ que interpola a $f$ en los $N + 1$ nodos $x_i$ y en $x$. En este polinomio la variable será $t$ ya que $x$ es un nodo más. Entonces:

$$
Q(t) - P(t) = f[x_{0},\ldots ,x_N,x](t - x_{0}) \dots (t - x_N)(t - x)
$$

Ahora bastará con evaluar en $x$:

$$
\begin{split}
    & Q(x) - P(x) = f[x_{0},\ldots ,x_N,x](x - x_{0}) \dots (x - x_N)(x - x)
\end{split}
$$

