---
id: 1716974550-ejercicio-19-tema-4-ecuaciones-diferenciales
aliases:
  - Ejercicio 19 tema 4 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve el siguiente sistema de ecuaciones utilizando la técnica de variación de parámetros:

$$
Y' = \begin{pmatrix}
    -3 & 1\\
    2 & -4
\end{pmatrix}Y + \begin{pmatrix}
    3x\\
    e^{-x}
\end{pmatrix}
$$

Sacamos los autovalores:

$$
\begin{split}
    & \det(A - \lambda I) = 0\\
    & \begin{vmatrix}
        -3 - \lambda & 1\\
        2 & -4 - \lambda
    \end{vmatrix} = (-3 - \lambda)(-4 - \lambda) - 2 = \lambda^2 + 7\lambda + 10 = 0 \implies\\
    & \frac{-7 \pm \sqrt{49 - 4\cdot 10}}{2} = \frac{-7 \pm \sqrt{9}}{2} = \frac{-7 \pm 3}{2} \implies \\
    & \lambda_1 = -5, \quad \lambda_2 = -2
\end{split}
$$

Calculamos los autovectores:

- Para $\lambda_1 = -5$:

$$
\begin{split}
    & S_{\lambda_{1}=-5} = \left(\begin{array}{cc|c}
        -3-(-5) & 1 & 0\\
        2 & -4-(-5) & 0
    \end{array}\right) \sim \left(\begin{array}{cc|c}
        2 & 1 & 0\\
        2 & 1 & 0
    \end{array}\right) = \{(x, -2x): x \in \mathbb{R}\}\implies\\
    & B_{\lambda_{1}=-5} = \left\{\begin{pmatrix}
        1\\
        -2
    \end{pmatrix}\right\}
\end{split}
$$

- Para $\lambda_2 = -2$:

$$
\begin{split}
    & S_{\lambda_{2}=-2} = \left(\begin{array}{cc|c}
        -3-(-2) & 1 & 0\\
        2 & -4-(-2) & 0
    \end{array}\right) \sim \left(\begin{array}{cc|c}
        -1 & 1 & 0\\
        2 & -2 & 0
    \end{array}\right) \sim \left(\begin{array}{cc|c}
        -1 & 1 & 0\\
        0 & 0 & 0
    \end{array}\right) = \{(x, x): x \in \mathbb{R}\}\implies\\
    & B_{\lambda_{2}=-2} = \left\{\begin{pmatrix}
        1\\
        1
    \end{pmatrix}\right\}
\end{split}
$$

Por lo tanto, la solución general del sistema homogéneo es:

$$
\begin{split}
    & Y_h = C_1\begin{pmatrix}
        1\\
        -2
    \end{pmatrix}e^{-5x} + C_2\begin{pmatrix}
        1\\
        1
    \end{pmatrix}e^{-2x}
\end{split}
$$

En forma de ecuaciones:

$$
Y_h = \begin{cases}
    y_1 = C_1e^{-5x} + C_2e^{-2x}\\
    y_2 = -2C_1e^{-5x} + C_2e^{-2x}
\end{cases}
$$

Ahora calculamos la solución particular:

- Empezaremos con la primera parte de la solución particular:

$$
Y_{p_{1}} = \begin{pmatrix}
    A_{1}x + A_{0}\\
    B_{1}x + B_{0}
\end{pmatrix}
$$

Derivamos:

$$
Y'_{p_{1}} = \begin{pmatrix}
    A_{1}\\
    B_{1}
\end{pmatrix}
$$

Sustituimos en la ecuación original:

$$
\begin{split}
    & Y' = AY + B \implies\\
    & \begin{pmatrix}
        A_{1}\\
        B_{1}
    \end{pmatrix} = \begin{pmatrix}
        -3 & 1\\
        2 & -4
    \end{pmatrix}\begin{pmatrix}
        A_{1}x + A_{0}\\
        B_{1}x + B_{0}  
    \end{pmatrix} + \begin{pmatrix}
        3x\\
        0
    \end{pmatrix} \implies\\
    & \begin{pmatrix}
        A_{1}\\
        B_{1}
    \end{pmatrix} = \begin{pmatrix}
        -3A_{1}x - 3A_{0} + B_{1}x + B_{0} + 3x\\
        2A_{1}x + 2A_{0} - 4B_{1}x - 4B_{0}
    \end{pmatrix}
\end{split}
$$

Obtenemos el siguiente sistema de ecuaciones:

$$
\begin{split}
    & \begin{cases}
        x(-3A_{1} + B_{1} + 3) + (-3A_{0} + B_{0}) = A_{1}\\
        x(2A_{1} - 4B_{1}) + (2A_{0} - 4B_{0}) = B_{1}
    \end{cases} \implies\\
    &\begin{cases}
        -3A_{1} + B_{1} = 0\\
        -3A_{0} + B_{0} + 3 = A_{1}\\
        2A_{1} - 4B_{1} = 0\\
        2A_{0} - 4B_{0} = B_{1}
    \end{cases}
\end{split}
$$

Empezaremos resolviendo el sistema de $A_{1},B_{1}$:

$$
\begin{split}
    & \begin{cases}
       -3A_{1} + B_{1} = -3\\ 
       2A_{1} - 4B_{1} = 0
    \end{cases} \implies
    \left(\begin{array}{cc|c}
        -3 & 1 & -3\\
        2 & -4 & 0
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        -3 & 1 & -3\\
        6 & -12 & 0
    \end{array}\right) \implies
    \left(\begin{array}{cc|c}
        -3 & 1 & -3\\
        0 & -10 & -6
    \end{array}\right) \implies\\
    & \begin{cases}
        -3A_{1} + B_{1} = -3\\
        B_{1} = \frac{3}{5}
    \end{cases} \implies
    \begin{cases}
        A_{1} = 1 + \frac{1}{5} = \frac{6}{5}\\
        B_{1} = \frac{3}{5}
    \end{cases}
