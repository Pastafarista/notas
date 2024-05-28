---
id: 1716912108-ejercicio-11-tema-4-ecuaciones-diferenciales
aliases:
  - Ejercicio 11 tema 4 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve el siguiente sistema de ecuaciones diferenciales:

$$
\begin{cases}
    y_{1}' = y_{1} - y_{3}
    y_{2}' = 4y_{1} - 3y_{3}
    y_{3}' = 2y_{1} - 2y_{3}
\end{cases}
$$

Calculamos la matriz de coeficientes:

$$
A = \begin{pmatrix}
    1 & 0 & -1\\
    4 & 0 & -3\\
    2 & 0 & -2
\end{pmatrix}
$$

Calculamos los autovalores de la matriz de coeficientes:

$$
\begin{split}
    & \det(A - \lambda I) = 0\\
    & \begin{vmatrix}
        1-\lambda & 0 & -1\\
        4 & -\lambda & -3\\
        2 & 0 & -2-\lambda
    \end{vmatrix} = 0\\
    & \lambda_1 = 0 \text{ (doble)} \quad \lambda_2 = -1
\end{split}
$$

Calculamos los autovectores asociados a cada autovalor:

- Para $\lambda_1 = 0$:

$$
\begin{split}
    & S_{\lambda = 0} = \left(\begin{array}{ccc|c}
        1 & 0 & -1 & 0\\
        4 & 0 & -3 & 0\\
        2 & 0 & -2 & 0
    \end{array}\right) \sim
    \left(\begin{array}{ccc|c}
        1 & 0 & -1 & 0\\
        0 & 0 & 1 & 0\\
        0 & 0 & 0 & 0
    \end{array}\right) = \{(0, x, 0): x\in \mathbb{R}\} \implies\\
    & B_{S_{\lambda = 0}} = \left\{\begin{pmatrix}
        0\\
        1\\
        0
    \end{pmatrix}\right\}
\end{split}
$$

- Para $\lambda_2 = -1$:

$$
\begin{split}
    & S_{\lambda = -1} = \left(\begin{array}{ccc|c}
        1-(-1) & 0 & -1 & 0\\
        4 & -(-1) & -3 & 0\\
        2 & 0 & -2-(-1) & 0
    \end{array}\right) \sim
    \left(\begin{array}{ccc|c}
        2 & 0 & -1 & 0\\
        4 & 1 & -3 & 0\\
        2 & 0 & -1 & 0
    \end{array}\right) \sim
    \left(\begin{array}{ccc|c}
        2 & 0 & -1 & 0\\
        0 & 1 & -1 & 0\\
        0 & 0 & 0 & 0
    \end{array}\right) = \{(x, 2x, 2x): x\in \mathbb{R}\} \implies\\
\end{split}
$$

Ya vemos que no es diagonalizable, por lo que calcularemos la [[1716897460-matriz-de-jordan|forma canónica de Jordan]]. Para ello, calculamos los autovectores generalizados asociados a $\lambda_{1}=0$:

$$
\begin{split}
    & E_{1}(\lambda = 0) = \{(0, x, 0): x\in \mathbb{R}\}\\
    & E_{2}(\lambda = 0) = ker(A)^2 = ker\left(\begin{pmatrix}
        1 & 0 & -1\\
        4 & 0 & -3\\
        2 & 0 & -2
    \end{pmatrix}^2\right) = ker\left(\begin{pmatrix}
        -1 & 0 & 1\\
        -2 & 0 & 2\\
        -2 & 0 & 2
    \end{pmatrix}\right) = \{(x, y, x): x, y \in \mathbb{R}\}
\end{split}
$$

El vector $v_{2}$ será un vector que pertenezca a $E_2(\lambda = 0)$ pero que no pertenezca a $E_1(\lambda = 0)$, por lo que podemos tomar $v_2 = (1, 0, 1)$. 

El vector $v_{1}$ será igual a $v_{1}=(A - 0I)v_{2} = (0, 1, 0)$.

Por lo tanto, la solución general del sistema de ecuaciones diferenciales es:

$$
\begin{split}
    & Y_{SGEH} = C_{1}\begin{pmatrix}
        1\\
        2\\
        2
    \end{pmatrix}e^{-t} + C_{2}\begin{pmatrix}
        0\\
        1\\
        0
    \end{pmatrix}e^{0t} 
    C_{3}\left(t\begin{pmatrix}
        0\\
        1\\
        0
    \end{pmatrix} + \begin{pmatrix}
        1\\
        0\\
        1
    \end{pmatrix}\right)e^{0}
\end{split}
$$

En forma de sistema de ecuaciones:

$$
Y_{SGEH} = \begin{cases}
    y_{1}(t) = C_{1}e^{-t} + C_{3}\\
    y_{2}(t) = 2C_{1}e^{-t} + C_{2} + C_{3}t\\
    y_{3}(t) = 2C_{1}e^{-t} + C_{3}
\end{cases}
$$
