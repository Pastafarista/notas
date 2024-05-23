---
id: 1709731645-ejercicio-8-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 8 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Sabiendo que $y_1(x)=x^{-2}$ es una solución particular de la [[1706869334-ecuacin-diferencial|ecuación]] ${x^2y'' - 7xy' -20y = 0}$, obtén la solución general mediante el método de reducción de orden

Es de reducible tipo 3

$$
\begin{split}
    & y = u \cdot y_1 \implies y = u \cdot  \frac{1}{x^2} - \frac{2u}{x^3} \implies y' = u' \cdot x^{-2} - 2u \cdot x^{-3} \implies\\
    & \implies y'' = u'' \cdot x^{-2} - 2u' \cdot x^{-3} - 2u'x^{-3} + 6u x^{-4} \implies y'' = u'' \cdot x^{-2} - 4u' x^{-3} + 6ux^{-4}\\
    & x^2 \cdot y'' - 7xy' -20y = 0 \implies x^2 (u'' \cdot x^{-2} - 4u' \cdot x^{-3} + 6ux^{-4}) - 7x(u' \cdot x^{-2} - 2u x^{-3}) -20 \cdot u \cdot x^{-2} = 0 \implies\\
    & \implies \ldots  \implies u'' - 11 \cdot u' + x^{-1} = 0 \implies u'' - \frac{11 \cdot u'}{x} = 0
\end{split}
$$

Falta $u$ por lo tanto usaremos el cambio $w = u'$

$$
\begin{split}
    & w = u' \implies w' = u''\\
    & u'' - \frac{11}{x}u' = 0 \implies w' - \frac{11}{x} \cdot w = 0 \implies \frac{dw}{dx} = \frac{11}{x} \cdot w \implies \\
    & \implies \frac{1}{w} dw = \int  \frac{11}{x} dx \implies \ln  \abs{w} = 11 \cdot \ln  \abs{x} + C_1 \implies \abs{w} = C_2 \cdot \abs{x}'' \implies w = C_3 \cdot x''\\
    & u' = w \implies u' = C_3 \cdot x'' \implies \frac{du}{dx} = C_3 x'' \implies u = C_3 \cdot \frac{x^{12}}{12}  +C_4\\
    & y = u \cdot y_1 \implies y = \left(C_3 \cdot \frac{x^12}{12} + C_4 \right) \cdot \frac{1}{x^2} \implies y = K_1 \cdot x^{10} + K_2 \cdot x^{-2} \;\; , K_1, K_2 \in \mathbb{R}
\end{split}
$$
