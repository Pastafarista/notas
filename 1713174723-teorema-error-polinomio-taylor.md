---
id: 1713174723-teorema-error-polinomio-taylor
aliases:
  - Teorema error polinomio Taylor
tags:
  - cálculo-numérico
---

# Teorema error polinomio Taylor
 
## Enunciado

Sean $x, x_{0}$ dos número reales distintos y sea $f$ una función con $N$ derivadas [[1716491727-funcin-continua|continuas]] en el intervalo $[x, x_{0}]$, supongamos además que la derivada $f^{(N+1)}$ existe en el intervalo abierto $(x, x_{0})$. Entonces, existe un punto $c$, comprendido estrictamente entre $x$ y $x_{0}$, tal que el [[1707819341-errores|error]] del polinomio de Taylor de orden $N$ de $f(x)$ centrado en $x_0$ es:

$$
f(x) - P(x) = f^{(N+1)}(c)\frac{(x - x_{0})^{N+1}}{(N+1)!}
$$

## Demostración

Definamos la función $M(x)$ como sigue:

$$
M(x) = \frac{f(x) - P(x)}{(x - x_{0})^{N+1}}
$$

Entonces hay que demostrar que:

$$
M(N + 1)! = f^{(N+1)}(c)
$$

Construyamos la función auxiliar $F(t)$

$$
F(t) = f(t) - P(t) - M(t)(t - x_{0})^{N+1}
$$

Entonces, vemos que se cumple que $F(x) = 0$ y $F(x_{0}) = 0$:

$$
\begin{split}
    & F(x) = f(x) - P(x) - M(x - x_{0})^{N+1} =\\
    &=f(x) - P(x) - \frac{f(x) - P(x)}{(x - x_{0})^{N+1}}(x - x_{0})^{N+1} = 0\\
    & F(x_{0}) = f(x_{0}) - P(x_{0}) - M(x_{0} - x_{0})^{N+1} = f(x_{0}) - f(x_{0}) - M \cdot 0 = 0
\end{split}
$$

Ahora con el teorema de Rolle:

$$
\begin{split}
    & F(x) = F(x_{0}) = 0 \to \exists c_{1} \in (x_{0}, x) \; | \; F'(c_{1}) = 0\\
\end{split}
$$

El valor de $F'(x_{0})$ es:

$$
F'(x_{0}) = f'(x_{0}) - P'(x_{0}) - M(N+1)(x_{0} - x_{0})^{N} = f'(x_{0}) - f'(x_{0}) - M \cdot 0 = 0
$$

Por lo tanto, si seguimos desarrollando:

$$
\begin{split}
    & F(x) = F(x_{0}) = 0 \to \exists c_{1} \in (x_{0}, x) \; | \; F'(c_{1}) = 0\\
    & F'(c_{1}) = F'(x_{0}) = 0 \to \exists c_{2} \in (x_{0}, c_{1}) \; | \; F''(c_{2}) = 0\\ 
    & \ldots\\
    & F^{(N)}(c_{N}) = F^{(N)}(x_{0}) = 0 \to \exists c \in (x_{0}, c_{N}) \; | \; F^{(N+1)}(c) = 0
\end{split}
$$

Por lo tanto, como $F^{(N+1)}(c) = 0$, entonces:

$$
\begin{split}
    & F^{(N+1)}(c) = 0 = f^{(N+1)}(c) - M(N+1)! = 0 \iff M(N+1)! = f^{(N+1)}(c) \iff\\
    &  \frac{f(x) - P(x)}{(x - x_0)^{N + 1}} = f^{(N+1)}(c)\cdot \frac{1}{(N + 1)!} \iff f(x) - P(x) = f^{(N+1)}(c)\frac{(x - x_{0})^{N+1}}{(N+1)!}
\end{split}
$$

Por lo tanto, hemos demostrado que existe un punto $c$ en el intervalo $(x, x_{0})$ tal que:

$$
f(x) - P(x) = f^{(N+1)}(c)\frac{(x - x_{0})^{N+1}}{(N+1)!}
$$
