---
id: 1716928158-ejercicio-17-tema-4-ecuaciones-diferenciales
aliases:
  - Ejercicio 17 tema 4 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve este sistema de ecuaciones utilizando la técnica de coeficientes indeterminados:

$$
Y' = \begin{pmatrix}
    5 & 3\\
    -1 & 1
\end{pmatrix}Y + \begin{pmatrix}
    -2e^{-x} + 1 \\
    e^{-x} - 5x + 7 
\end{pmatrix}
$$

Calculamos los autovalores de la matriz de coeficientes:

$$
\begin{split}
    & \det(A - \lambda I) = 0\\
    & \begin{vmatrix}
        5-\lambda & 3\\
        -1 & 1-\lambda
    \end{vmatrix} = (5-\lambda)(1-\lambda) + 3 = \lambda^2 - 6\lambda + 8 = 0\\
    & \frac{6 \pm \sqrt{36 - 4*8}}{2} = \frac{6 \pm \sqrt{4}}{2} = \frac{6 \pm 2}{2} \implies \lambda_1 = 4 \quad \lambda_2 = 2
\end{split}
$$

Calculamos los autovectores asociados a cada autovalor:

- Para $\lambda_1 = 4$:

$$
\begin{split}
    & S_{\lambda = 4} = \left(\begin{array}{cc|c}
        5-4 & 3 & 0\\
        -1 & 1-4 & 0
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        1 & 3 & 0\\
        -1 & -3 & 0
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        1 & 3 & 0\\
        0 & 0 & 0
    \end{array}\right) = \{(3y, -y):y\in \mathbb{R}\} \implies\\
    & B_{S_{\lambda = 4}} = \begin{pmatrix}
        3\\
        -1
    \end{pmatrix}
\end{split}
$$

- Para $\lambda_2 = 2$:

$$
\begin{split}
    & S_{\lambda = 2} = \left(\begin{array}{cc|c}
        5-2 & 3 & 0\\
        -1 & 1-2 & 0
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        3 & 3 & 0\\
        -1 & -1 & 0
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        3 & 3 & 0\\
        0 & 0 & 0
    \end{array}\right) = \{(y, -y):y\in \mathbb{R}\} \implies\\
    & B_{S_{\lambda = 2}} = \begin{pmatrix}
        1\\
        -1
    \end{pmatrix}
\end{split}
$$

Por lo tanto, la solución general del sistema de ecuaciones es:

$$
Y = C_1e^{4x}\begin{pmatrix}
    3\\
    -1
\end{pmatrix} + C_2e^{2x}\begin{pmatrix}
    1\\
    -1
\end{pmatrix}
$$

Para encontrar la solución particular, usamos la técnica de coeficientes indeterminados. 

$$
\begin{split}
    & s_{1}(x) = -2e^{-x} + 1\\
    & s_{2}(x) = e^{-x} - 5x + 7
\end{split}
$$

Vamos a buscar la primera parte de la solución particular:

$$
\begin{pmatrix}
    -2e^{-x}\\
    e^{-x}
\end{pmatrix}
$$

La solución particular para la primera parte es:

$$
Y_{SP_{1}} = \begin{pmatrix}
    A_0e^{-x}\\
    B_0e^{-x}
\end{pmatrix}
$$

Su derivada es:

$$
\begin{split}
    & Y'_{SP_{1}} = \begin{pmatrix}
        -A_0e^{-x}\\
        -B_0e^{-x}
    \end{pmatrix}
\end{split}
$$

Sustituimos en el sistema de ecuaciones:

$$
\begin{split}
    & Y' = AY + B \implies\\
    & \begin{pmatrix}
        -A_0e^{-x}\\
        -B_0e^{-x}
    \end{pmatrix} = \begin{pmatrix}
        5 & 3\\
        -1 & 1
    \end{pmatrix}\begin{pmatrix}
        A_0e^{-x}\\
        B_0e^{-x}
    \end{pmatrix} + \begin{pmatrix}
        -2e^{-x}\\
        e^{-x}
    \end{pmatrix} \implies\\
    & \begin{pmatrix}
        -A_0e^{-x}\\
        -B_0e^{-x}
    \end{pmatrix} = \begin{pmatrix}
        5A_0e^{-x} + 3B_0e^{-x} - 2e^{-x}\\
        -A_0e^{-x} + B_0e^{-x} + e^{-x}
    \end{pmatrix}
\end{split}
$$

En forma de ecuaciones:

$$
\begin{split}
    & \begin{cases}
        6A_0 + 3B_{0} = 2
        A_0 - 2B_0 = 1
    \end{cases} \implies
    \left(\begin{array}{cc|c}
        6 & 3 & 2\\
        1 & -2 & 1
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        1 & -2 & 1\\
        6 & 3 & 2
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        1 & -2 & 1\\
        0 & 15 & -4
    \end{array}\right) \implies\\
    & \begin{cases}
        A_0 - 2B_0 = 1\\
        15B_0 = -4 \implies B_0 = -\frac{4}{15}
    \end{cases} \implies
    \begin{cases}
        A_0 =  1 + 2B_0 = 1 - \frac{8}{15} = \frac{7}{15}\\
        B_0 = -\frac{4}{15}
    \end{cases}
\end{split}
$$

Por lo tanto, la primera parte de la solución particular es:

$$
\begin{pmatrix}
    \frac{7}{15}e^{-x}\\
    -\frac{4}{15}e^{-x}
\end{pmatrix}
$$

