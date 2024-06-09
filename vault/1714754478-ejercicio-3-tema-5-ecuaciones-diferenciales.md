---
id: 1714754478-ejercicio-3-tema-5-ecuaciones-diferenciales
aliases:
  - Ejercicio 3 tema 5 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Determina los [[1714749330-punto-crtico-de-un-sistema-autnomo|puntos críticos]] del siguiente sistema y analiza su estabilidad o inestabilidad

$$
\begin{cases}
    & x' = -x \\
    & y' = -4y
\end{cases}
$$

El único punto crítico es $(0,0)$.

Para analizar su estabilidad, se calculan los autovalores de la [[1709025451-expresin-matricial-de-un-sistema-de-ecuaciones|matriz asociada]] al [[1714749015-sistema-de-ecuaciones-difereciales-autnomo|sistema autónomo]].

$$
\begin{split}
    & A = \begin{pmatrix}
        -1 & 0 \\
        0 & -4
    \end{pmatrix} \\
    & \det(A - \lambda I) = \begin{vmatrix}
        -1 - \lambda & 0 \\
        0 & -4 - \lambda
    \end{vmatrix} = (-1 - \lambda)(-4 - \lambda)\\
    & \det(A - \lambda I) = 0 \implies \lambda_{1} = -1, \lambda_{2} = -4
\end{split}
$$

Como los dos autovalores son negativos, el sistema es asintóticamente estable. Ademas como son distintos, se trata de un nodo estable.

Ahora, saquemos los autovectores:

- Para $\lambda = -1$:

$$
\begin{split}
    & (A - (-1)I)\cdot X = 0 \implies \begin{array}{cc|c}
        0 & 0 & 0 \\
        0 & -3 & 0
    \end{array} \implies B_{S_{\lambda=-1}} = \{(1,0)\}
\end{split}
$$

- Para $\lambda = -4$:

$$
\begin{split}
    & (A - (-4)I)\cdot X = 0 \implies \begin{array}{cc|c}
        3 & 0 & 0 \\
        0 & 0 & 0
    \end{array} \implies B_{S_{\lambda=-4}} = \{(0,1)\}
\end{split}
$$

Con todo esto:

$$
\begin{split}
    & \binom{x}{y} = C_1\binom{1}{0}e^{-t} + C_2\binom{0}{1}e^{-4t} \implies\\
    & \implies \begin{cases}
        & x(t) = C_1e^{-t} \\
        & y(t) = C_2e^{-4t}
    \end{cases}\\
    & t \to \infty \implies (x,y) \to (0,0)
\end{split}
$$

La ecuación final será:

$$
\begin{split}
    & \frac{dy}{dx} = -\frac{4y}{-x} \implies \frac{1}{y}dy = 4\frac{1}{x}dx \implies\\
    & \implies \ln|y| = 4\ln|x| + C \implies y = Cx^4
\end{split}
$$