\end{split}
$$

Ahora, resolvemos el sistema de $A_{0},B_{0}$:

$$
\begin{split}
    & \begin{cases}
        -3A_{0} + B_{0} = \frac{6}{5}\\
        2A_{0} - 4B_{0} = \frac{3}{5}
    \end{cases} \implies
    \left(\begin{array}{cc|c}
        -3 & 1 & \frac{6}{5}\\
        2 & -4 & \frac{3}{5}
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        -3 & 1 & \frac{6}{5}\\
        6 & -12 & \frac{9}{5}
    \end{array}\right) \sim\\
    & \left(\begin{array}{cc|c}
        -3 & 1 & \frac{6}{5}\\
        0 & -10 & \frac{21}{5}
    \end{array}\right) \implies
    \begin{cases}
        -3A_{0} + B_{0} = \frac{6}{5}\\
        B_{0} = -\frac{21}{50}
    \end{cases} \implies
    \begin{cases}
        A_{0} = -\frac{7}{50} - \frac{2}{5} = -\frac{27}{50}\\
        B_{0} = -\frac{21}{50}
    \end{cases}
\end{split}
$$

Por lo tanto, la primera parte de la solución particular es:

$$
Y_{p_{1}} = \begin{pmatrix}
    \frac{6}{5}x - \frac{27}{50}\\
    \frac{3}{5}x - \frac{21}{50}
\end{pmatrix}
$$

- Ahora, calculamos la segunda parte de la solución particular:

$$
Y_{p_{2}} = \begin{pmatrix}
    A_{0}e^{-x}\\ 
    B_{0}e^{-x}
\end{pmatrix}
$$

Derivamos:

$$
Y'_{p_{2}} = \begin{pmatrix}
    -A_{0}e^{-x}\\
    -B_{0}e^{-x}
\end{pmatrix}
$$

Sustituimos en la ecuación original:

$$
\begin{split}
    & Y' = AY + B \implies\\
    & \begin{pmatrix}
        -A_{0}e^{-x}\\
        -B_{0}e^{-x}
    \end{pmatrix} = \begin{pmatrix}
        -3 & 1\\
        2 & -4
    \end{pmatrix}\begin{pmatrix}
        A_{0}e^{-x}\\
        B_{0}e^{-x}
    \end{pmatrix} + \begin{pmatrix}
        0\\
        e^{-x}
    \end{pmatrix} \implies\\
    & \begin{pmatrix}
        -A_{0}e^{-x}\\
        -B_{0}e^{-x}
    \end{pmatrix} = \begin{pmatrix}
        -3A_{0}e^{-x} + B_{0}e^{-x}\\
        2A_{0}e^{-x} - 4B_{0}e^{-x} + e^{-x}
    \end{pmatrix}
\end{split}
$$

Obtenemos el siguiente sistema de ecuaciones:

$$
\begin{split}
    & \begin{cases}
        -3A_{0} + B_{0} = -A_{0}\\
        2A_{0} - 4B_{0} + 1 = -B_{0}
    \end{cases} \implies
    \begin{cases}
        -2A_{0} + B_{0} = 0\\
        2A_{0} - 3B_{0} = -1
    \end{cases} \implies\\
     & \left(\begin{array}{cc|c}
        -2 & 1 & 0\\
        2 & -3 & -1
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        -2 & 1 & 0\\
        0 & -2 & -1
    \end{array}\right) \implies
    \begin{cases}
        -2A_{0} + B_{0} = 0\\
        B_{0} = \frac{1}{2}
    \end{cases} \implies\\
    & \begin{cases}
        A_{0} = \frac{1}{4}\\
        B_{0} = \frac{1}{2}
    \end{cases}
\end{split}
$$

Por lo tanto, la segunda parte de la solución particular es:

$$
Y_{p_{2}} = \begin{pmatrix}
    \frac{1}{4}e^{-x}\\
    \frac{1}{2}e^{-x}
\end{pmatrix}
$$

Por lo tanto, la solución particular es:

$$
Y_p = \begin{pmatrix}
    \frac{6}{5}x - \frac{27}{50} + \frac{1}{4}e^{-x}\\
    \frac{3}{5}x - \frac{21}{50} + \frac{1}{2}e^{-x}
\end{pmatrix}
$$

Por lo tanto, la solución general es:

$$
\begin{split}
    & Y = Y_h + Y_p = \begin{pmatrix}
        C_1e^{-5x} + C_2e^{-2x} + \frac{6}{5}x - \frac{27}{50} + \frac{1}{4}e^{-x}\\
        -2C_1e^{-5x} + C_2e^{-2x} + \frac{3}{5}x - \frac{21}{50} + \frac{1}{2}e^{-x}
    \end{pmatrix}
\end{split}
$$

En forma de ecuaciones:

$$
Y = \begin{cases}
    y_1 = C_1e^{-5x} + C_2e^{-2x} + \frac{6}{5}x - \frac{27}{50} + \frac{1}{4}e^{-x}\\
    y_2 = -2C_1e^{-5x} + C_2e^{-2x} + \frac{3}{5}x - \frac{21}{50} + \frac{1}{2}e^{-x}
\end{cases}
$$
