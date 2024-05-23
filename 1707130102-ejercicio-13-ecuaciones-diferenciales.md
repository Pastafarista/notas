---
id: 1707130102-ejercicio-13-ecuaciones-diferenciales
aliases:
  - Ejercicio 13 ecuaciones diferenciales
  - Determina la ecuación diferencial asociada a las siguientes soluciones generales
tags:
  - ecuaciones-diferenciales
---

# Determina la [[1706869334-ecuacin-diferencial|ecuación diferencial]] asociada a las siguientes [[1707058998-solucin-de-una-ecuacin-diferencial-ordinaria|soluciones generales]]

1. $y - 4x - C = 0$

$$y'- 4=0 \implies y' = 4$$

2. $y = C_1 e^x + C_2 e^{-x}$

$$y' = C_1 e^x - C_2 e^{-x} \implies y'' = C_1 e^x + C_2 e^{-x} \implies y'' = y \implies y'' - y = 0$$

3. $x^2 + C_1 y^2 = C_2 \text{ donde } C_1, C_2 > 0$

$$\begin{split}
    & 2x + 2C_1 y y' = 0 \implies 2 + 2C_1 ((y')^2 +y y'') = 0 \implies \\
    & \implies \begin{cases} & 2x + 2C_1 y y' = 0 \ \implies C_1 = \frac{-x}{y y'}\\ & 2 + 2C_1 ((y')^2 + y y''))=0 \ \implies C_1 = \frac{-1}{(y')^2 + y y''} \\ \end{cases} \implies\\
    & \implies \frac{-x}{y y'} = \frac{-1}{(y')^2 + y y''} \implies x ((y')^2 + y y'') = y y'
\end{split}$$
