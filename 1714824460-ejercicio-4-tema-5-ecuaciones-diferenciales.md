---
id: 1714824460-ejercicio-4-tema-5-ecuaciones-diferenciales
aliases:
  - Ejercicio 4 tema 5 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Determina los [[1714749330-punto-crtico-de-un-sistema-autnomo|puntos críticos]] del siguiente sistema y analiza su estabilidad o inestabilidad:

$$
\begin{cases}
    & x' = x\\
    & y' = 4y
\end{cases}
$$

Autovalores:

$$
\begin{split}
    & A = \begin{pmatrix}
        1 & 0\\
        0 & 4
    \end{pmatrix}\\
    & \text{det}(A - \lambda I) = 0\\
    & \text{det}\begin{pmatrix}
        1 - \lambda & 0\\
        0 & 4 - \lambda
    \end{pmatrix} = 0\\
    & (1 - \lambda)(4 - \lambda) = 0\\
    \begin{cases}
        & \lambda = 1\\
        & \lambda = 4
    \end{cases}\\
\end{split}
$$

Se trata de un nodo inestable, ya que ambos autovalores son positivos.

Autovalores asociados a $\lambda = 1$:

$$
\begin{split}
    & \array{cc|c}
        & 1 - 1 & 0 & 0\\
        & 0 & 4 - 1 & 0\\
    \end{array} \implies 
    B_{S_{\lambda = 1}} = \{(1,0)\}
\end{split}
$$

Autovalores asociados a $\lambda = 4$:

$$
\begin{split}
    & \array{cc|c}
        & 1 - 4 & 0 & 0\\
        & 0 & 4 - 4 & 0\\
    \end{array} \implies 
    B_{S_{\lambda = 4}} = \{(0,1)\}
\end{split}
$$

Entonces:

$$
\begin{split}
    & \binom{x}{y} = C_1\binom{1}{0}e^t + C_2\binom{0}{1}e^{4t} \implies\\
    & \implies \begin{cases}
        & x(t) = C_1e^t\\
        & y(t) = C_2e^{4t}
    \end{cases}\\
    t \to \infty \implies (x,y) \to (\infty, \infty)
\end{split}
$$

La ecuación sería:

$$
\begin{split}
    & \frac{dy}{dx} = \frac{4y}{x} \implies \frac{1}{y}dy = \frac{4}{x}dx \implies\\
    & \implies \ln|y| = 4\ln|x| + C \implies y = Cx^4
\end{split}
$$
