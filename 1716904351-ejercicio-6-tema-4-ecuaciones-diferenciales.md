---
id: 1716904351-ejercicio-6-tema-4-ecuaciones-diferenciales
aliases:
  - Ejercicio 6 tema 4 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve el siguiente sistema de ecuaciones diferenciales:

$$
\begin{cases}
    x' = x - 2y + 2z\\
    y' = -2x + y -2z\\
    z' = 2x - 2y + z
\end{cases}
$$

Sacamos la matriz de coeficientes:

$$
A = \begin{pmatrix}
    1 & -2 & 2\\
    -2 & 1 & -2\\
    2 & -2 & 1
\end{pmatrix}
$$

Calculamos los autovalores asociados a la matriz de coeficientes:

$$
\begin{split}
    & det(A-\lambda I) = 0 \Longleftrightarrow \\
    & \Longleftrightarrow det\left(\begin{pmatrix}
        1-\lambda & -2 & 2\\
        -2 & 1-\lambda & -2\\
        2 & -2 & 1-\lambda
    \end{pmatrix}\right) = 0 \Longleftrightarrow \\
    & \implies \lambda_{1} = -1 \; \text{(doble)} \quad \lambda_{2} = 5
\end{split}
$$

Calculamos los autovectores asociados a los autovalores:

- Para $\lambda_{1} = -1$:

$$
\begin{split}
    & S_{\lambda = -1} = \left( \begin{array}{ccc|c}
        1 - (-1) & -2 & 2 & 0\\
        -2 & 1 - (-1) & -2 & 0\\
        2 & -2 & 1 - (-1) & 0
    \end{array}\right) \sim 
    \left( \begin{array}{ccc|c}
        1 & -1 & 1 & 0\\
        0 & 0 & 0 & 0\\
        0 & 0 & 0 & 0
    \end{array}\right) = \{(x, x+z, z) : x,z \in \mathbb{R} \} \implies\\
    & B_{S_{\lambda = -1}} = \left\{ \begin{pmatrix}
        1\\
        1\\
        0
    \end{pmatrix}, \begin{pmatrix}
        0\\
        1\\
        1
    \end{pmatrix} \right\}
\end{split}
$$

- Para $\lambda_{2} = 5$:

$$
\begin{split}
    & S_{\lambda = 5} = \left( \begin{array}{ccc|c}
        1 - 5 & -2 & 2 & 0\\
        -2 & 1 - 5 & -2 & 0\\
        2 & -2 & 1 - 5 & 0
    \end{array}\right) \sim
    \left( \begin{array}{ccc|c}
        1 & -1 & -2 & 0\\
        0 & -1 & -1 & 0\\
        0 & 0 & 0 & 0
    \end{array}\right) = \{(x, -x, x) : x \in \mathbb{R}\} \implies\\
    & B_{S_{\lambda = 5}} = \left\{ \begin{pmatrix}
        1\\
        -1\\
        1
    \end{pmatrix} \right\}
\end{split}
$$

Ahora que ya tenemos los autovectores podemos construir nuestra solución general:

$$
Y_{SGEH} = C_{1}e^{-t}\begin{pmatrix}
    1\\
    1\\
    0
\end{pmatrix} + C_{2}e^{-t}\begin{pmatrix}
    0\\
    1\\
    1
\end{pmatrix} + C_{3}e^{5t}\begin{pmatrix}
    1\\
    -1\\
    1
\end{pmatrix}
$$

En forma de sistema de ecuaciones:

$$
Y_{SGEH} = \begin{cases}
    x(t) = C_{1}e^{-t} + C_{3}e^{5t}\\
    y(t) = C_{1}e^{-t} + C_{2}e^{-t} - C_{3}e^{5t}\\
    z(t) = C_{2}e^{-t} + C_{3}e^{5t}
\end{cases}
$$
