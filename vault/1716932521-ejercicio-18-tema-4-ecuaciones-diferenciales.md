---
id: 1716932521-ejercicio-18-tema-4-ecuaciones-diferenciales
aliases:
  - Ejercicio 18 tema 4 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve el siguiente sistema de ecuaciones utilizando la técnica de variación de parámetros:

$$
\begin{cases}
    x' = x + y\\
    y' = x + y + t
\end{cases}
$$

Calculamos la matriz de coeficientes:

$$
A = \begin{pmatrix}
    1 & 1\\
    1 & 1
\end{pmatrix}
$$

Sacamos los autovalores:

$$
\begin{split}
    & \det(A - \lambda I) = 0\\
    & \begin{vmatrix}
        1 - \lambda & 1\\
        1 & 1 - \lambda
    \end{vmatrix} = (1 - \lambda)^2 - 1 = 0 \implies\\
    & \lambda^2 - 2\lambda = 0 \implies \\
    & \lambda_1 = 0, \quad \lambda_2 = 2
\end{split}
$$

Calculamos los autovectores:

- Para $\lambda_1 = 0$:

$$
\begin{split}
    & S_{\lambda_{1}=0} = \left(\begin{array}{cc|c}
        1 & 1 & 0\\
        1 & 1 & 0
    \end{array}\right) \sim \left(\begin{array}{cc|c}
        1 & 1 & 0\\
        0 & 0 & 0
    \end{array}\right) = \{(x, -x): x \in \mathbb{R}\}\implies\\
    & B_{\lambda_{1}=0} = \left\{\begin{pmatrix}
        1\\
        -1
    \end{pmatrix}\right\}
\end{split}
$$

- Para $\lambda_2 = 2$:

