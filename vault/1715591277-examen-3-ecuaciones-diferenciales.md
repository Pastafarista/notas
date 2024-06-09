---
id: 1715591277-examen-3-ecuaciones-diferenciales
aliases:
  - Ejercicio 1 examen 3 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Examen 3 ecuaciones diferenciales

1. Resuelve el siguiente [[1714749015-sistema-de-ecuaciones-difereciales-autnomo|sistema de ecuaciones difereciales]]:

$$
\begin{cases}
    x' = -6x - 3y + 14z \\
    y' = 4x + 3y - 8z \\
    z' = -2x - y + 5z
\end{cases}
$$

Primero sacamos los autovalores de la matriz de coeficientes:

$$
\begin{split}
    & |A-\lambda I| = \begin{vmatrix}
        -6 - \lambda & -3 & 14 \\
        4 & 3 - \lambda & -8 \\
        -2 & -1 & 5 - \lambda
    \end{vmatrix} =\\
    & = (-6-\lambda )(3 - \lambda )(5-\lambda ) + (4)(-1)(14) + (-2)(-3)(-8)-\\
     & -(14)(3-\lambda )(-2)-(-8)(-1)(4)-(5-\lambda )(-3)(4) =\\
     & = \ldots = -\lambda^3 +2 \lambda^2 + \lambda - 2 = 0 \implies \lambda = 1, -1, 2
\end{split}
$$

Autovectores asociados a $\lambda = -1$:

$$
\begin{split}
    & (A - (-1)I)X = 0 \implies\\
    & \left(\begin{array}{ccc|c}
        -5 & -3 & 14 & 0\\
        4 & 4 & -8 & 0\\
        -2 & -1 & 6 & 0
    \end{array}\right)\implies \dots \implies\\
    & \begin{cases}
        x_{1} = 4 \alpha \\
        x_{2} = -2 \alpha \\
        x_{3} = \alpha 
    \end{cases}\\
    & B_{S_{\lambda = -1}} = \{(4,-2,1)\}
\end{split}
$$


Autovectores asociados a $\lambda = 1$:

$$
\begin{split}
    & (A - 1I)X = 0 \implies\\
    & \left(\begin{array}{ccc|c}
        -7 & -3 & 14 & 0\\
        4 & 2 & -8 & 0\\
        -2 & -1 & 4 & 0
    \end{array}\right) \implies \dots \implies\\
    & \begin{cases}
        x_{1} = 2 \alpha\\ 
        x_{2} = 0\\
        x_{3} = \alpha
    \end{cases} \\
    & B_{S_{\lambda = 1}} = \{(2,0,1)\}
\end{split}
$$

Autovectores asociados a $\lambda = 2$:

$$
\begin{split}
    & (A - 2I)X = 0 \implies\\
    & \left(\begin{array}{ccc|c}
        -8 & -3 & 14 & 0\\
        4 & 4 & -8 & 0\\
        -2 & -1 & 3 & 0
    \end{array}\right) \implies \dots \implies\\
    & \begin{cases}
        x_{1} = \frac{5}{2} \alpha \\
        x_{2} = -2 \alpha \\
        x_{3} = \alpha 
    \end{cases}\\
    & B_{S_{\lambda = 2}} = \{(5,-4,2)\}
\end{split}
$$

Entonces la solución general es:

$$
\begin{split}
    & \begin{pmatrix}
        x\\
        y\\
        z
    \end{pmatrix} = C_{1}e^{-t}\begin{pmatrix}
        4\\
        -2\\
        1
    \end{pmatrix} + C_{2}e^{t}\begin{pmatrix}
        2\\
        0\\
        1
    \end{pmatrix} + C_{3}e^{2t}\begin{pmatrix}
        5\\
        -4\\
        2
    \end{pmatrix} \implies\\
    & \begin{cases}
        & x(t) = 4C_{1}e^{-t} + 2C_{2}e^{t} + 5C_{3}e^{2t}\\
        & y(t) = -2C_{1}e^{-t} + 0 + -4C_{3}e^{2t}\\
        & z(t) = C_{1}e^{-t} + C_{2}e^{t} + 2C_{3}e^{2t}
    \end{cases}
\end{split}
$$
