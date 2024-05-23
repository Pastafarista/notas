---
id: 1708521857-ejercicio-25-ecuaciones-diferenciales-de-primer-orden
aliases:
  - Ejercicio 25 ecuaciones diferenciales de primer orden
  - Resuelve la ecuación diferencial $y' = y^2 -2xy +1 + x^2$
tags:
  - ecuaciones-diferenciales
---

# Resuelve la [[1706869334-ecuacin-diferencial|ecuación diferencial]] $y' = y^2 -2xy +1 + x^2$

$$\begin{split}
    & p(x) = 1\\
    & q(X) = -2x\\
    & r(x) = x^2 + 1\\
\end{split}$$

$y=x$ es una [[1707058998-solucin-de-una-ecuacin-diferencial-ordinaria|solución]] específica $\implies y = x + \frac{1}{u}$

$$\begin{split}
    & y = x + \frac{1}{u} \implies y' = 1 - \frac{u'}{u^2}\\
    & y' = y^2 -2xy +1 +x^2 \implies \left( 1 - \frac{u'}{u^2}\right) = \left(x+ \frac{1}{u}\right)^2 - 2x\left(x + \frac{1}{u}\right) + 1 + x^2 \implies\\
    & \implies 1 - \frac{u'}{u^2} = x^2 + 2 \frac{x}{u} + \frac{1}{u^2} - 2x^2 - \frac{2x}{u} + 1 + x^2 \implies \frac{u'}{u^2} = \frac{-1}{u^2} \implies\\
    & \implies u' = -1 \implies u = -x + c\\
\end{split}$$

Ahora deshacemos el cambio de variable:

$$\begin{split}
    & y = x + \frac{1}{u} \implies y = x + \frac{1}{-x+C} \implies (y-x)(-x+C) = 1\\
\end{split}$$
