---
id: 1716908018-ejercicio-10-tema-4-ecuaciones-diferenciales
aliases:
  - Ejercicio inventado ecuaciones diferenciales tema 4
tags:
  - ecuaciones-diferenciales
---

# Resuelve el siguiente sistema de ecuaciones diferenciales:

$$
Y' = \begin{pmatrix}
    3 & 1\\
    -1 & -1
\end{pmatrix}Y
$$

Sacamos los autovalores asociados a la matriz de coeficientes:

$$
\begin{split}
    & det(A-\lambda I) = 0 \Longleftrightarrow \\
    & \Longleftrightarrow det\left(\begin{pmatrix}
        3-\lambda & 1\\
        -1 & -1-\lambda
    \end{pmatrix}\right) = 0 \Longleftrightarrow \\
    & \implies \lambda_{1} = 1 + \sqrt{3} \quad \lambda_{2} = 1 - \sqrt{3} 
\end{split}
$$

Calculamos los autovectores asociados a los autovalores:

- Para $\lambda_{1} = 1 + \sqrt{3}$:

$$
\begin{split}
    & S_{\lambda = 1 + \sqrt{3}} = \left( \begin{array}{cc|c}
        3 - (1 + \sqrt{3}) & 1 & 0\\
        -1 & -1 - (1 + \sqrt{3}) & 0
    \end{array}\right) \sim
    \left( \begin{array}{cc|c}
        2 - \sqrt{3} & 1 & 0\\
        -1 & -2 - \sqrt{3} & 0
    \end{array}\right) \sim \left( \begin{array}{cc|c}
        1 & 2 + \sqrt{3}  & 0\\
        0 & 0 & 0
    \end{array}\right) = \{((-2 - \sqrt{3})y,y) : y \in \mathbb{R} \} \implies\\
    & B_{S_{\lambda = 1 + \sqrt{3}}} = \left\{ \begin{pmatrix}
        2 + \sqrt{3}\\
        -1
    \end{pmatrix} \right\}
\end{split}
$$

- Para $\lambda_{2} = 1 - \sqrt{3}$:

$$
\begin{split}
    & S_{\lambda = 1 - \sqrt{3}} = \left( \begin{array}{cc|c}
        3 - (1 - \sqrt{3}) & 1 & 0\\
        -1 & -1 - (1 - \sqrt{3}) & 0
    \end{array}\right) \sim
    \left( \begin{array}{cc|c}
        2 + \sqrt{3} & 1 & 0\\
        -1 & -2 + \sqrt{3} & 0
    \end{array}\right) = \left( \begin{array}{cc|c}
        1 & 2 - \sqrt{3}  & 0\\
        0 & 0 & 0
    \end{array}\right) = \{((-2 + \sqrt{3})y,y) : y \in \mathbb{R} \} \implies\\
    & B_{S_{\lambda = 1 - \sqrt{3}}} = \left\{ \begin{pmatrix}
        2 - \sqrt{3}\\
        -1
    \end{pmatrix} \right\}
\end{split}
$$

Por lo tanto, la solución general del sistema de ecuaciones diferenciales es:

$$
\begin{split}
    & Y_{SGEH} = C_{1}e^{(1 + \sqrt{3})t}\begin{pmatrix}
        2 + \sqrt{3}\\
        -1
    \end{pmatrix} + C_{2}e^{(1 - \sqrt{3})t}\begin{pmatrix}
        2 - \sqrt{3}\\
        -1
    \end{pmatrix}
\end{split}
$$

En forma de sistema de ecuaciones:

$$
Y_{SGEH} = \begin{cases}
    x(t) = C_{1}e^{(1 + \sqrt{3})t}(2 + \sqrt{3}) + C_{2}e^{(1 - \sqrt{3})t}(2 - \sqrt{3})\\
    y(t) = -C_{1}e^{(1 + \sqrt{3})t} - C_{2}e^{(1 - \sqrt{3})t}
\end{cases}
$$
