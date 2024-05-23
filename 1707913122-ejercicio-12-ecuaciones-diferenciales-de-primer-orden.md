---
id: 1707913122-ejercicio-12-ecuaciones-diferenciales-de-primer-orden
aliases:
  - Ejercicio 12 ecuaciones diferenciales de primer orden
  - Resuelve la ecuación diferencial ${(y^3 - kxy^4 - 2x)dx + (3xy^2 + 2y)dy = 0}$
  - Resuelve la ecuación diferencial ${(y^3 - kxy^4 - 2x)dx + (3xy^2 + 2y)dy = 0}$ eligiendo un valor de $k$ para que la ecuación sea diferencial exacta
tags:
  - ecuaciones-diferenciales
---

# Resuelve la [[1706869334-ecuacin-diferencial|ecuación diferencial]] ${(y^3 - kxy^4 - 2x)dx + (3xy^2 + 2y)dy = 0}$ eligiendo un valor de $k$ para que la ecuación sea [[1707912287-ecuaciones-diferenciales-exactas|diferencial exacta]]

$$\begin{split}
    & M(x,y) = y^3 - kxy^4 - 2x \;\;, N(x,y) = 3xy^2 + 2y\\
    & \frac{\partial M}{\partial y} = 3y^2 - 4kxy^3 \;\;, \frac{\partial N}{\partial x} = 3y^2 + 40xy^3\\
    & 3y^2 - 4kxy^3 = 3y^2 + 40xy^3 \implies -4kxy^3 = 40xy^3 \implies -4k = 40 \implies k = -10
\end{split}$$

Por lo tanto, la ecuación diferencial es exacta para $k = -10$. Ahora resolvemos la ecuación:

$$\begin{split}
    & (y^3 + 10xy^4 - 2x)dx + (3xy^2 + 20x^2y^3)dy = 0\\
    & \frac{\partial F(x,y)}{\partial x} = M(x,y) \implies F(x,y) = \int M(x,y)dx + C(y)\\
    & \implies F(x,y) = \int (y^3 + 10xy^4 - 2x)dx + C(y) = x^2y^3 + 5x^2y^4 - x^2 + C(y)\\
    & \frac{\partial F(x,y)}{\partial y} = N(x,y) \implies 3x^2y^2 + 20x^2y^3 + C'(y) = 3xy^2 + 20x^2y^3 \implies \\
    & \implies C'(y) = 0 \implies C(y) = C \implies F(x,y) = xy^3 + 5x^2y^4 - x^2 + C
\end{split}$$

