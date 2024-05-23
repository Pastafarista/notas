---
id: 1709731010-ejercicio-7-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 7 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Sabiendo que $y_1(x)=e^x$ es una solución particular de la [[1706869334-ecuacin-diferencial|ecuación]] $y'' - y = 0$, obtén la solución general utilizando el método de reducción de orden

Es de reducible tipo 3

$$
\begin{split}
    & y = uy_1 \implies y = u \cdot e^x => y' = u' = u'\cdot e^x +  u \cdot e^x \implies y'' = u'' \cdot e^x + 2u' e^x + u \cdot e^x\\
    & y'' - y = 0 \implies u'' \cdot e^x + 2u' e^x + u e^x - u e^x = 0 \implies u'' \cdot e^x + eu' \cdot e^x = 0\\
\end{split}
$$

Falta $u$ por lo tanto usaremos el cambio $w = u'$

$$
\begin{split}
    & w = u' \implies w' = u''\\
    & u'' e^x + 2u' e^x = 0 \implies u'' + 2u' = 0 \implies w' + 2w = 0 \implies\\
    & \implies \frac{dw}{dx} = -2w \implies \int  \frac{1}{w} dw = - \int 2 dx \implies \\
    & \implies \ln \abs{w} = -2x + C_1 \implies \abs{w} = C_2 e^{-2x} \implies w = C_3 e^{-2x}\\
    & w = u' \implies u' = C_3 e^{-2x} \implies \frac{du}{dx} = C_3 \cdot e^{-2x} \implies \int du = \int C_3 e^{-2x}dx \implies \\
    & \implies u = - \frac{1}{2} C_3 e^{-2x} + C_4\\
    & y = u \cdot y_1 \implies y = u \cdot e^{x} \implies y = \left(- \frac{1}{2} C_3 e^{-2x} + C_y \right)e^x \implies\\
    & \implies y = - \frac{1}{2} \cdot C_3 e^{-x} + C_4 \cdot e^{x} \implies y = K_1 \cdot e^{-x} + K_2 \cdot e^{x}\;\; , K_1, K_2 \in \mathbb{R}
\end{split}
$$