Ahora vamos con la segunda parte de la solución particular:

$$
\begin{pmatrix}
    1\\
    -5x + 7
\end{pmatrix}
$$

La solución particular para la segunda parte es:

$$
Y_{SP_{2}} = \begin{pmatrix}
    A_1x + A_{0}\\
    B_1x + B_0
\end{pmatrix}
$$

Su derivada es:

$$
Y'_{SP_{2}} = \begin{pmatrix}
    A_{1}\\
    B_1
\end{pmatrix}
$$

Sustituimos en el sistema de ecuaciones:

$$
\begin{split}
    & Y' = AY + B \implies\\
    & \begin{pmatrix}
        A_{1}\\
        B_1
    \end{pmatrix} = \begin{pmatrix}
        5 & 3\\
        -1 & 1
    \end{pmatrix}\begin{pmatrix}
        A_1x + A_{0}\\
        B_1x + B_0
    \end{pmatrix} + \begin{pmatrix}
        1\\
        -5x + 7
    \end{pmatrix} \implies\\
    & \begin{pmatrix}
        A_{1}\\
        B_1
    \end{pmatrix} = \begin{pmatrix}
        5A_1x + 5A_0 + 3B_1x + 3B_0 + 1\\
        -A_1x - A_0 + B_1x + B_0 - 5x + 7
    \end{pmatrix}
\end{split}
$$

En forma de ecuaciones:

$$
\begin{split}
    & \begin{cases}
        x(5A_1 + 3B_1) + 5A_0 + 3B_0 + 1 = A_{1}\\
        x(-A_1 + B_1 - 5) - A_0 + B_0 + 7 = B_{1}
    \end{cases} \implies \begin{cases}
        5A_1 + 3B_1 = 0\\
        -A_1 + B_1 = 5
    \end{cases} \implies\\
    & \left(\begin{array}{cc|c}
        5 & 3 & 0\\
        -1 & 1 & 5
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        -1 & 1 & 5\\
        0 & 8 & 25
    \end{array}\right) \implies \begin{cases}
        5A_1 + 3B_1 = 0\\
        8B_1 = 25 \implies B_1 = \frac{25}{8}
    \end{cases} \implies\\
    & \begin{cases}
        A_1 = -\frac{3}{5}B_1 = -\frac{3}{5}\cdot\frac{25}{8} = -\frac{75}{40} = -\frac{15}{8}\\
        B_1 = \frac{25}{8}
    \end{cases}\\
    & \begin{cases}
        5A_0 + 3B_0 + 1 = A_1\\
        -A_0 + B_0 + 7 = B_1
    \end{cases} \implies
    \begin{cases}
        5A_0 + 3B_0 = -\frac{15}{8} - 1\\
        -A_0 + B_0 = \frac{25}{8} - 7
    \end{cases} \implies\\
    & \left(\begin{array}{cc|c}
        5 & 3 & -\frac{23}{8}\\
        -1 & 1 & -\frac{31}{8} 
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        -1 & 1 & -\frac{31}{8}\\
        5 & 3 & -\frac{23}{8}
    \end{array}\right) \implies
    \left(\begin{array}{cc|c}
        -1 & 1 & -\frac{31}{8}\\
        0 & 8 & -\frac{31\cdot 5}{8} - \frac{23}{8}
    \end{array}\right) \implies\\
    & \begin{cases}
        A_0  = \frac{31}{8} - \frac{89}{32} = \frac{35}{32}\\
        B_0 = -\frac{89}{32} 
    \end{cases} \implies
\end{split}
$$

Por lo tanto, la segunda parte de la solución particular es:

$$
\begin{pmatrix}
    -\frac{15}{8}x + \frac{35}{32}\\
    \frac{25}{8}x - \frac{89}{32}
\end{pmatrix}
$$

Por lo tanto, la solución particular del sistema no homogéneo es:

$$
Y_{SP} = \begin{pmatrix}
    \frac{7}{15}e^{-x}\\
    -\frac{4}{15}e^{-x}
\end{pmatrix} + \begin{pmatrix}
    -\frac{15}{8}x + \frac{35}{32}\\
    \frac{25}{8}x - \frac{89}{32}
\end{pmatrix} = \begin{pmatrix}
    \frac{7}{15}e^{-x} + -\frac{15}{8}x + \frac{35}{32}\\
    -\frac{4}{15}e^{-x} + \frac{25}{8}x - \frac{89}{32}
\end{pmatrix}
$$

Finalmente, la solución general del sistema de ecuaciones es:

$$
Y_{SGEC} = Y_{SGEH} + Y_{SPEC} = C_1e^{4x}\begin{pmatrix}
    3\\
    -1
\end{pmatrix} + C_2e^{2x}\begin{pmatrix}
    1\\
    -1
\end{pmatrix} + \begin{pmatrix}
    \frac{7}{15}e^{-x} + -\frac{15}{8}x + \frac{35}{32}\\
    -\frac{4}{15}e^{-x} + \frac{25}{8}x - \frac{89}{32}
\end{pmatrix}
$$
En forma de sistema de ecuaciones:

$$
Y_{SGEC} = \begin{cases}
    y_1(x) = C_1e^{4x}3 + C_2e^{2x} + \frac{7}{15}e^{-x} + -\frac{15}{8}x + \frac{35}{32}\\
    y_2(x) = -C_1e^{4x} + C_2e^{2x} - \frac{4}{15}e^{-x} + \frac{25}{8}x - \frac{89}{32}
\end{cases}
$$
