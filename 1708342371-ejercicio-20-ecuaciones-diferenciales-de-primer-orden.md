---
id: 1708342371-ejercicio-20-ecuaciones-diferenciales-de-primer-orden
aliases:
  - Ejercicio 20 ecuaciones diferenciales de primer orden
  - Resuelve el problema del valor inicial $\begin{cases}& (x^2 + 1)y' + 4xy = x\\ & y(x) = 1\end{cases}$
tags:
  - ecuaciones-diferenciales
---

# Resuelve el problema del valor inicial $\begin{cases}& (x^2 + 1)y' + 4xy = x\\ & y(x) = 1\end{cases}$

$$\begin{split}
    & {(x^2 + 1)y' + 4xy = x \implies y' + \frac{4x}{x^2 + 1}y = \frac{x}{x^2 + 1}}\\
    & P(x) = \frac{4x}{x^2 +1}\\
    & r(x) = \frac{x}{x^2 +1}\\
\end{split}$$

Para resolver la [[1706869334-ecuacin-diferencial|ecuación diferencial]] usaremos el método del factor integrante


1. Buscamos un factor integrante

$$\begin{split}
    & \mu(x) = e^{\int P(x)dx} = e^{\int \frac{4x}{x^2 + 1}dx} = e^{2ln|x^2 + 1|} = (x^2 + 1)^2\\
\end{split}$$

2. Usamos el factor integrante para resolver la ecuación

$$\begin{split}
    & y' + \frac{4x}{x^2 + 1}y = \frac{x}{x^2 + 1} \implies (x^2 + 1)^2 y' + 4x(x^2 + 1)y = x(x^2 + 1) \implies\\
    & \implies (4xy(x^2 +1) - x(x^2 +1))dx + (x^2 +1)^2dy = 0 \implies\\
    & \implies \frac{\partial F(x,y)}{\partial y} = Q(x,y) \implies F(x,y) = \int Q(x,y)dy + C(x) = \int(x^2 + 1)dy + C(x) = (x^2 + 1)^2y + C(x)\\
    & \frac{\partial F(x,y)}{\partial x} = P(x,y) \implies 4x(x^2 + 1)y+ C'(x) = 4x^3 y + 4xy - x^3 - x \implies \\
    & \implies 4x^3 y + 4xy + C'(x) = 4x^3y + 4xy - x^3 -x \implies\\
    & \implies C(x) = \frac{-x^4}{4} - \frac{x^2}{2} + C\\
    & F(x,y) = (x^2 + 1)^2 y - \frac{x^4}{4} - \frac{x^2}{2} + C = 0\\
\end{split}$$

3. Sacamos la [[1707058998-solucin-de-una-ecuacin-diferencial-ordinaria|solución]] particular

$$y(2) = 1 \implies \cdots \implies C=-19$$
