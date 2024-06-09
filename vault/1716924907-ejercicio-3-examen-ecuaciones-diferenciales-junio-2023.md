---
id: 1716924907-ejercicio-3-examen-ecuaciones-diferenciales-junio-2023
aliases:
  - Ejercicio 3 examen ecuaciones diferenciales junio 2023
tags:
  - ecuaciones-diferenciales
---

# Completa los siguientes apartados relativos al sistema de ecuaciones diferenciales que se muestra a continuación:

$$
\begin{cases}
    x' = -5x + y + 6e^{2t}
    y' = 4x - 2y -e^{2t}
\end{cases}
$$

##### a) Obtener la solución general del sistema.

Calculamos la matriz de coeficientes:

$$
A = \begin{pmatrix}
    -5 & 1\\
    4 & -2
\end{pmatrix}
$$

Calculamos los autovalores de la matriz de coeficientes:

$$
\begin{split}
    & \det(A - \lambda I) = 0\\
    & \begin{vmatrix}
        -5-\lambda & 1\\
        4 & -2-\lambda
    \end{vmatrix} = (-5-\lambda )(-2-\lambda) - 4 = \lambda^2 + 7 lambda + 6 = 0\\
    & \frac{-7 \pm \sqrt{49 - 4\cdot 6}}{2} = \frac{-7 \pm \sqrt{25}}{2} = \frac{-7 \pm 5}{2} = -6 \quad -1 \implies\\
    & \lambda_1 = -6 \quad \lambda_2 = -1
\end{split}
$$

Calculamos los autovectores asociados a cada autovalor:

- Para $\lambda_1 = -6$:

$$
\begin{split}
    & S_{\lambda = -6} = \left(\begin{array}{cc|c}
        -5+6 & 1 & 0\\
        4 & -2+6 & 0
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        1 & 1 & 0\\
        4 & 4 & 0
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        1 & 1 & 0\\
        0 & 0 & 0
    \end{array}\right) = \{(-y,y):y\in \mathbb{R}\} \implies\\
    & B_{S_{\lambda = -6}} = \begin{pmatrix}
        1\\
        -1
    \end{pmatrix}
\end{split}
$$

- Para $\lambda_2 = -1$:

$$
\begin{split}
    & S_{\lambda = -1} = \left(\begin{array}{cc|c}
        -5+1 & 1 & 0\\
        4 & -2+1 & 0
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        -4 & 1 & 0\\
        4 & -1 & 0
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        -4 & 1 & 0\\
        0 & 0 & 0
    \end{array}\right) = \{(y,4y):y\in \mathbb{R}\} \implies\\
    & B_{S_{\lambda = -1}} = \begin{pmatrix}
        1\\
        4
    \end{pmatrix}
\end{split}
$$

Por lo tanto, la solución general al sistema de ecuaciones homogéneo es:

$$
Y_{SGEH} = C_{1}\begin{pmatrix}
    1\\
    -1
\end{pmatrix}e^{-6t} + C_{2}\begin{pmatrix}
    1\\
    4
\end{pmatrix}e^{-t}
$$

Calculamos una solución particular para el sistema no homogéneo. Para ello, utilizaremos el método de coeficientes indeterminados.

$$
\begin{split}
    & Y_{P} = \begin{pmatrix}
        A_{0}e^{2t}\\
        B_{0}e^{2t}
    \end{pmatrix} \implies Y_{P}' = \begin{pmatrix}
        2A_{0}e^{2t}\\
        2B_{0}e^{2t}
    \end{pmatrix}\\
\end{split}
$$

Sustituimos en el sistema de ecuaciones:

$$
\begin{split}
    & Y' = AY + B \implies\\
    & \begin{pmatrix}
        2A_{0}e^{2t}\\
        2B_{0}e^{2t}
    \end{pmatrix} = \begin{pmatrix}
        -5 & 1\\
        4 & -2
    \end{pmatrix}\begin{pmatrix}
        A_{0}e^{2t}\\
        B_{0}e^{2t}
    \end{pmatrix} + \begin{pmatrix}
        6e^{2t}\\
        -e^{2t}
    \end{pmatrix}
\end{split}
$$

En forma de ecuaciones:

$$
\begin{split}
    & \begin{cases}
        2A_{0}e^{2t} = -5A_{0}e^{2t} + B_{0}e^{2t} + 6e^{2t}\\
        2B_{0}e^{2t} = 4A_{0}e^{2t} - 2B_{0}e^{2t} - e^{2t}
    \end{cases} \implies
    \begin{cases}
        2A_{0} = -5A_{0} + B_{0} + 6\\
        2B_{0} = 4A_{0} - 2B_{0} - 1
    \end{cases} \implies\\
    & \begin{cases}
        7A_{0} - B_{0} = 6\\
        4A_{0} + -4B_{0} = 1
    \end{cases} 
\end{split}
$$

Resolvemos el sistema mediante el método de Gauss:

$$
\begin{split}
    & \left(\begin{array}{cc|c}
        7 & -1 & 6\\
        4 & -4 & 1
    \end{array}\right) \sim \left(\begin{array}{cc|c}
        7 & -1 & 6\\
        28 & -28 & 7
    \end{array}\right) \sim \left(\begin{array}{cc|c}
        7 & -1 & 6\\
        0 & -24 & -17
    \end{array}\right) \implies\\
\end{split}
$$

Resolvemos el sistema escalonado:

$$
\begin{cases}
    A_{0} =  \frac{6 + \frac{17}{24}}{7} = \frac{23}{24}
    B_{0} = \frac{17}{24}
\end{cases}
$$

Por lo tanto, la solución particular del sistema no homogéneo es:

$$
Y_{SP} = \begin{pmatrix}
    \frac{23}{24}e^{2t}\\
    \frac{17}{24}e^{2t}
\end{pmatrix}
$$

Y por último, la solución general del sistema de ecuaciones diferenciales es:

$$
Y_{SGEC} = Y_{SGEH} + Y_{SPEC} = C_{1}\begin{pmatrix}
    1\\
    -1
\end{pmatrix}e^{-6t} + C_{2}\begin{pmatrix}
    1\\
    4
\end{pmatrix}e^{-t} + \begin{pmatrix}
    \frac{23}{24}e^{2t}\\
    \frac{17}{24}e^{2t}
\end{pmatrix}
$$

En forma de sistema de ecuaciones:

$$
Y_{SGEC} = \begin{cases}
    x = C_{1}e^{-6t} + C_{2}e^{-t} + \frac{23}{24}e^{2t}\\
    y = -C_{1}e^{-6t} + 4C_{2}e^{-t} + \frac{17}{24}e^{2t}
\end{cases}
$$
