---
id: 1709730404-ejercicio-6-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 6 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Obtén la solución general de la [[1706869334-ecuacin-diferencial|ecuación]] $yy''+ (y')^2 = 0$

Falta $x \to$ Reducible tipo 2

$$
\begin{split}
    & y' = u \implies y'' = \frac{dy'}{dx} = \frac{du}{dx} = \\
    & = \frac{du}{dy}  \cdot \frac{dy}{dx} = \frac{du}{dy} \cdot u\\
    & y \cdot y'' + (y')^2 = 0 \implies y \cdot u \cdot \frac{du}{dy} + u^2 = 0 \implies \\
    & \implies y \cdot u \cdot \frac{du}{dy} = -u^2 \implies \int  \frac{1}{u}du = \int  - \frac{1}{y} dy\\
    & \ln |{u}| = -\ln |{y}| + C_1 \implies |{u}| = C_2 \cdot \frac{1}{|{y}|} \implies u = \frac{C_3}{y}\\
    & y' = u \implies y' = \frac{C_3}{y} \implies \frac{dy}{dx} = \frac{C_3}{y} \implies\\
    & \implies \int  y dy = \int C_3 dx \implies \frac{y^2}{2} = C_3 x + C_y \implies\\
    & \implies y^2 = K_1 \cdot x + K_2, \;\; k_1, \; k_2 \int \mathbb{R}
\end{split}
$$
