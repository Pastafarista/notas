---
id: 1716901123-ejercicio-2-tema-4-ecuaciones-diferenciales
aliases:
  - Ejercicio 2 tema 4 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve el siguiente sistema de ecuaciones diferenciales:

$$
\begin{cases}
    y_{1}' = 2y_{1} + 3y_{2} \\
    y_{2}' = 2y_{1} + y_{2}
\end{cases}
$$

Sacamos la matriz de coeficientes del sistema:

$$
A = \begin{pmatrix}
    2 & 3 \\
    2 & 1
\end{pmatrix}
$$

Sacamos los valores propios de la matriz $A$:

$$
\begin{split}
    & \det(A - \lambda I) = 0 \iff\\
    & \iff \begin{vmatrix}
        2 - \lambda & 3 \\
        2 & 1 - \lambda
    \end{vmatrix} = (2 - \lambda)(1 - \lambda) - 6 = 0 \implies\\
    & \implies \lambda_1 = -1, \quad \lambda_2 = 4
\end{split}
$$

Sacamos los autovectores de la matriz $A$:

Para $\lambda_1 = -1$:

$$
\begin{split}
    & S_{\lambda = 1} = \left( \begin{array}{cc|c}
        2+1 & 3 & 0 \\
        2 & 1+1 & 0
    \end{array}\right) \sim \left( \begin{array}{cc|c}
        3 & 3 & 0 \\
        2 & 2 & 0
    \end{array}\right) \sim \{(x,-x) : x \in \mathbb{R}\} \implies\\
    & B_{S_{\lambda = 1}} = \begin{pmatrix}
        1 \\
        -1
    \end{pmatrix}
\end{split}
$$

Para $\lambda_2 = 4$:

$$
\begin{split}
    & S_{\lambda = 4} = \left( \begin{array}{cc|c}
        2-4 & 3 & 0 \\
        2 & 1-4 & 0
    \end{array}\right) \sim \left( \begin{array}{cc|c}
        -2 & 3 & 0 \\
        2 & -3 & 0
    \end{array}\right) \sim \{(\frac{3}{2}x, y) : x \in \mathbb{R}\} \implies\\
    & B_{S_{\lambda = 4}} = \begin{pmatrix}
        3 \\
        2
    \end{pmatrix}
\end{split}
$$

Por lo tanto, la solución general del sistema de ecuaciones diferenciales es:

$$
Y_{SGEH} = C_{1}e^{-x}\begin{pmatrix}
    1 \\
    -1
\end{pmatrix} + C_{2}e^{4x}\begin{pmatrix}
    3 \\
    2
\end{pmatrix}
$$

En forma de sistema de ecuaciones diferenciales, la solución general es:

$$
Y_{SGEH} = \begin{cases}
    y_{1} = C_{1}e^{-x} + 3C_{2}e^{4x} \\
    y_{2} = -C_{1}e^{-x} + 2C_{2}e^{4x}
\end{cases}
$$
