---
id: 1713209182-teorema-diferencia-divididas-derivadas
aliases:
  - Teorema diferencia divididas derivadas
tags:
  - cálculo-numérico
---

# Teorema diferencia divididas derivadas

## Enunciado

Si $N$ es un entero no negativo, sean $x_{0}, \ldots , x_{N+1}$, $N+ 2$ puntos, dos a dos distintos del intervalo $[a,b]$. Si $f$ es una función con $N$ derivadas [[1716491727-funcin-continua|continuas]] en $[a,b]$ y $f^{(N+1)}$ existe en $(a,b)$, entonces hay un punto $c$ con ${min(x_{0},\ldots ,x_{N+1})} < c < {max(x_{0},\ldots ,x_{N+1})}$ tal que:

$$
f[x_{0}, \ldots , x_{N+1}] = \frac{f^{(N+1)}(c)}{(N+1)!}
$$

## Demostración

Si utilizamos el [[1713174723-teorema-error-polinomio-taylor|teorema error polinomio Taylor]] y el [[1713207677-teorema-diferencias-divididas|teorema diferencias divididas]], podemos escribir:

$$
\begin{split}
    & f(x) - P(x) = \frac{(x - x_{0}) \dots (x - x_N)}{(N + 1)!}f^{(N+1)}(c)\\
    & f(x) - P(x) = f[x_{0},\ldots ,x_N,x](x - x_{0}) \dots (x - x_N)
\end{split}
$$

Entonces:

$$
\begin{split}
    & f[x_{0},\ldots ,x_N,x](x - x_{0}) \dots (x - x_N) = \frac{(x - x_{0}) \dots (x - x_N)}{(N + 1)!}f^{(N+1)}(c)\\
    & f[x_{0},\ldots ,x_N,x] = \frac{f^{(N+1)}(c)}{(N + 1)!}
\end{split}
$$
