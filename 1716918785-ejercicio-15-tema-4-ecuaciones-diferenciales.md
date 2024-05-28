---
id: 1716918785-ejercicio-15-tema-4-ecuaciones-diferenciales
aliases:
  - Ejercicio 15 tema 4 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve el siguiente sistema de ecuaciones diferenciales:

$$
\begin{cases}
    x' = x\\
    y' = y - z\\
    z' = y + z
\end{cases}
$$

Calculamos la matriz de coeficientes:

$$
A = \begin{pmatrix}
    1 & 0 & 0\\
    0 & 1 & -1\\
    0 & 1 & 1
\end{pmatrix}
$$

Calculamos los autovalores de la matriz de coeficientes:

$$
\begin{split}
    & \det(A - \lambda I) = 0\\
    & \begin{vmatrix}
        1-\lambda & 0 & 0\\
        0 & 1-\lambda & -1\\
        0 & 1 & 1-\lambda
    \end{vmatrix} = 0\\
    & \lambda_1 = 1 \quad \lambda_2 = 1+i \quad \lambda_3 = 1-i
\end{split}
$$

Calculamos los autovectores asociados a cada autovalor:

- Para $\lambda_1 = 1$:

$$
\begin{split}
    & S_{\lambda = 1} = \left(\begin{array}{ccc|c}
        1-1 & 0 & 0 & 0\\
        0 & 1-1 & -1 & 0\\
        0 & 1 & 1-1 & 0
    \end{array}\right) \sim
    \left(\begin{array}{ccc|c}
        0 & 0 & 0 & 0\\
        0 & 0 & -1 & 0\\
        0 & 1 & 0 & 0
    \end{array}\right) = \{(x,0,0):x \in \mathbb{R}\} \implies\\
    & B_{S_{\lambda = 1}} = \left\{\begin{pmatrix}
        1\\
        0\\
        0
    \end{pmatrix}\right\}
\end{split}
$$

- Para $\lambda_2 = 1+i$:

$$
\begin{split}
    & S_{\lambda = 1+i} = \left(\begin{array}{ccc|c}
        1-(1+i) & 0 & 0 & 0\\
        0 & 1-(1+i) & -1 & 0\\
        0 & 1 & 1-(1+i) & 0
    \end{array}\right) \sim
    \left(\begin{array}{ccc|c}
        i & 0 & 0 & 0\\
        0 & 1 & -i & 0\\
        0 & 0 & 0 & 0
    \end{array}\right) = \{(0,xi,x):x \in \mathbb{R}\} \implies\\
    & B_{S_{\lambda = 1+i}} = \left\{\begin{pmatrix}
        0\\
        1\\
        -i
    \end{pmatrix}\right\}
\end{split}
$$

- Para $\lambda_3 = 1-i$:

$$
\begin{split}
    & B_{S_{\lambda = 1-i}} = \left\{\begin{pmatrix}
        0\\
        1\\
        i
    \end{pmatrix}\right\}
\end{split}
$$

Por lo tanto, la solución general del sistema de ecuaciones diferenciales es:

$$
\begin{split}
    & Y_{SGEH} = C_{1}\begin{pmatrix}
        1\\
        0\\
        0
    \end{pmatrix}e^{t} + C_{2}\begin{pmatrix}
        0\\
        1\\
        -i
    \end{pmatrix}e^{(1+i)t} + C_{3}\begin{pmatrix}
        0\\
        1\\
        i
    \end{pmatrix}e^{(1-i)t}
\end{split}
$$

Simplificamos la solución general:

$$
\begin{split}
    & Y_{SGEH} = C_{1}\begin{pmatrix}
        1\\
        0\\
        0
    \end{pmatrix}e^{t} + 2e^{t}\Re\left[\begin{pmatrix}
        0\\
        a+bi\\
        b-ai
    \end{pmatrix}(\cos(t) + i\sin(t))\right] =\\
    & = C_{1}\begin{pmatrix}
        1\\
        0\\
        0
    \end{pmatrix}e^{t} + 2e^{t}\begin{pmatrix}
        0\\
        a\cos(t) - b\sin(t)\\
        b\cos(t) + a\sin(t)
    \end{pmatrix} =\\
    & = C_{1}\begin{pmatrix}
        1\\
        0\\
        0
    \end{pmatrix}e^{t} + 2e^{t}\begin{pmatrix}
        0\\
        C_{1}\cos(t) - C_{2}\sin(t)\\
        C_{1}\cos(t) + C_{2}\sin(t)
    \end{pmatrix}
\end{split}
$$

En forma de sistema de ecuaciones:

$$
\begin{split}
    & Y_{SGEH} = \begin{cases}
        y_{1}(t) = C_{1}e^{t}\\
        y_{2}(t) = C_{2}\cos(t)e^{t} - C_{3}\sin(t)e^{t}\\
        y_{3}(t) = C_{2}\cos(t)e^{t} + C_{3}\sin(t)e^{t} 
    \end{cases}
\end{split}
$$
