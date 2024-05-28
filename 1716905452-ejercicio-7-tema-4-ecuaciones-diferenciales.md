---
id: 1716905452-ejercicio-7-tema-4-ecuaciones-diferenciales
aliases:
  - Ejercicio 7 tema 4 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve el siguiente sistema de ecuaciones diferenciales:

$$
Y' = \begin{pmatrix}
    0 & 1 & 1\\
    1 & 0 & 1\\
    1 & 1 & 0
\end{pmatrix}Y
$$

Sacamos los autovalores asociados a la matriz de coeficientes:

$$
\begin{split}
    & det(A-\lambda I) = 0 \Longleftrightarrow \\
    & \Longleftrightarrow det\left(\begin{pmatrix}
        -\lambda & 1 & 1\\
        1 & -\lambda & 1\\
        1 & 1 & -\lambda
    \end{pmatrix}\right) = 0 \Longleftrightarrow \\
    & \implies \lambda_{1} = 2 \quad \lambda_{2} = -1 \text{ (doble)}
\end{split}
$$

Calculamos los autovectores asociados a los autovalores:

- Para $\lambda_{1} = 2$:

$$
\begin{split}
    & S_{\lambda = 2} = \left( \begin{array}{ccc|c}
        -2 & 1 & 1 & 0\\
        1 & -2 & 1 & 0\\
        1 & 1 & -2 & 0
    \end{array}\right) \sim
    \left( \begin{array}{ccc|c}
        1 & 1 & -2 & 0\\
        0 & -1 & 1 & 0\\
        0 & 0 & 0 & 0
    \end{array}\right) = \{(x, x, x) : x \in \mathbb{R} \} \implies\\
    & B_{S_{\lambda = 2}} = \left\{ \begin{pmatrix}
        1\\
        1\\
        1
    \end{pmatrix} \right\}
\end{split}
$$

- Para $\lambda_{2} = -1$:

$$
\begin{split}
    & S_{\lambda = -1} = \left( \begin{array}{ccc|c}
        1 & 1 & 1 & 0\\
        1 & 1 & 1 & 0\\
        1 & 1 & 1 & 0
    \end{array}\right) \sim
    \left( \begin{array}{ccc|c}
        1 & 1 & 1 & 0\\
        0 & 0 & 0 & 0\\
        0 & 0 & 0 & 0
    \end{array}\right) = \{(-y-z, y, z) : y,z \in \mathbb{R}\} \implies\\
    & B_{S_{\lambda = -1}} = \left\{ \begin{pmatrix}
        1\\
        -1\\
        0
    \end{pmatrix}, \begin{pmatrix}
        1\\
        0\\
        -1
    \end{pmatrix} \right\}
\end{split}
$$

Por lo que la solución general del sistema de ecuaciones diferenciales es:

$$
Y_{SGEH} = C_{1}e^{2t}\begin{pmatrix}
    1\\
    1\\
    1
\endpmatrix + C_{2}e^{-t}\begin{pmatrix}
    1\\
    -1\\
    0
\end{pmatrix} + C_{3}e^{-t}\begin{pmatrix}
    1\\
    0\\
    -1
\end{pmatrix}
$$

En forma de sistema de ecuaciones:

$$
Y_{SGEH} = \begin{cases}
    x(t) = C_{1}e^{2t} + C_{2}e^{-t} + C_{3}e^{-t}\\
    y(t) = C_{1}e^{2t} - C_{2}e^{-t}\\
    z(t) = C_{1}e^{2t} - C_{3}e^{-t}
\end{cases}
$$
