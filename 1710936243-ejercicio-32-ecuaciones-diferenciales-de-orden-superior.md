---
id: 1710936243-ejercicio-32-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 32 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Obtén una solución particular de la ecuación $xy''' - y'' - xy' + y = 8x^2e^{x}$ sabiendo que $y_{1} = x, \; y_{2} = e^{x}$ e $y_{3} = e^{-x}$ son tres soluciones particulares de la ecuación homogénea.

$$
\begin{split}
    & \mathcal{W}(y_{1},y_{2},y_{3}) =
    \begin{vmatrix}
        y_{1} & y_{2} & y_{3}\\
        y_{1}' & y_{2}' & y_{3}'\\
        y_{1}'' & y_{2}'' & y_{3}''
    \end{vmatrix} =
    \begin{vmatrix}
        x & e^{x} & e^{-x}\\
        1 & e^{x} & -e^{-x}\\
        0 & e^{x} & e^{-x}
    \end{vmatrix} = 2x \neq 0 \quad \forall x \neq 0\\
    & y_{SGEH} = C_{1}x + C_{2}e^{x} + C_{3}e^{-x}\\
    & y = C_{1}(x)x + C_{2}(x)e^{x} + C_{3}(x)e^{-x}\\

    & \begin{cases}
        & C_{1}'(x)y_{1}(x) + C_{2}'(x)y_{2}(x) + C_{3}'(x)y_{3}(x) = 0\\
        & C_{1}'(x)y_{1}'(x) + C_{2}'(x)y_{2}'(x) + C_{3}'(x)y_{3}'(x) = 0\\
        & C_{1}'(x)y_{1}''(x) + C_{2}'(x)y_{2}''(x) + C_{3}'(x)y_{3}''(x) = \frac{8x^{2}e^{x}}{2x} = 4x e^{x}\\
    \end{cases} \implies\\
    & \implies \begin{cases}
        & C_{1}'(x)x + C_{2}'(x)e^{x} + C_{3}'(x)e^{-x} = 0\\
        & C_{1}'(x) + C_{2}'(x)e^{x} - C_{3}'(x)e^{-x} = 0\\
        & C_{1}'(x) \cdot 0 + C_{2}'(x)e^{x} - C_{3}'(x)e^{-x} = 8xe^{x} 
    \end{cases} \implies\\
    & \implies \begin{cases}
        & C_{1}'(x)x = -8xe^{x} \implies C_{1}'(x) = -8e^{x} \implies C_{1}(x) = -8e^{x} + C_{1}\\
        & C_{1}'(x)(x+1) + 2C_{2}'(x)e^{x} = 0 \implies C_{2}'(x)  = 4x + 4 \implies C_{2}(x) = 2x^{2} + 4x + C_{2}\\
        & C_{3}'(x) = (4x-4)e^{2x} \implies C_{3}(x) = (2x-3)e^{2x} + C_{3}   
    \end{cases} \implies\\
    & \implies y = C_{1}(x)x + C_{2}(x)e^{x} + C_{3}(x)e^{-x} = (-8e^{x} + C_{1} )x + (2x^{2} + 4x + C_{2})e^{x} + ((2x-3)e^{2x} + C_{3})e^{-x} =\\
    & = C_{1}x + C_{2}x + C_{3}e^{-x} + (2x^2-2x-3)e^{x}  
\end{split}
$$



