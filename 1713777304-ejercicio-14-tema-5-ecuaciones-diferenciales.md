---
id: 1713777304-ejercicio-14-tema-5-ecuaciones-diferenciales
aliases:
  - Ejercicio 14 tema 5 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Determina los puntos críticos del siguiente sistema y analiza su estabilidad o inestabilidad:

$$
\begin{split}
    & \begin{cases}
        & x' = x - xy\\
        & y' = x - y
    \end{cases}\\

    & \begin{array}
        & x - xy = 0\\
        & x -y = 0
    \end{array} \rightarrow 

    \begin{array}
        & x(1 - y) = 0\\
        & x = y
    \end{array} \rightarrow 

    \begin{array}
        & (0, 0)\\
        & (1, 1)
    \end{array}\\

    & \begin{array}
        & g_{1}(x,y) = x - xy\\
        & g_{2}(x,y) = x - y
    \end{array} \rightarrow

    J_g(x,y) =

    \begin{pmatrix}
        \frac{\partial g_{1}}{\partial x} & \frac{\partial g_{1}}{\partial y}\\
        \frac{\partial g_{2}}{\partial x} & \frac{\partial g_{2}}{\partial y}
    \end{pmatrix} =\\

    & \begin{pmatrix}
        (1 - y) & -x\\
        1 & -1
    \end{pmatrix} \implies
    J_g(0,0) = \begin{pmatrix}
        1 & 0\\
        1 & -1
    \end{pmatrix}\\
    & J_g(1,1) = \begin{pmatrix}
        0 & -1\\
        1 & -1
    \end{pmatrix}
\end{split}
$$

Ahora sacamos los autovalores de $J_g(0,0)$:

$$
\begin{split}
    & |J_g(0,0) - \lambda I| = 0 \implies \begin{array} & \lambda = 1\\ \lambda = -1 \end{array}\\
    & S_{\lambda = 1} =  \{(2,1)\} \\
    & S_{\lambda = -1} = \{(0,1)\}
\end{split}
$$

Es inestable y de tipo silla.

$$
\begin{split}
    & \binom{x}{y} = C_{1}\binom{2}{1}e^{\lambda_{1}t} + C_{2}\binom{0}{1}e^{\lambda_{2}t}\\
    & \binom{x}{y} = C_{1}\binom{2}{1}e^{t} + C_{2}\binom{0}{1}e^{-t}
\end{split}
$$

Para $(1,1)$:

$$
\begin{cases}
    & x' = -y\\
    & y' = x-y
\end{cases} \rightarrow A = \begin{pmatrix} 0 & -1\\ 1 & -1 \end{pmatrix} \implies |A - \lambda I| = 0 \implies \begin{array} & \lambda = -\frac{1}{2} + i\frac{\sqrt{3}}{2}\\ \lambda = -\frac{1}{2} - i\frac{\sqrt{3}}{2} \end{array}
$$

Se trata de una espiral estable

