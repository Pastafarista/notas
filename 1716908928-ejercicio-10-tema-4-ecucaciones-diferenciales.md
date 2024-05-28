---
id: 1716908928-ejercicio-10-tema-4-ecucaciones-diferenciales
aliases:
  - Ejercicio 10 tema 4 ecucaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve el siguiente sistema de ecuaciones diferenciales::w

$$
Y' = \begin{pmatrix}
    3 & 1\\
    -1 & 1
\end{pmatrix}Y
$$

Sacamos los autovalores de la matriz de coeficientes:

$$
\begin{split}
    & \det(A - \lambda I) = 0\\
    & \det\left(\begin{pmatrix}
        3-\lambda & 1\\
        -1 & 1-\lambda
    \end{pmatrix}\right) = 0\\
    & \lambda_2 = 2 \text{ (doble)}
\end{split}
$$

Calculamos los autovectores asociados a cada autovalor:

- Para $\lambda_1 = 2$:

$$
\begin{split}
    & S_{\lambda = 2} = \left(\begin{array}{cc|c}
        3-2 & 1 & 0\\
        -1 & 1-2 & 0
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        1 & 1 & 0\\
        0 & 0 & 0
    \end{array}\right) = \{(x,-x):x\in \mathbb{R}\} \implies\\
    & B_{S_{\lambda = 2}} = \left\{\begin{pmatrix}
        1\\
        -1
    \end{pmatrix}\right\}
\end{split}
$$

Como vemos, la matriz no es diagonalizable, por lo que calcularemos la [[1716897460-matriz-de-jordan|forma canónica de Jordan]]. Para ello, calculamos los autovectores generalizados asociados a cada autovalor:

- Para $\lambda_1 = 2$:

$$
\begin{split}
    & E_{1}(\lambda = 2) = \{(x,-x):x\in \mathbb{R}\}\\
    & E_{2}(\lambda = 2) = ker(A - 2I)^2 = ker(\begin{pmatrix}
        1 & 1\\
        -1 & -1
    \end{pmatrix}^2 = ker(\begin{pmatrix}
        0 & 0\\
        0 & 0
    \end{pmatrix}) = \{(x,y):x,y \in \mathbb{R}\}
\end{split}
$$

Nuestro vector $v_{2}$ será un vector que pertenezca a $E_2(\lambda = 2)$ pero que no pertenezca a $E_1(\lambda = 2)$, por lo que podemos tomar $v_2 = (1,0)$. 

El vector $v_{1}$ será igual a $v_{1}=(A - 2I)v_{2} = (1,-1)$.

Por lo tanto, la solución general del sistema de ecuaciones diferenciales es:

$$
\begin{split}
    & Y_{SGEH} = C_{1}v_{1}e^{2t} + C_{2}(tv_{1} + v_{2})e^{2t} =\\
    & = C_{1}\begin{pmatrix}
        1\\
        -1
    \end{pmatrix}e^{2t} + C_{2}\left(t\begin{pmatrix}
        1\\
        -1
    \end{pmatrix} + \begin{pmatrix}
        1\\
        0
    \end{pmatrix}\right)e^{2t}
\end{split}
$$

En forma de sistema de ecuaciones:

$$
Y_{SGEH} = \begin{cases}
    y_{1}(t) = C_{1}e^{2t} + C_{2}(t + 1)e^{2t}\\
    y_{2}(t) = -C_{1}e^{2t} - C_{2}te^{2t}
\end{cases}
$$

