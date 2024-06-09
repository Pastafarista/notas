---
id: 1716902323-ejercicio-4-tema-4-ecuaciones-diferenciales
aliases:
  - Ejercicio 4 tema 4 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve el siguiente sistema de ecuaciones diferenciales

$$
Y' = \begin{pmatrix}
    3 & -1 & 1\\
    -1 & 5 & -1\\
    1 & -1 & 3
\end{pmatrix}Y
$$

Sacamos los autovalores de la matriz $A$:

$$
\begin{split}
    & \det(A - \lambda I) = 0 \iff\\
    & \iff \begin{vmatrix}
        3 - \lambda & -1 & 1\\
        -1 & 5 - \lambda & -1\\
        1 & -1 & 3 - \lambda
    \end{vmatrix} \implies\\
    & \implies \lambda_1 = 2, \quad \lambda_2 = 3, \quad \lambda_3 = 6
\end{split}
$$

Sacamos los autovectores de la matriz $A$:

- Para $\lambda_1 = 2$:

$$
\begin{split}
    & S_{\lambda = 2} = \left( \begin{array}{ccc|c}
        3-2 & -1 & 1 & 0\\
        -1 & 5-2 & -1 & 0\\
        1 & -1 & 3-2 & 0
    \end{array}\right) \sim \left( \begin{array}{ccc|c}
        1 & -1 & 1 & 0\\
        0 & 2 & 0 & 0\\
        0 & 0 & 0 & 0
    \end{array}\right) = \{(x,0,-x) : x \in  \mathbb{R}\} \implies\\
    & \implies B_{S_{\lambda = 2}} = \begin{pmatrix}
        1\\
        0\\
        -1
    \end{pmatrix}
\end{split}
$$

- Para $\lambda_2 = 3$:

$$
\begin{split}
    & S_{\lambda = 3} = \left( \begin{array}{ccc|c}
        3-3 & -1 & 1 & 0\\
        -1 & 5-3 & -1 & 0\\
        1 & -1 & 3-3 & 0
    \end{array}\right) \sim \left( \begin{array}{ccc|c}
        1 & -1 & 0 & 0\\
        0 & 1 & -1 & 0\\
        0 & 0 & 0 & 0
    \end{array}\right) = \{(x,x,x) : x \in  \mathbb{R}\} \implies\\
    & \implies B_{S_{\lambda = 3}} = \begin{pmatrix}
        1\\
        1\\
        1
    \end{pmatrix}
\end{split}
$$

- Para $\lambda_3 = 6$:

$$
\begin{split}
    & S_{\lambda = 6} = \left( \begin{array}{ccc|c}
        3-6 & -1 & 1 & 0\\
        -1 & 5-6 & -1 & 0\\
        1 & -1 & 3-6 & 0
    \end{array}\right) \sim \left( \begin{array}{ccc|c}
        -3 & -1 & 1 & 0\\
        -1 & -1 & -1 & 0\\
        1 & -1 & -3 & 0
    \end{array}\right) \sim \{(x,-2x,x) : x \in  \mathbb{R}\} \implies\\
    & \implies B_{S_{\lambda = 6}} = \begin{pmatrix}
        1\\
        -2\\
        1
    \end{pmatrix}
\end{split}
$$

Con esto ya podemos construir la solución general $Y$:

$$
Y_{SGEH} = C_{1}e^{2x}\begin{pmatrix}
    1\\
    0\\
    -1
\end{pmatrix} + C_{2}e^{3x}\begin{pmatrix}
    1\\
    1\\
    1
\end{pmatrix} + C_{3}e^{6x}\begin{pmatrix}
    1\\
    -2\\
    1
\end{pmatrix}
$$

En forma de sistema de ecuaciones:

$$
Y_{SGEH} = \begin{cases}
    y_{1} = C_{1}e^{2x} + C_{2}e^{3x} + C_{3}e^{6x}\\
    y_{2} = C_{2}e^{3x} - 2C_{3}e^{6x}\\
    y_{3} = -C_{1}e^{2x} + C_{2}e^{3x} + C_{3}e^{6x}
\end{cases}
$$
