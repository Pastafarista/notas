---
id: 1713779854-ejercicio-16-tema-5-ecuaciones-diferenciales
aliases:
  - Ejercicio 16 tema 5 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Determina los puntos críticos del siguiente sistema y analiza su estabilidad o inestabilidad:

$$
\begin{cases}
    & x' = y^2 - 3y + 2\\
    & y' = (1-x)(y-2)
\end{cases}
$$

$$
\begin{split}
    & \begin{array}
        & y^2 - 3y + 2 = 0\\
        & (1-x)(y-2) = 0
    \end{array} \implies

    \begin{array}
        & x = 1\\
        & y = 1
        & y = 2
    \end{array} \implies
\end{split}
$$

Tenemos $(1,1)$ y la recta $y=2$, estudiemos la estabilidad de $(1,1)$:

$$
\begin{split}

    & \begin{array}
        g_{1}(x,y) & = y^2 - 3y + 2\\
        g_{2}(x,y) & = (1-x)(y-2)
    \end{array} \implies

    J_g(x,y) = \begin{pmatrix} 
        \frac{\partial g_{1}}{\partial x} & \frac{\partial g_{1}}{\partial y}\\
        \frac{\partial g_{2}}{\partial x} & \frac{\partial g_{2}}{\partial y}
    \end{pmatrix} =\\

    & \begin{pmatrix}
        0 & 2y - 3\\
        2-y & 1-x
    \end{pmatrix}\\

    & J_g(1,1) = \begin{pmatrix}
        0 & -1\\
        1 & 0
    \end{pmatrix} \implies \ldots \implies \lambda = \pm i
\end{split}
$$

Por lo tanto, $(1,1)$ es de tipo centro inestable. Ahora intentaremos sacar las trayectorias que pasan por $(1,1)$:

$$
\begin{split}
    & \frac{dy}{dx} = \frac{(1-x)(y-2)}{(y-2)(y-1)} \implies\\
    & \implies (y-1)dy = -(x-1)dx \implies \ldots  \implies (x-1)^2+ (y-1)^2 = C
\end{split}
$$


