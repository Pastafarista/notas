---
id: 1713201633-teorema-error-polinomio-lagrange
aliases:
  - Teorema error polinomio Lagrange
tags:
  - cálculo-numérico
---

# Teorema error polinomio Lagrange

## Enunciado

Supongamos que $f$ es una función con $N\ge 1$ derivadas [[1716491727-funcin-continua|continuas]] en un intervalo $[a,b]$ y tal que $f^{(N+1)}$ existe en $(a,b)$. Sean $x_{0},\ldots ,x_{N}$, $N + 1$ nodos en $[a,b]$, dos a dos distintos, y sea $P$ el correspondiente [[1709641715-polinomio-interpolador-de-lagrange|polinomio interpolador de Lagrange]]. Entonces a cada punto $x$ en $[a,b]$ le corresponde un punto $c$ con ${min(x_{0},\ldots ,x_N,x)}$ < c < ${max(x_{0},\ldots ,x_N,x)}$ tal que:

$$
f(x) - P(x) = \frac{(x - x_{0}) \dots (x - x_N)}{(N + 1)!}f^{(N+1)}(c)
$$

## Demostración

Elijamos un $x \in [a,b]$, si $x \in \{x_{0},\ldots,x_N\}$, entonces el error será nulo y la igualdad se cumplirá. Si $x \notin \{x_{0},\ldots,x_N\}$, entonces definimos:

$$
M = \frac{f(x) - P(x)}{(x - x_{0}) \dots (x - x_N)}
$$

Con lo que hay que probar que existe $c$ en el intervalo ya enunciado tal que $f^{(N+1)}(c) = M(N + 1)!$. Definimos:

$$
F(t) = f(t) - P(t) - M(t - x_{0}) \dots (t - x_N)
$$

Entonces si $t = x$:

$$
\begin{split}
    & F(x) = f(x) - P(x) - M(x - x_{0}) \dots (x - x_N) =\\
    & = f(x) - P(x) - (f(x) + P(x)) = 0
\end{split}
$$

$F$ también se anula en $x_{0},\ldots,x_N$, entonces $F$ tiene $N + 2$ raíces distintas en $[a,b]$.

Por el teorema de Rolle, $F'(t)$ tiene $N + 1$ raíces distintas en $[a,b]$, ya que entre dos raíces de $F$ hay una raíz de $F'$.

Si seguimos este razonamiento, llegamos a que $F^{(N+1)}(t)$ tiene una raíz en $(a,b)$, es decir, existe $c$ tal que $F^{(N+1)}(c) = 0$.

Entonces:

$$
\begin{split}
    & F^{(N+1)}(t) = f^{(N+1)}(t) - M(N + 1)! = 0\\
    & f^{(N+1)}(t) = M(N + 1)!\\
    & f^{(N+1)}(c) = \frac{f(x) - P(x)}{(x - x_{0}) \dots (x - x_N)}(N + 1)! \iff\\
    & f(x) - P(x) = \frac{(x - x_{0}) \dots (x - x_N)}{(N + 1)!}f^{(N+1)}(c)
\end{split}
$$

Por lo tanto, hemos demostrado el teorema.