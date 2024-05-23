---
id: 1708941999-ejercicio-27-ecuaciones-diferenciales-de-primer-orden
aliases:
  - Ejercicio 27 ecuaciones diferenciales de primer orden
  - Resuelve la ecuación $y = x y' - \frac{1}{y'}$
tags:
  - ecuaciones-diferenciales
---

# Resuelve la [[1706869334-ecuacin-diferencial|ecuación]] $(y')^2+xy'-y=0$

$$\begin{split}
    & (y')^2 +xy' - y = 0 \implies xy' + (y')^2\\
    & y = xy' + (y')^2 \implies y' = y' + xy'' + 2y' y'' \implies y''(x + 2y')=0\\ 
\end{split}$$

Opción 1:

$$\begin{split}
    & y'' = 0 \implies \begin{cases}
       & y' = C\\
        & y =xy' + (y')^2\\
    \end{cases} \implies y = Cx + C^2\\
    & \text{Solución general}
\end{split}$$

Opción 2:

$$\begin{split}
    & x+2y' = 0 \implies \begin{cases}
        & y' = -\frac{x}{2}\\
        & y = xy' + (y')^2\\
    \end{cases} \implies y = x \left( -\frac{x}{2} \right) + \left( -\frac{x}{2} \right)^2 = -\frac{x^2}{2} + \frac{x^2}{4} = -\frac{x^2}{4} \implies \\
    & \implies y = -\frac{x^2}{4}\\
    & \text{Solución singular}
\end{split}$$
