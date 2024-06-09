---
id: 1709729669-ejercicio-5-ecucaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 5 ecucaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Obtén la solución general de la [[1706869334-ecuacin-diferencial|ecuación]]  ${y''= 2x(y')^2}$

$$\begin{split}
    & y' = u \implies  y'' = u\\
    & y'' = 2x(y')^2 \implies u' = 2x \cdot u ^2 \implies\\
    & \implies \frac{du}{dx} = 2xu^2 \implies \int \frac{1}{u^2}du = \int 2x dx \implies \\
    & \implies -\frac{1}{u} = x^2 + C_1 \implies u = - \frac{1}{x^2 + C_1}\\
    & y'= u \implies y' = - \frac{1}{x^2 + C_1} \implies y = -\int \frac{1}{x^2 + C_1}dx\\
    & \text{Si } C_1 > 0 \implies y = - \int  \frac{1}{x^2 + C_1} \implies y - \frac{1}{\sqrt{C_1}} arctg \left(\frac{x}{\sqrt{C_1}}\right) + C_2\\
    & \text{Si } C_1 < 0 \implies y = -\int  \frac{1}{x^2 - \|{C_1}|}dx = - \int \frac{1}{(x + \sqrt{|{C_1}|} )(x - \sqrt{|{C_1}|} )}dx =\\
    & = - \int \left( \frac{\frac{1}{2}}{x - \sqrt{|{C_1}|} } - \frac{\frac{1}{2}}{x + \sqrt{|{C_1}|} } \right) dx =\\
    & = \ldots = \ln  \left( \sqrt{\frac{x + \sqrt{|{c_1}|} }{x - \sqrt{|{C_1}|} }}  \right) + C_2\\
\end{split}$$

$$\begin{split}
    & y' = 2 \implies y = 2x + C_1\\
    & y' = 2x \implies y = x^2 + C_2\\
    & (y' -2)(y' -2x)=0 \implies (y')^2 - y' (2 + 2x) + 4x = 0
\end{split}$$
