---
id: 1716913379-ejercicio-13-tema-4-ecuaciones-diferenciales
aliases:
  - Ejercicio 13 tema 4 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve el siguiente sistema de ecuaciones diferenciales:

$$
Y' = \begin{pmatrix}
    2 & -6 & 3\\
    2 & -5 & 2\\
    1 & -2 & 0
\end{pmatrix}Y
$$

Sacamos los autovalores de la matriz de coeficientes:

$$
\begin{split}
    & \det(A - \lambda I) = 0\\
    & \det\left(\begin{pmatrix}
        2-\lambda & -6 & 3\\
        2 & -5-\lambda & 2\\
        1 & -2 & -\lambda
    \end{pmatrix}\right) = 0\\
    & \lambda_1 = -1 \text{ (trible)}
\end{split}
$$

Calculamos los autovectores asociados a cada autovalor:

- Para $\lambda_1 = -1$:

$$
\begin{split}
    & S_{\lambda = -1} = \left(\begin{array}{ccc|c}
        2+1 & -6 & 3 & 0\\
        2 & -5+1 & 2 & 0\\
        1 & -2 & 1 & 0
    \end{array}\right) \sim
    \left(\begin{array}{ccc|c}
        3 & -6 & 3 & 0\\
        2 & -4 & 2 & 0\\
        1 & -2 & 1 & 0
    \end{array}\right) \sim
    \left(\begin{array}{ccc|c}
        1 & -2 & 1 & 0\\
        0 & 0 & 0 & 0\\
        0 & 0 & 0 & 0
    \end{array}\right) = \{(2y - z, y, z):y,z \in \mathbb{R}\}
\end{split}
$$

Como vemos, la matriz no es diagonalizable, por lo que calcularemos la [[1716897460-matriz-de-jordan|forma canónica de Jordan]]. Para ello, calculamos los autovectores generalizados asociados a cada autovalor:

- Para $\lambda_1 = -1$:

$$
\begin{split}
    & E_{1}(\lambda = -1) = \{(2y - z, y, z):y,z \in \mathbb{R}\}\\
    & E_{2}(\lambda = -1) = ker(A + I)^2 = ker\left(\begin{pmatrix}
        3 & -6 & 3\\
        2 & -4 & 2\\
        1 & -2 & 1
    \end{pmatrix}^2\right) = ker\left(\begin{pmatrix}
        0 & 0 & 0\\
        0 & 0 & 0\\
        0 & 0 & 0
    \end{pmatrix}\right) = \{(x,y,z):x,y,z \in \mathbb{R}\}
\end{split}
$$

| $E_{1}(\lambda = -1)$ | $E_{2}(\lambda = -1)$ |
| -------------- | --------------- |
| $v_{1}$ | $v_{2}$ |
| $v_{3}$ |  |

El vector $v_{2}$ es un vector que pertenezca a $E_2(\lambda = -1)$ pero que no pertenezca a $E_1(\lambda = -1)$, por lo que podemos tomar $v_2 = (1,0,0)$.

El vector $v_{1}$ será igual a $v_{1}=(A + I)v_{2} = (3,2,1)$.
El vector $v_{3}$ es un vector que pertenece a $E_{1}(\lambda = -1)$ y que sea linealmente independiente de $v_{1}$, por lo que podemos tomar $v_3 = (1,0,-1)$.

Por lo tanto, la solución general del sistema de ecuaciones diferenciales es:

$$
\begin{split}
    & Y_{SGEH} = C_{1}v_{1}e^{-t} + C_{2}(tv_{1} + v_{2})e^{-t} + C_{3}v_{3}e^{-t} =\\
    & = C_{1}\begin{pmatrix}
        3\\
        2\\
        1
    \end{pmatrix}e^{-t} + C_{2}\left(t\begin{pmatrix}
        3\\
        2\\
        1
    \end{pmatrix} + \begin{pmatrix}
        1\\
        0\\
        0
    \end{pmatrix}\right)e^{-t} + C_{3}\begin{pmatrix}
        1\\
        0\\
        -1
    \end{pmatrix}e^{-t}
\end{split}
$$

En forma de sistema de ecuaciones:

$$
Y_{SGEH} = \begin{cases}
    y_{1}(t) = 3C_{1}e^{-t} + C_{2}e^{-t}(3t + 1) + C_{3}e^{-t}\\
    y_{2}(t) = 2C_{1}e^{-t} + 2C_{2}te^{-t}\\
    y_{3}(t) = C_{1}e^{-t} + C_{2}te^{-t} - C_{3}e^{-t}
\end{cases}
$$
