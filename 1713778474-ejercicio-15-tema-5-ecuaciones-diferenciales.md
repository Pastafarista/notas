---
id: 1713778474-ejercicio-15-tema-5-ecuaciones-diferenciales
aliases:
  - Ejercicio 15 tema 5 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Determina los puntos críticos del siguiente sistema y analiza su estabilidad o inestabilidad:

$$
\begin{cases}
    & x' = 1 - xy\\
    & y' = x - y^3 
\end{cases}
$$

$$
\begin{split}
    & \begin{array}
        & 1 - xy = 0\\
        & x - y^3 = 0
    \end{array} \implies

    \begin{array}
        & x = \pm 1
        & y = \pm 1
    \end{array} \implies
\end{split}
$$

$$
\begin{split}
    & \begin{array}
        & g_{1}(x,y) = 1 - xy\\
        & g_{2}(x,y) = x - y^3
    \end{array} \implies
    J_g(x,y) = \begin{pmatrix} 
        \frac{\partial g_{1}}{\partial x} & \frac{\partial g_{1}}{\partial y}\\
        \frac{\partial g_{2}}{\partial x} & \frac{\partial g_{2}}{\partial y}
    \end{pmatrix} =\\
    & \begin{pmatrix}
        -y & -x\\
        1 & -3y^2
    \end{pmatrix}\\
    & J_g(1,1) = \begin{pmatrix}
        -1 & -1\\
        1 & -3
    \end{pmatrix}

    & J_g(-1,-1) = \begin{pmatrix}
        1 & 1\\
        1 & -3
    \end{pmatrix}
\end{split}
$$

Para $(1,1)$:

$$
\begin{split}
    & \begin{cases}
        & x' = -x - y\\
        & y' = x - 3y^2
    \end{cases}\\
    & A = \begin{pmatrix}
        -1 & -1\\
        1 & -3
    \end{pmatrix} \implies | A - \lambda I| = 0 \implies \begin{cases}
        & \lambda  = -2\\
        & \lambda = -2
    \end{cases}
\end{split}
$$

Entonces es de tipo tangente estable con autovector $B_{S_{\lambda = -2}} = \{(1,1)\}$

Para $(-1,-1)$:

$$
\begin{split}
    & \begin{cases}
        & x' = x + y\\
        & y' = x - 3y^2
    \end{cases}\\
    & A = \begin{pmatrix}
        1 & 1\\
        1 & -3
    \end{pmatrix} \implies | A - \lambda I| = 0 \implies \begin{cases}
    & \lambda  = -1 - \sqrt{5}  \\
    & \lambda = -1 + \sqrt{5}
    \end{cases}
\end{split}
$$

Entonces es de tipo silla inestable con autovectores $B_{S_{\lambda = -1 - \sqrt{5}}} = \{(2 - \sqrt{5}, 1 )\}$ y $B_{S_{\lambda = -1 + \sqrt{5}}} = \{(2 + \sqrt{5}, 1 )\}$

$$
\begin{split}
    & \binom{x}{y} = C_{1}\binom{2 - \sqrt{5} }{1}e^{-(1 + \sqrt{5} )t} + C_{2}\binom{2 + \sqrt{5}}{1}e^{(-1 + \sqrt{5} )t}
\end{split}
$$


