---
id: 1707132777-ejercicio-4-ecuaciones-diferenciales-primer-orden
aliases:
  - Ejercicio 4 ecuaciones diferenciales primer orden
  - Resuelve el proble de valor inicial $\begin{cases} & (x-4)y^4 dx - x^3 (y^2 - 3) dy = 0 \\ & y(1) = 1\end{cases}$
  - Resuelve el problema de valor inicial $\begin{cases} & (x-4)y^4 dx - x^3 (y^2 - 3) dy = 0 \\ & y(1) = 1\end{cases}$
tags:
  - ecuaciones-diferenciales
---

# Resuelve el problema de valor inicial $\begin{cases} & (x-4)y^4 dx - x^3 (y^2 - 3) dy = 0 \\ & y(1) = 1\end{cases}$

$$
\begin{split}
    & (x-4)y^4 dx - x^3 (y^2 - 3) dy = 0 \implies (x-4)y^4 dx = x^3 (y^2 - 3) dy \implies \\
    & \implies \left(\frac{x-4}{x^3}\right) dx = \left(\frac{y^2 - 3}{y^4}\right) dy \implies \\
    & \implies (x^{-2} - 4x^{-3}) dx = (y^{-2} - 3y^{-4}) dy \implies \\
    & \implies \int (x^{-2} - 4x^{-3}) dx = \int (y^{-2} - 3y^{-4}) dy \implies -x^{-1} + 2x^{-2} = -y^{-1} + y^{-3} + C \implies \\
    & \implies \frac{1}{x} - \frac{2}{x^2} - \frac{1}{y} + \frac{1}{y^3} = C \implies \frac{1}{x} - \frac{1}{y} - \frac{2}{x^2} + \frac{1}{y^3} + C = 0 \\
    & y(1) = 1 \implies ... \implies \frac{1}{1} - \frac{2}{1^2} - \frac{1}{1} + \frac{1}{1^3} + C = 0 \implies C = 1
\end{split}
$$

$y = 0 \text{ es una solución singular}$
