---
id: 1716920132-ejercicio-16-tema-4-ecuaciones-diferenciales
aliases:
  - Ejercicio 16 tema 4 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve este sistema de ecuaciones utilizando la técnica indeterminados:

$$
\begin{cases}
    x' = 6x + y + 6t\\
    y' = 4x + 3y - 10t + 4
\end{cases}
$$

Calculamos la matriz de coeficientes:

$$
A = \begin{pmatrix}
    6 & 1\\ 
    4 & 3
\end{pmatrix}
$$

Calculamos los autovalores de la matriz de coeficientes:

$$
\begin{split}
    & \det(A - \lambda I) = 0\\
    & \begin{vmatrix}
        6-\lambda & 1\\
        4 & 3-\lambda
    \end{vmatrix} = (6-\lambda)(3-\lambda) - 4 = \lambda^2 - 9\lambda + 14 = 0\\
    & \frac{9 \pm \sqrt{81 - 4*14}}{2} = \frac{9 \pm \sqrt{25}}{2} = \frac{9 \pm 5}{2} \implies \lambda_1 = 7 \quad \lambda_2 = 2
\end{split}
$$

Calculamos los autovectores asociados a cada autovalor:

- Para $\lambda_1 = 7$:

$$
\begin{split}
    & S_{\lambda = 7} = \left(\begin{array}{cc|c}
        6-7 & 1 & 0\\
        4 & 3-7 & 0
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        -1 & 1 & 0\\
        4 & -4 & 0
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        -1 & 1 & 0\\
        0 & 0 & 0
    \end{array}\right) = \{(y,y):y\in \mathbb{R}\} \implies\\
    & B_{S_{\lambda = 7}} = \begin{pmatrix}
        1\\
        1
    \end{pmatrix}
\end{split}
$$

- Para $\lambda_2 = 2$:

$$
\begin{split}
    & S_{\lambda = 2} = \left(\begin{array}{cc|c}
        6-2 & 1 & 0\\
        4 & 3-2 & 0
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        4 & 1 & 0\\
        4 & 1 & 0
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        4 & 1 & 0\\
        0 & 0 & 0
    \end{array}\right) = \{(-\frac{1}{4}y,y):y\in \mathbb{R}\} \implies\\
    & B_{S_{\lambda = 2}} = \begin{pmatrix}
        1\\
        -4
    \end{pmatrix}
\end{split}
$$

Por lo tanto, la solución general del sistema de ecuaciones es:

$$
Y_{SGEH} = C_{1}\begin{pmatrix}
    1\\
    1
\end{pmatrix}e^{7t} + C_{2}\begin{pmatrix}
    1\\
    -4
\end{pmatrix}e^{2t}
$$

Para hallar la solución particular usaremos el método de coeficientes indeterminados.

$$
B = \begin{pmatrix}
    6t\\
    -10t + 4
\end{pmatrix} = \begin{pmatrix}
    e^{0t}(6t)\\ 
    e^{0t}(-10t + 4)
\end{pmatrix}
$$

Para ambos casos tenemos $\alpha = 0, \; \beta = \frac{\pi}{2}\; k = \max(m,n)=1, \; \mu = 0$, (donde $\mu$ sería $t$ en la nomenclatura de los apuntes) y sabemos que cada fila de la matriz de la solución particular es de la forma:

$$
t^{\mu}(A_k + \ldots + A_{1}t + A_{0})e^{\alpha t}\sin(\beta t) + t^{\mu}(B_k + \ldots + B_{1}t + B_{0})e^{\alpha t}\cos(\beta t)
$$

$$
Y_{SP} = \begin{pmatrix}
    A_{1}t + A_{0}\\
    B_{1}t + B_{0}
\end{pmatrix} 
$$

Su derivada es:

$$
Y_{SP}' = \begin{pmatrix}
    A_{1}\\
    B_{1}
\end{pmatrix}
$$

Por lo tanto ahora sustituimos en el sistema de ecuaciones:

