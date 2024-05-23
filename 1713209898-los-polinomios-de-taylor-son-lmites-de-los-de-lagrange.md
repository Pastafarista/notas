---
id: 1713209898-los-polinomios-de-taylor-son-lmites-de-los-de-lagrange
aliases:
  - Los polinomios de Taylor son límites de los de Lagrange
tags:
  - cálculo-numérico
---

# Los polinomios de Taylor son límites de los de Lagrange

## Enunciado

Sea $f$ una función con $N$ derivadas [[1716491727-funcin-continua|continuas]] en un intervalo y $P$ el [[1709641715-polinomio-interpolador-de-lagrange|polinomio interpolador de Lagrange]] en $N+1$ nodos $x_{0}, \ldots , x_{N}$, dos a dos distintos, del intervalo. Por otro lado sea $Q(x)$ el polinomio de Taylor de grado $\le N$ de $f$ en $x_{0}$. Entonces, si se fijan $x_{0}$ y $x$, mientras que $x_{1} \to x_{0}, \ldots, x_N \to x_{0}$, se verifica que:

$$
P(x) \to Q(x)
$$

## Demostración

Basta con escribir $P(x)$ en la forma de Newton y aplicar [[1713209182-teorema-diferencia-divididas-derivadas|el colorario anterior]]: Los coeficientes $f[x_{0},\ldots ,x_i]$ de la forma de Newton tienden a los $\frac{f^{(i)}x_{0}}{i!}$ del polinomio de Taylor, mientras que ${(x - x_0)\dots(x - x_n) \to (x - x_{0})^{i}}$

$$
\begin{split}
    & Q(x) = f[x_{0}] + f[x_{0},x_{1}](x - x_{0}) + \ldots + f[x_{0},\ldots ,x_{N}](x - x_{0})\dots(x - x_{N}) =\\
    & = f(x_{0}) + f'(c)(x - x_{0}) + \ldots + \frac{f^{(N)}(c)}{N!}(x - x_{0})(x - x_{1})\dots(x - x_{N})
\end{split}
$$

Si $x_{1} \to x_{0}, \ldots, x_N \to x_{0}$, entonces $(x-x_{0})(x-x_{1}) \dots (x - x_N)$ tiende a $(x - x_{0})^{N}$, y $c$ tenderá a $x_0$ ya que $\min\{x_0,\dots,x_N\} < c < \max\{x_0, \dots, x_N\}$

