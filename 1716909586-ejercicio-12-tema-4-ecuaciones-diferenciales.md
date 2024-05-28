---
id: 1716909586-ejercicio-12-tema-4-ecuaciones-diferenciales
aliases:
  - Ejercicio 12 tema 4 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve el siguiente sistema de ecuaciones diferenciales:

$$
\begin{cases}
    x' = 2x + y + z\\
    y' = 2y - z\\
    z' = 2z
\end{cases}
$$

Calculamos la matriz de coeficientes:

$$
A = \begin{pmatrix}
    2 & 1 & 1\\
    0 & 2 & -1\\
    0 & 0 & 2
\end{pmatrix}
$$

Calculamos los autovalores de la matriz de coeficientes:

$$
\begin{split}
    & \det(A - \lambda I) = 0\\
    & \det\left(\begin{pmatrix}
        2-\lambda & 1 & 1\\
        0 & 2-\lambda & -1\\
        0 & 0 & 2-\lambda
    \end{pmatrix}\right) = 0\\
    & \lambda_1 = 2 \text{ (triple)}
\end{split}
$$

Calculamos los autovectores asociados a cada autovalor:

- Para $\lambda_1 = 2$:

$$
\begin{split}
    & S_{\lambda = 2} = \left(\begin{array}{ccc|c}
        2-2 & 1 & 1 & 0\\
        0 & 2-2 & -1 & 0\\
        0 & 0 & 2-2 & 0
    \end{array}\right) \sim
    \left(\begin{array}{ccc|c}
        0 & 1 & 1 & 0\\
        0 & 0 & -1 & 0\\
        0 & 0 & 0 & 0
    \end{array}\right) = \{(x, 0, 0):x\in \mathbb{R}\} \implies\\
    & B_{S_{\lambda = 2}} = \left\{\begin{pmatrix}
        0\\
        1\\
        0
    \end{pmatrix}\right\}
\end{split}
$$

Como vemos, la matriz no es diagonalizable, por lo que calcularemos la [forma canónica de Jordan](1716897460-matriz-de-jordan). Para ello, calculamos los autovectores generalizados asociados a cada autovalor:

- Para $\lambda_1 = 2$:

$$
\begin{split}
    & E_{1}(\lambda = 2) = \{(x, 0, 0):x\in \mathbb{R}\}\\
    & E_{2}(\lambda = 2) = ker(A - 2I)^2 = ker(\begin{pmatrix}
        0 & 1 & 1\\
        0 & 0 & -1\\
        0 & 0 & 0
    \end{pmatrix}^2) = ker(\begin{pmatrix}
        0 & 0 & -1\\
        0 & 0 & 0\\
        0 & 0 & 0
    \end{pmatrix}) = \{(x, y, 0):x, y \in \mathbb{R}\}\\
    & E_{3}(\lambda = 2) = ker(A - 2I)^3 = ker(\begin{pmatrix}
        0 & 1 & 1\\
        0 & 0 & -1\\
        0 & 0 & 0
    \end{pmatrix}^3) = ker(\begin{pmatrix}
        0 & 0 & 0\\
        0 & 0 & 0\\
        0 & 0 & 0\\
    \end{pmatrix}) = \{(x, y, z):x, y, z \in \mathbb{R}\}
\end{split}
$$

| $E_{1}(\lambda = 2)$ | $E_{2}(\lambda = 2)$  | $E_{3}(\lambda = 2)$  |
| --------------- | --------------- | --------------- |
| $v_{1}$  | $v_{2}$ | $v_{3}$ |

Nuestro vector $v_{3}$ será un vector que pertenezca a $E_3(\lambda = 2)$ pero que no pertenezca a $E_2(\lambda = 2)$, por ejemplo, $v_3 = (0, 0, 1)$. 

El vector $v_{2}$:

$$
\begin{split}
    & v_{2} = (A - 2I) v_{3} = \begin{pmatrix}
        0 & 1 & 1\\
        0 & 0 & -1\\
        0 & 0 & 0
    \end{pmatrix} \begin{pmatrix}
        0\\
        0\\
        1
    \end{pmatrix} = \begin{pmatrix}
        1\\
        -1\\
        0
    \end{pmatrix}
\end{split}
$$

El vector $v_{1}$:

$$
\begin{split}
    & v_{1} = (A - 2I) v_{2} = \begin{pmatrix}
        0 & 1 & 1\\
        0 & 0 & -1\\
        0 & 0 & 0
    \end{pmatrix} \begin{pmatrix}
        1\\
        -1\\
        0
    \end{pmatrix} = \begin{pmatrix}
        -1\\
        0\\
        0
    \end{pmatrix}
\end{split}
$$

Por lo tanto, la solución general del sistema de ecuaciones diferenciales es:

$$
\begin{split}
    & Y_{SGEH} = C_{1}v_{1}e^{2t} + C_{2}(tv_{1} + v_{2})e^{2t} + C_{3}(\frac{t_{2}}{2}v_{1} + tv_{2} + v_{3})e^{2t} =\\
    & = C_{1}\begin{pmatrix}
        -1\\
        0\\
        0
    \end{pmatrix}e^{2t} + C_{2}\left(t\begin{pmatrix}
        -1\\
        0\\
        0
    \end{pmatrix} + \begin{pmatrix}
        1\\
        -1\\
        0
    \end{pmatrix}\right)e^{2t} + C_{3}\left(\frac{t^{2}}{2}\begin{pmatrix}
        -1\\
        0\\
        0
    \end{pmatrix} + t\begin{pmatrix}
        1\\
        -1\\
        0
    \end{pmatrix} + \begin{pmatrix}
        0\\
        0\\
        1
    \end{pmatrix}\right)e^{2t}
\end{split} 
$$

En forma de sistema de ecuaciones:

$$
Y_{SGEH} = \begin{cases}
    x(t) = -C_{1}e^{2t} + C_{2}(-t+1)e^{2t} + C_3(-\frac{t^2}{2} + t)e^{2t} \\
    y(t) = -C_{2}e^{2t} - C_{3}e^{2t}\\
    z(t) = C_{3}e^{2t}
\end{cases}
$$