$$
\begin{split}
    & S_{\lambda_{2}=2} = \left(\begin{array}{cc|c}
        1-2 & 1 & 0\\
        1 & 1-2 & 0
    \end{array}\right) \sim \left(\begin{array}{cc|c}
        -1 & 1 & 0\\
        0 & 0 & 0
    \end{array}\right) = \{(x, x): x \in \mathbb{R}\}\implies\\
    & B_{\lambda_{2}=2} = \left\{\begin{pmatrix}
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
        -1
    \end{pmatrix}e^{0t} + C_2\begin{pmatrix}
        1\\
        1
    \end{pmatrix}e^{2t}
\end{split}
$$

En forma de sistema de ecuaciones:

$$
\begin{split}
    & Y_h = \begin{cases}
        x = C_1 + C_2e^{2t}\\
        y = -C_1 + C_2e^{2t}
    \end{cases}
\end{split}
$$

Ahora para obtener la solución particular, usaremos la técnica de variación de parámetros. Sabiendo que la solución del sistema homogéneo es $Y_h = S(t)C$, la solución particular del sistema completo es:

$$
Y_p = S(t)\int S^{-1}(t)B(t)dt
$$

En nuestro caso, $S(t)$ es:

$$
\begin{split}
    & S(t) = \begin{pmatrix}
        1 & e^{2t} \\
        -1 & e^{et} 
    \end{pmatrix}
\end{split}
$$

Y $S^{-1}(t)$ es:

$$
\begin{split}
    & \left(\begin{array}{cc|cc}
        1 & e^{2t} & 1 & 0\\
        -1 & e^{2t} & 0 & 1
    \end{array}\right) \sim \left(\begin{array}{cc|cc}
        1 & e^{2t} & 1 & 0\\
        0 & 2e^{2t} & 1 & 1
    \end{array}\right) \sim \left(\begin{array}{cc|cc}
        2 & 2e^{2t} & 2 & 2\\
        0 & 2e^{2t}  &  1 & 1
    \end{array}\right) \sim \left(\begin{array}{cc|cc}
        2 & 0        & 1 & 1\\
        0 & 2e^{2t}  &  1 & 1
    \end{array}\right) \implies\\
    & S^{-1}(t) = \begin{pmatrix}
        \frac{1}{2} & \frac{1}{2}\\
        \frac{1}{2}e^{-2t}  & \frac{1}{2}e^{-2t}
    \end{pmatrix}
\end{split}
$$

Por lo tanto, la solución particular es:

$$
\begin{split}
    & Y_p = \begin{pmatrix}
        1 & e^{2t} \\
        -1 & e^{2t}
    \end{pmatrix}\int \begin{pmatrix}
        \frac{1}{2} & \frac{1}{2}\\
        \frac{1}{2}e^{-2t}  & \frac{1}{2}e^{-2t}
    \end{pmatrix}\begin{pmatrix}
        0\\
        t
    \end{pmatrix}dt =\\
    & = \begin{pmatrix}
        1 & e^{2t} \\
        -1 & e^{2t}
    \end{pmatrix}\int \begin{pmatrix}
        \frac{t}{2}\\
        \frac{t}{2}e^{-2t}
    \end{pmatrix}dt = \begin{pmatrix}
        1 & e^{2t} \\
        -1 & e^{2t}
    \end{pmatrix}\begin{pmatrix}
        \int \frac{t}{2}dt\\
        \int \frac{t}{2}e^{-2t}dt
    \end{pmatrix}
\end{split}
$$

Ahora, lo vamos a hacer por el método de coeficientes indeterminados. Como $\alpha  = 0$ y $\beta = 0$, la multiplicad de $\alpha + ip\beta$ es 1, por lo tanto la solución particular es:

$$
\begin{split}
    & Y_p = \begin{pmatrix}
        A_{2}t^2 + A_{1}t + A_{0}\\
        B_{2}t^2 + B_{1}t + B_{0}
    \end{pmatrix}
\end{split}
$$

Su derivada es:

$$
\begin{split}
    & Y_p' = \begin{pmatrix}
        2A_{2}t + A_{1}\\
        2B_{2}t + B_{1}
    \end{pmatrix}
\end{split}
$$

Sustituyendo en el sistema de ecuaciones:

$$
\begin{split}
    & Y' = AY+B \implies\\
    & \begin{pmatrix}
        2A_{2}t + A_{1}\\
        2B_{2}t + B_{1}
    \end{pmatrix} = \begin{pmatrix}
        1 & 1\\
        1 & 1
    \end{pmatrix}\begin{pmatrix}
        A_{2}t^2 + A_{1}t + A_{0}\\
        B_{2}t^2 + B_{1}t + B_{0}
    \end{pmatrix} + \begin{pmatrix}
        0\\
        t
    \end{pmatrix} \implies\\
    & \begin{pmatrix}
        2A_{2}t + A_{1}\\
        2B_{2}t + B_{1}
    \end{pmatrix} = \begin{pmatrix}
        A_{2}t^2 + A_{1}t + A_{0} + B_{2}t^2 + B_{1}t + B_{0}\\
        A_{2}t^2 + A_{1}t + A_{0} + B_{2}t^2 + B_{1}t + B_{0} + t
    \end{pmatrix}
\end{split}
$$

Entonces, tenemos el siguiente sistema de ecuaciones:

$$
\begin{split}
    & \begin{cases}
        2A_{2}t + A_{1} = t^2(A_{2} + B_{2}) + t(A_{1} + B_{1}) + A_{0} + B_{0}\\
        2B_{2}t + B_{1} = t^2(A_{2} + B_{2}) + t(A_{1} + B_{1} + 1) + A_{0} + B_{0}
    \end{cases} \implies\\
    & \begin{cases}
        A_{2} + B_{2} = 0\\
        A_{0} + B_{0} = A_{1} = B_{1}\\
        A_{1} + B_{1} = 2A_{2}\\
        A_{1} + B_{1} + 1 = 2B_{2}
    \end{cases} \implies
    \begin{cases}
        A_{2} = -B_{2}\\
        A_{0} + B_{0} = A_{1} = B_{1}\\
        2A_{1} = 2A_{2}\\
        2B_{1} + 1 = 2B_{2}
    \end{cases} \implies\\
    & \begin{cases}
        A_{2} = -B_{2}\\
        A_{0} + B_{0} = A_{1} = B_{1} = A_{2}\\
        B_{1} = B_{2} - \frac{1}{2} = -A_{2} - \frac{1}{2} = A_{2}
    \end{cases} \implies\\
    & A_{2} = -A_{2} - \frac{1}{2} \implies A_{2} = -\frac{1}{4} \implies\\
    & \begin{cases}
        A_{2} = -\frac{1}{4}\\
        A_{1} = -\frac{1}{4}\\
        B_{2} = \frac{1}{4}\\
        B_{1} = -\frac{1}{4}\\
        A_{0} = B_{0} = -\frac{1}{4}
    \end{cases} \implies
    \begin{cases}
        A_{2} = -\frac{1}{4}\\
        B_{2} = \frac{1}{4}\\
        A_{1} = -\frac{1}{4}\\
        B_{1} = -\frac{1}{4}\\
        A_{0} = -\frac{1}{4}\\
        B_{0} = 0
    \end{cases}
\end{split}
$$

Por lo tanto, la solución particular es:

$$
\begin{split}
    & Y_p = \begin{pmatrix}
        -\frac{1}{4}t^2 - \frac{1}{4}t - \frac{1}{4}\\
        \frac{1}{4}t^2 - \frac{1}{4}t
    \end{pmatrix}
\end{split}
$$

Finalmente, la solución general es:

$$
\begin{split}
    & Y = Y_h + Y_p = \begin{pmatrix}
        1\\
        -1
    \end{pmatrix}C_1 + \begin{pmatrix}
        1\\
        1
    \end{pmatrix}C_2e^{2t} + \begin{pmatrix}
        -\frac{1}{4}t^2 - \frac{1}{4}t - \frac{1}{4}\\
        \frac{1}{4}t^2 - \frac{1}{4}t
    \end{pmatrix}
\end{split}
$$

En forma de sistema de ecuaciones:

$$
Y = \begin{cases}
    x = C_1 + C_2e^{2t} - \frac{1}{4}t^2 - \frac{1}{4}t - \frac{1}{4}\\
    y = -C_1 + C_2e^{2t} + \frac{1}{4}t^2 - \frac{1}{4}t
\end{cases}
$$
