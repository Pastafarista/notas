---
id: 1716907553-ejercicio-9-tema-4-ecuaciones-diferenciales
aliases:
  - Ejercicio 9 tema 4 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve el siguiente sistema de ecuaciones diferenciales:

$$
\begin{cases}
    x' = x + 2y\\
    y' = -2x + 5y
\end{cases}
$$

Sacamos la matriz de coeficientes:

$$
A = \begin{pmatrix}
    1 & 2\\
    -2 & 5
\end{pmatrix}
$$

Calculamos los autovalores asociados a la matriz de coeficientes:

$$
\begin{split}
    & det(A-\lambda I) = 0 \Longleftrightarrow \\
    & \Longleftrightarrow det\left(\begin{pmatrix}
        1-\lambda & 2\\
        -2 & 5-\lambda
    \end{pmatrix}\right) = 0 \Longleftrightarrow \\
    & \implies \lambda_{1} = 3 \text{ (doble)}
\end{split}
$$

Calculamos los autovectores asociados a los autovalores:

- Para $\lambda_{1} = 3$:

$$
\begin{split}
    & S_{\lambda = 3} = \left( \begin{array}{cc|c}
        1-3 & 2 & 0\\
        -2 & 5-3 & 0
    \end{array}\right) \sim
    \left( \begin{array}{cc|c}
        -2 & 2 & 0\\
        0 & 0 & 0
    \end{array}\right) = \{(x, x) : x \in \mathbb{R} \}
\end{split}
$$

Como vemos, la matriz no es diagonalizable, por lo tanto calcularemos el bloque de Jordan asociado a $\lambda_{1} = 3$:

$$
\begin{split}
    & E_{1}(\lambda = 3) = \{(x, x) : x \in \mathbb{R}\}
    & E_{2}(\lambda = 3) = Ker(A - 3I)^2 = Ker \begin{pmatrix}
        -2 & 2\\
        -2 & 2
    \end{pmatrix}^2 = Ker \begin{pmatrix}
        0 & 0\\
        0 & 0
    \end{pmatrix} = \{(x, y) : x,y \in \mathbb{R}\}
\end{split}
$$

Nuestro vector $v_{2}$ será un vector que pertenezca a $E_{2}(\lambda = 3)$ pero que no pertenezca a $E_{1}(\lambda = 3)$, por lo que tomamos $v_{2}=(1,0)$. Para encontrar $v_{1}$, tomamos $v_{1}=(A-3I)v_{2} = (-2,-2)$.

Por lo tanto, la solución general del sistema de ecuaciones diferenciales es:

$$
\begin{split}
    & Y_{SGEH} = C_{1}v_{1}e^{3t} + C_{2}(tv_{1} + v_{2})e^{3t} =\\
    & = C_{1}\begin{pmatrix}
        -2\\
        -2
    \end{pmatrix}e^{3t} + C_{2}\left(t\begin{pmatrix}
        -2\\
        -2
    \end{pmatrix} + \begin{pmatrix}
        1\\
        0
    \end{pmatrix}\right)e^{3t}\\
\end{split}
$$

En forma de sistema de ecuaciones, la solución general es:

$$
\begin{cases}
    x(t) = -2C_{1}e^{3t} + C_{2}(-2t+1)e^{3t}\\
    y(t) = -2C_{1}e^{3t} + C_{2}(-2t)e^{3t}
\end{cases}
$$
