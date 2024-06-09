---
id: 1716916919-ejercicio-14-tema-4-ecuaciones-diferenciales
aliases:
  - Ejercicio 14 tema 4 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve el siguiente sistema de ecuaciones diferenciales:

$$
\begin{cases}
    y_{1}' = 6y_{1} - y_{2}\\
    y_{2}' = 5y_{1} + 4y_{2}
\end{cases}
$$

Calculamos la matriz de coeficientes:

$$
A = \begin{pmatrix}
    6 & -1\\
    5 & 4
\end{pmatrix}
$$

Calculamos los autovalores de la matriz de coeficientes:

$$
\begin{split}
    & \det(A - \lambda I) = 0\\
    & \begin{vmatrix}
        6-\lambda & -1\\
        5 & 4-\lambda
    \end{vmatrix} = 0\\
    & \lambda_1 = 5+2i \quad \lambda_2 = 5-2i
\end{split}
$$

Calculamos los autovectores asociados a cada autovalor:

- Para $\lambda_1 = 5+2i$:

$$
\begin{split}
    & S_{\lambda = 5+2i} = \left(\begin{array}{cc|c}
        6-(5+2i) & -1 & 0\\
        5 & 4-(5+2i) & 0
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        1-2i & -1 & 0\\
        5 & -1-2i & 0
    \end{array}\right) \sim
    \left(\begin{array}{cc|c}
        5 & -1-2i & 0\\
        0 & 0 & 0
    \end{array}\right) = \{(\frac{1+2i}{5}y,y):y\in \mathbb{R}\} \implies\\
    & B_{S_{\lambda = 5+2i}} = \begin{pmatrix}
        1\\
        1-2i
    \end{pmatrix}
\end{split}
$$

- Para $\lambda_2 = 5-2i$, como son conjugados, el autovector asociado es el conjugado del autovector asociado a $\lambda_1$:

$$
\begin{split}
    & B_{S_{\lambda = 5-2i}} = \begin{pmatrix}
        1\\
        1+2i
    \end{pmatrix}
\end{split}
$$

Por lo tanto, la solución general del sistema de ecuaciones diferenciales es:

$$
\begin{split}
    & Y_{SGEH} = C_{1}v_{1}e^{(5+2i)t} + C_{2}v_{2}e^{(5-2i)t} =\\
\end{split}
$$

Si escogemos $C_{1} = a+bi$ y $C_{2}= a-bi$ se simplifica la solución general:

$$
\begin{split}
    & Y_{SGEH} = z + \hat{z} = 2\Re\{z\} = 2\Re\{C_{1}v_{1}e^{(5+2i)t} + C_{2}v_{2}e^{(5-2i)t}\} =\\ 
    &  = 2\Re\left[\begin{pmatrix}
        a+bi\\
        (a+2b)+(b-2a)i
    \end{pmatrix}e^{5t}e^{2ti}\right] =\\
    & = 2e^{5t}\Re\left[\begin{pmatrix}
        a+bi\\
        (a+2b)+(b-2a)i 
    \end{pmatrix}(\cos(2t) + i\sin(2t))\right] = 2e^{5t}\begin{pmatrix}
        a\cos(2t) - b\sin(2t)\\
        (a+2b)\cos(2t) - (b-2a)\sin(2t)
    \end{pmatrix} =\\
    & 2e^{5t}\begin{pmatrix}
        C_{1}\cos(2t) + C_{2}\sin(2t)\\
        (C_{1}-2C_{2})\cos(2t) + (2C_{1}+C_{2})\sin(2t)
    \end{pmatrix}
\end{split}
$$

Si lo escribimos en forma de sistema de ecuaciones:

$$
\begin{split}
    & Y_{SGEH} = \begin{cases}
        y_{1}(t) = 2e^{5t}(C_{1}\cos(2t) + C_{2}\sin(2t))\\
        y_{2}(t) = 2e^{5t}((C_{1}-2C_{2})\cos(2t) + (2C_{1}+C_{2})\sin(2t))
\end{split}
$$
