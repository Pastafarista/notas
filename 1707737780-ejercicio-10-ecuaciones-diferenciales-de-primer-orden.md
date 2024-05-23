---
id: 1707737780-ejercicio-10-ecuaciones-diferenciales-de-primer-orden
aliases:
  - Ejercicio 10 ecuaciones diferenciales de primer orden
  - Resuelve la siguiente ecuación diferencial
  - Resuelve la siguiente ecuación diferencial 
tags:
  - ecuaciones-diferenciales
---

# Resuelve la siguiente [[1706869334-ecuacin-diferencial|ecuación diferencial]] 

$$
\begin{split}
    & (x + y - 1)dx + (2x + 2y -1)dy = 0 \implies \\
    & \implies y' = - \frac{x+y-1}{2x+2y-1} = f \left( \frac{x+y-1}{2x+2y-1} \right)\\
    & r: x + y -1 = 0 \;\; , s: 2x+2yy-1=0\\
    & u = ax + by = x + y \implies y = u - x \implies y' = u' - 1\\
    & y' = \frac{-(x+y-1)}{2x+2y-1} \implies u' - 1 = \frac{-(x + u - x - 1)}{2x + 2(u-x) - 1} \implies \\
    & \implies u' - 1 = \frac{1 - u}{2u - 1} \implies \frac{du}{dx} = \frac{1 - u}{2u - 1} + 1 \implies \\
    & \implies \frac{du}{dx} = \frac{1 - u + 2u - 1}{2u - 1} \implies \frac{du}{dx} = \frac{u}{2u - 1} \implies \\
    & \implies \frac{2u - 1}{u} du = dx \implies \int \left(2 - \frac{1}{u} \right)du = \int dx \implies \\
    & \implies 2u - \ln|u| = x + C \implies 2(y + x) - ln|y+x| = x + C \implies \\
    & \implies x + 2y - ln|y+x| = C, \;\; C \in \mathbb{R}
\end{split}
$$

$$
\begin{split}
    & u = 0 \implies y+x = 0 \implies y = -x \text{ ¿Solución de la ecuación?}\\
    & (x+y-1) + (2x-2y-1) \cdot y' = (x - x - 1) + (2x - 2x - 1)(-1) = 0 \implies \\
    & \implies y = -x \text{ es solución de la ecuación}
\end{split}
$$

$$
\begin{split}
    & x + 2(-x) - ln|-x + x| = C \implies C = -x - ln(0) !!!
\end{split}
$$
