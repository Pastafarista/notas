---
id: 1713170007-teorema-caracterizacin-polinomio-de-taylor
aliases:
  - Teorema caracterización polinomio de Taylor
tags:
  - cálculo-numérico
---

# Teorema caracterización polinomio de Taylor

## Enunciado

Para $N \ge 1$, sea $f$ una función $N$ veces derivable en $x_{0}$. Su polinomio de Taylor de orden $N$ en $x_{0}$ verifica:

$$
f - P = o((x - x_{0})^{N}), \; x \to x_{0}
$$

Además, $P$ es el único polinomio de grado $\le N$ con esta propiedad, y por ello caracteriza al polinomio de Taylor entre todos los de grado $\le N$.

## Demostración

Tenemos que probar que $f-p$ es [[1713169805-notaciones-de-landau|o pequeña]] de $(x - x_{0})^{N}$:

$$
\lim_{x \to x_{0}} \frac{f(x) - P(x)}{(x - x_{0})^{N}} = 0
$$

Si hacemos el limite vemos que tenemos una indeterminación de la forma $\left\{\frac{0}{0}\right\}$, por lo que podemos aplicar la regla de L'Hôpital

$$
\begin{split}
    & \lim_{x \to x_{0}} \frac{f(x) - P(x)}{(x - x_{0})^{N}} = \lim_{x \to x_{0}} \frac{f'(x) - P'(x)}{N(x - x_{0})^{N-1}} = \ldots =\\
    & = \lim_{x \to x_{0}} \frac{f^{(N - 1)}(x) - P^{(N - 1)}(x)}{N!(x - x_{0})} = 0 \iff\\
    &  \lim_{x \to x_{0}} \frac{f^{(N - 1)}(x) - \left(f^{N}(x_0)\frac{N!(x-x_{0}) }{N!} + f^{N-1}(x_0)\frac{(N-1)!}{(N-1)!} \right) }{N!(x - x_{0})}  = \\
    & \frac{1}{N!}\lim_{x \to x_{0}} \frac{f^{(N - 1)}(x) - f^{N}(x_0)(x - x_{0}) - f^{N-1}(x_0) }{x - x_{0}} =\\
    & = \frac{1}{N!}\left( \lim_{x \to x_0} \frac{f^{(N-1)}(x)-f^{(N-1)}(x_0)}{x-x_0} - \lim_{x \to x_0}\frac{f^N(x_0)(x-x_0)}{x-x_0}\right) =\\
    & = \frac{1}{N!}(f^N(x_0)-f^N(x_0))=\frac{1}{N!}\cdot0 = 0
\end{split}
$$

Ahora tenemos que demostrar su unicidad. Supongamos por reducción al absurdo que existen dos polinomios $P$ y $Q$ de grado $\le N$ que cumplen la propiedad, con $P \neq Q$.

Entonces, $P - Q$ es un polinomio de grado $\le N$ que cumple la propiedad, es decir, $f - (P - Q) = o((x - x_{0})^{N})$.

Si $P - Q \neq 0$, entonces existirá un $m$ tal que $a_m$ es el primer coeficiente no nulo de $P - Q$.

$$
\begin{split}
    & m = min\{ k \in \{1,\ldots, n\}: a_k \neq 0 \}\\
    & \lim_{x \to x_{0}} \frac{f(x) - (P(x) - Q(x))}{(x - x_{0})^{m}} = \lim_{x \to x_{0}} \frac{\sum_{i=0}^{m}a_i(x-x_{0})^i}{(x - x_{0})^m} =\\
    & = \lim_{x \to x_{0}} \frac{\sum_{i = m}^{n}a_i(x - x_{0})^i}{(x - x_{0})^m} =\\
    & = \lim_{x \to x_{0}} \frac{a_m(x - x_{0})^m + \sum_{i = m + 1}^{n}a_i(x - x_{0})^i}{(x - x_{0})^m} = a_m + 0 + \ldots + 0 = a_m\\
\end{split}
$$

Ahora veremos que si $P$ y $Q$ son [[1713169805-notaciones-de-landau|o pequeña]], entonces $P - Q$ también lo será:

$$
\begin{split}
    & \lim_{x \to x_{0}} \frac{P(x) - Q(x)}{(x - x_{0})^N} = \lim_{x \to x_{0}} \frac{P(x) - Q(x) + f(x) - f(x)}{(x - x_{0})^{N}} =\\
    & \lim_{x \to x_{0}} \frac{f(x) - Q(x)}{(x - x_{0})^{N}} - \lim_{x \to x_{0}} \frac{f(x) - P(x)}{(x - x_{0})^{N}} =\\
    & = 0 + 0 = 0
\end{split}
$$

Por lo que si $P - Q$ es o pequeña:

$$
a_m = \lim_{x \to x_{0}}\frac{P(x) - Q(x)}{(x - x_{0})^{m}} = \lim_{x \to x_{0}}\frac{P(x) - Q(x)}{(x - x_{0})^{m}}(x - x_{0})^{N - m} = 0 \cdot0=0
$$

Pero hemos dicho que $a_m \neq 0$, contradicción. 