$$
\begin{split}
    & Y' = AY + B \implies\\
    & \begin{pmatrix}
        A_{1}\\
        B_{1}
    \end{pmatrix} = \begin{pmatrix}
        6 & 1\\
        4 & 3
    \end{pmatrix}\begin{pmatrix}
        A_{1}t + A_{0}\\
        B_{1}t + B_{0}
    \end{pmatrix} + \begin{pmatrix}
        6t\\
        -10t + 4
    \end{pmatrix} \iff\\
    & \begin{pmatrix}
        A_{1}\\
        B_{1}
    \end{pmatrix} = \begin{pmatrix}
        6A_{1}t + 6A_{0} + B_{1}t + B_{0} + 6t\\
        4A_{1}t + 4A_{0} + 3B_{1}t + 3B_{0} - 10t + 4
    \end{pmatrix}
\end{split}
$$

En forma de ecuaciones:

$$
\begin{split}
    & \begin{cases}
        A_{1} = 6A_{0} + B_{0} + t(6A_{1} + B_{1} + 6)\\
        B_{1} = 4A_{0} + 3B_{0} + 4 + t(4A_{1} + 3B_{1} - 10)
    \end{cases} \implies
    \begin{cases}
        6A_{1} + B_{1}  = -6\\
        4A_{1} + 3B_{1} = 10
        A_{1} = 6A_{0} + B_{0}\\
        B_{1} = 4A_{0} + 3B_{0} + 4
    \end{cases}
\end{split}
$$

Resolvemos $A_{1}$ y $B_{1}$

$$
\begin{split}
    & \left(\begin{array}{cc|c}
        6 & 1 & -6\\
        4 & 3 & 10
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        6 & 1 & -6\\
        12 & 9 & 30
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        6 & 1 & -6\\
        0 & 7 & 42
    \end{array}\right) \implies\\
    & \begin{cases}
        6A_{1} + 6 = -6\\    
        B_{1} = 6
    \end{cases} \implies
    \begin{cases}
        A_{1} = -2\\
        B_{1} = 6
    \end{cases}
\end{split}
$$

Ahora resolvemos $A_{0}$ y $B_{0}$

$$
\begin{split}
    & \begin{cases}
        A_{1} = 6A_{0} + B_{0}\\
        B_{1} = 4A_{0} + 3B_{0} + 4
    \end{cases} \implies
    \begin{cases}
        6A_{0} + B_{0} = -2\\
        4A_{0} + 3B_{0} = 2
    \end{cases} \implies
    \left(\begin{array}{cc|c}
        6 & 1 & -2\\
        4 & 3 & 2
    \end{array}\right) \sim\\
    & \sim \left(\begin{array}{cc|c}
        6 & 1 & -2\\
        12 & 9 & 6
    \end{array}\right) \sim \left(\begin{array}{cc|c}
        6 & 1 & -2\\
        0 & 7 & 10
    \end{array}\right) \implies
    \begin{cases}
        6A_{0} + B_{0} = -2\\
        B_{0} = \frac{10}{7}
    \end{cases} \implies
    \begin{cases}
        A_{0} = \frac{-2 - \frac{10}{7}}{6} = -\frac{4}{7}\\
        B_{0} = \frac{10}{7}
    \end{cases}
\end{split}
$$

Por lo tanto, la solución particular es:

$$
Y_{SP} = \begin{pmatrix}
    -2t - \frac{4}{7}\\
    6t + \frac{10}{7}
\end{pmatrix}
$$

Finalmente, la solución general del sistema de ecuaciones es:

$$
Y_{SGEC} = Y_{SGEH} + Y_{SPEC} = C_{1}\begin{pmatrix}
    1\\
    1
\end{pmatrix}e^{7t} + C_{2}\begin{pmatrix}
    1\\
    -4
\end{pmatrix}e^{2t} + \begin{pmatrix}
    -2t - \frac{4}{7}\\
    6t + \frac{10}{7}
\end{pmatrix}
$$

En forma de sistema de ecuaciones:

$$
Y_{SGEC} = \begin{cases}
    x = C_{1}e^{7t} + C_{2}e^{2t} - 2t - \frac{4}{7}\\
    y = C_{1}e^{7t} - 4C_{2}e^{2t} + 6t + \frac{10}{7}
\end{cases}
$$
