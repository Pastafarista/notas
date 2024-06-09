---
id: 1707129199-ejercicio-11-ecuaciones-diferenciales
aliases:
  - Ejercicio 11 ecuaciones diferenciales
  - Aplica el teorema de existencia y unicidad para resolver la ecuación diferencial $y'=y^{1/3}$, determinando los recintos del plano donde se puede asegurar que en cada punto pase una única solución.
tags:
  - ecuaciones-diferenciales
---

# Aplica el [[1707127934-teorema-de-existencia-y-unicidad-para-ecuaciones-de-primer-orden|teorema de existencia y unicidad]] para resolver la [[1706869334-ecuacin-diferencial|ecuación diferencial]] $y'=y^{1/3}$, determinando los recintos del plano donde se puede asegurar que en cada punto pase una única solución.

$$
\begin{split}
    & y' = y^{1/3} \\
    & y' = f(x,y) \implies f(x,y) = y^{1/3} \text{ continua } \forall (x,y) \in \mathbb{R}^2\\
    & \frac{d f(x,y)}{d y} = \frac{1}{3} y^{-2/3} \text{ continua } \forall (x,y) \in \mathbb{R}^2 - \{(x,y) \in \mathbb{R}^2 \mid y = 0\}\\
    & y' = y^{1/3} \implies \frac{d y }{d x} = y^{1/3} \implies \\
    & \implies \frac{1}{y^{1/3}} d y = d x \implies \int \frac{1}{y^{1/3}} d y = \int d x \implies \\
    & \implies x = \frac{3}{2} y^{2/3} + C \implies y = \left(\frac{2}{3} x \right)^{3/2} \text{ S.P.} \mid y=0\\
\end{split}
$$
