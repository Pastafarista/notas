---
id: 1708341158-ejercicio-18-ecuaciones-diferenciales-de-primer-orden
aliases:
  - Ejercicio 18 ecuaciones diferenciales de primer orden
  - Resuelve la ecuación ${(x^2 + 1)y' + 4xy = 0}$
tags:
  - ecuaciones-diferenciales
---

# Resuelve la ecuación ${(x^2 + 1)y' + 4xy = 0}$

La ecuación es [[1708333648-ecuacin-diferencial-lineal|lineal]] [[1708330960-ecuacin-diferencial-homognea|homogénea]] de primer [[1706869571-orden-ecuacin-diferencial|orden]], además es de [[1708330652-eucacin-diferencial-de-variable-separada|variable separada]]

$$\begin{split}
    & (x^2 + 1) \frac{dy}{dx} + 4xy = 0 \implies (x^2  + 1) \frac{dy}{dx} = -4xy \implies \\
    & \implies \frac{1}{y} dy = \frac{-4x}{x^2 + 1}dx \implies \int \frac{1}{y}dy = - \int \frac{4x}{x^2 + 1}dx \implies \\
    & \implies ln|y| = -2ln|x^2 + 1| + C_1 \implies e^{ln|y|} = e^{ln(x^2 + 1)^{-2}}e^{C_1} \implies \\
    & \implies |y| = \frac{1}{(x^2 + 1)^2}C_2 \implies y_{SGEH} = \frac{C}{(x^2 + 1)^2}
\end{split}$$
