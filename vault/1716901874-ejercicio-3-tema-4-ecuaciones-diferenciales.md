---
id: 1716901874-ejercicio-3-tema-4-ecuaciones-diferenciales
aliases:
  - Ejercicio 3 tema 4 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve el siguiente sistema de ecuaciones diferenciales:

\begin{cases}
    x' = x + y + z\\
    y' = 3y + 2z\\
    z' = 5z
\end{cases}

Sacamos la matriz de coeficientes del sistema:

$$
A = \begin{pmatrix}
    1 & 1 & 1 \\
    0 & 3 & 2 \\
    0 & 0 & 5
\end{pmatrix}
$$

Sacamos los valores propios de la matriz $A$:

$$
\begin{split}
    & \det(A - \lambda I) = 0 \iff\\
    & \iff \begin{vmatrix}
        1 - \lambda & 1 & 1 \\
        0 & 3 - \lambda & 2 \\
        0 & 0 & 5 - \lambda
    \end{vmatrix} = (1 - \lambda)(3 - \lambda)(5 - \lambda) = 0 \implies\\
    & \implies \lambda_1 = 1, \quad \lambda_2 = 3, \quad \lambda_3 = 5
\end{split}
$$

Sacamos los autovectores de la matriz $A$:

- Para $\lambda_1 = 1$:

$$
\begin{split}
    & S_{\lambda = 1} = \left( \begin{array}{ccc|c}
        1-1 & 1 & 1 & 0 \\
        0 & 3-1 & 2 & 0 \\
        0 & 0 & 5-1 & 0
    \end{array}\right) \sim \left( \begin{array}{ccc|c}
        0 & 1 & 1 & 0 \\
        0 & 2 & 2 & 0 \\
        0 & 0 & 4 & 0
    \end{array}\right) \sim \{(x, 0, 0) : x \in \mathbb{R}\} \implies\\
    & \implies B_{S_{\lambda = 1}} = \begin{pmatrix}
        1 \\
        0 \\
        0
    \end{pmatrix}
\end{split}
$$

- Para $\lambda_2 = 3$:

$$
\begin{split}
    & S_{\lambda = 3} = \left( \begin{array}{ccc|c}
        1-3 & 1 & 1 & 0 \\
        0 & 3-3 & 2 & 0 \\
        0 & 0 & 5-3 & 0
    \end{array}\right) \sim \left( \begin{array}{ccc|c}
        -2 & 1 & 1 & 0 \\
        0 & 0 & 2 & 0 \\
        0 & 0 & 2 & 0
    \end{array}\right) \sim \{(x, 2x, 0) : x \in \mathbb{R}\} \implies\\
    & \implies B_{S_{\lambda = 3}} = \begin{pmatrix}
        1 \\
        2 \\
        0
    \end{pmatrix}
\end{split}
$$

- Para $\lambda_3 = 5$:

$$
\begin{split}
    & S_{\lambda = 5} = \left( \begin{array}{ccc|c}
        1-5 & 1 & 1 & 0 \\
        0 & 3-5 & 2 & 0 \\
        0 & 0 & 5-5 & 0
    \end{array}\right) \sim \left( \begin{array}{ccc|c}
        -4 & 1 & 1 & 0 \\
        0 & -2 & 2 & 0 \\
        0 & 0 & 0 & 0
    \end{array}\right) \sim \{(x, 2x, 2x) : x \in \mathbb{R}\} \implies\\
    & \implies B_{S_{\lambda = 5}} = \begin{pmatrix}
        1 \\
        2 \\
        2
    \end{pmatrix}
\end{split}
$$

Una vez tenemos los vectores propios podemos construir nuestra solución general del sistema de ecuaciones diferenciales:

$$
Y_{SGEH} = C_{1}e^{x}\begin{pmatrix}
    1 \\
    0 \\
    0
\end{pmatrix} + C_{2}e^{3x}\begin{pmatrix}
    1 \\
    2 \\
    0
\end{pmatrix} + C_{3}e^{5x}\begin{pmatrix}
    1 \\
    2 \\
    2
\end{pmatrix}
$$

En forma de sistema de ecuaciones diferenciales, la solución general es:

$$
Y_{SGEH} = \begin{cases}
    y_{1} = C_{1}e^{x} + C_{2}e^{3x} + C_{3}e^{5x} \\
    y_{2} = 2C_{2}e^{3x} + 2C_{3}e^{5x} \\
    y_{3} = 2C_{3}e^{5x}
\end{cases}
$$

