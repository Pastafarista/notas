---
id: 1707912664-ejercicio-11-ecuaciones-diferenciales-de-primer-orden
aliases:
  - Ejercicio 11 ecuaciones diferenciales de primer orden
  - "Determina la solución general de la siguiente ecuación: $(3x^2 + 4xy)dx + (2x^2 +2y)dy = 0$"
tags:
  - ecuaciones-diferenciales
---

# Determina la [[1707058998-solucin-de-una-ecuacin-diferencial-ordinaria|solución general]] de la siguiente ecuación: $(3x^2 + 4xy)dx + (2x^2 +2y)dy = 0$

Primero vamos a ver si es una ecuación de tipo [[1707912287-ecuaciones-diferenciales-exactas|diferencial exacta]]

$$\begin{split}
    & M(x,y) = 3x^2 + 4xy \;\;, N(x,y) = 2x^2 + 2y\\
    & \frac{\partial M}{\partial y} = 4x \;\;, \frac{\partial N}{\partial x} = 4x\\
    & \implies \text{Es exacta}
\end{split}$$

Ahora resolvemos la ecuación:

$$\begin{split}
    & \frac{\partial F(x,y)}{\partial x} = M(x,y) \implies F(x,y) = \int M(x,y)dx + C(y)\\
    & \implies F(x,y) = \int (3x^2 + 4xy)dx + C(y) = x^3 + 2x^2y + C(y)\\
    & \frac{\partial F(x,y)}{\partial y} = N(x,y) \implies 2x^2 + C'(y) = 2x^2 + 2y \implies \\
    & \implies C'(y) = 2y \implies C(y) = y^2 + C\\
\end{split}$$
