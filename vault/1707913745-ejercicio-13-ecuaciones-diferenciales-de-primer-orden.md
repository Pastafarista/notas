---
id: 1707913745-ejercicio-13-ecuaciones-diferenciales-de-primer-orden
aliases:
  - Ejercicio 13 ecuaciones diferenciales de primer orden
  - Resuelve la ecuación diferencial ${x(2x^2 + y^2)dx + y(x^2 + 2y^2)dy = 0}$
tags:
  - ecuaciones-diferenciales
---

# Resuelve la [[1706869334-ecuacin-diferencial|ecuación diferencial]] ${x(2x^2 + y^2)dx + y(x^2 + 2y^2)dy = 0}$

Primero vamos a ver si es una ecuación de tipo [[1707912287-ecuaciones-diferenciales-exactas|diferencial exacta]]

$$\begin{split}
    & M(x,y) = x(2x^2 + y^2) \;\;, N(x,y) = y(x^2 + 2y^2)\\
    & \frac{\partial M}{\partial y} = 2xy \;\;, \frac{\partial N}{\partial x} = 2xy\\
    & \implies \text{Es exacta}
\end{split}$$

Ahora resolvemos la ecuación:

$$\begin{split}
    & \frac{\partial F(x,y)}{\partial y} = N(x,y) \implies F(x,y) = \int N(x,y)dy + C(x)\\
    & \implies F(x,y) = \int (x^2y + 2y^3)dy + C(x) = \frac{x^2y^2}{2} + \frac{y^4}{2} + C(x)\\
    & \frac{\partial F(x,y)}{\partial x} = M(x,y) \implies xy^2 + C'(x) = 2x^3 + xy^2 \implies \\
    & \implies C'(x) = 2x^3 \implies C(x) = \frac{2x^4}{4} + C \implies F(x,y) = \frac{x^2y^2}{2} + \frac{y^4}{2} + \frac{x^4}{2} + C \implies\\
    & \implies F(x,y) = \frac{x^2y^2}{2} + \frac{y^4}{2} + \frac{x^4}{2} + C = 0 \implies x^2y^2 + y^4 + x^4 + K = 0\\
\end{split}$$

Vamos a comprobar que la solución es correcta:

$$\begin{split}
    & x^2y^2 + y^4 + x^4 + K = 0 \implies 2xy^2 + x^2 2y y' + 4y^3 y' + 4x^3 = 0 \implies\\
    & \implies (2x^2y + 4y^3)\frac{dx}{dy} + (2xy^2 + 4x^3) = 0 \implies (2xy^2 + 4x^3)dx + (2x^2y + 4y^3)dy = 0 \implies \int (2xy^2 + 4x^3)dx + \int (2x^2y + 4y^3)dy = 0\\
\end{split}$$
