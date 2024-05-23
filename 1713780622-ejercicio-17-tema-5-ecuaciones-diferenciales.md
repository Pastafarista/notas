---
id: 1713780622-ejercicio-17-tema-5-ecuaciones-diferenciales
aliases:
  - Ejercicio 17 tema 5 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Analiza el modelo presa-depredador de Lotka-Volterra dado por el siguiente sistema de ecuaciones desde un punto de vistas cualitativo:

$$
\begin{cases}
    & x' = x - 2xy\\
    & y' = -4y + 2xy
\end{cases}
$$

$$
\begin{split}
    & \begin{array}
        & x - 2xy = 0\\
        & -4y + 2xy = 0
    \end{array} \implies

    \begin{array}
        & x = 0\\
        & x = 2
        & y = 0\\
        & y = \frac{1}{2}
    \end{array} 
\end{split}
$$

Tenemos los puntos $(0,0)$ y $(2,\frac{1}{2})$

Estudiemos la estabilidad de $(0,0)$:

$$
\begin{split}

    & \begin{array}
        & g_{1}(x,y) = x - 2xy\\
        & g_{2}(x,y) = -4y + 2xy
    \end{array} \implies

    J_g(x,y) = \begin{pmatrix} 
        \frac{\partial g_{1}}{\partial x} & \frac{\partial g_{1}}{\partial y}\\
        \frac{\partial g_{2}}{\partial x} & \frac{\partial g_{2}}{\partial y}
    \end{pmatrix} =\\

    & \begin{pmatrix}
        1 - 2y & -2x\\
        2y & (2x - 4)
    \end{pmatrix}\\

    & J_g(0,0) = \begin{pmatrix}
        1 & 0\\
        0 & -4
    \end{pmatrix} \implies \ldots \implies \lambda = 1, -4

\end{split}
$$

Por lo tanto, $(0,0)$ es de tipo silla inestable. Sus autovectores son: $B_{S_{\lambda = 1}} = \{(1,0)\}$ y $B_{S_{\lambda = 4}} = \{(0,1)\}$. Ahora intentaremos sacar las trayectorias que pasan por $(2, \frac{1}{2})$:

$$
J_g(2,\frac{1}{2}) = \begin{pmatrix}
    -1 & -2\\
    1 & 0
\end{pmatrix} \implies \ldots \implies \lambda = \pm 2i
$$

Por lo tanto, $(2,\frac{1}{2})$ es de tipo centro inestable. Sus autovectores son: $B_{S_{\lambda = 2i}} = \{(1,2)\}$ y $B_{S_{\lambda = -2i}} = \{(1,-2)\}$.

Ahora intentaremos sacar las trayectorias que pasan por $(2, \frac{1}{2})$:

$$
\begin{split}
    & \frac{dy}{dx} = \frac{-4y + 2xy}{x - 2xy} \implies \ldots \implies \frac{x^{4}y }{e^{2x + 2y} } = C
\end{split}
$$

