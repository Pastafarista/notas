---
id: 1710936971-ejercicio-33-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 33 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Halla la ecuación diferencial de la familia de elipses con centro en el origen y cuyos ejes coinciden con los ejes coordenados.

$$
\begin{split}
    & \frac{x^2}{a^2} + \frac{y^2}{b^2} = 1 \implies bx^2 +a^2y^2 = a^2b^2 \implies\\
    & \implies 2bx + a^22yy^2=0 \implies 2b^2 2a^2((y')^2 +y\cdot y'') = 0\\
    & \begin{cases}
        & \frac{b^2}{a^2}x + 2y \cdot  y' = 0 \implies \frac{b^2}{a^2} = \frac{-y\cdot y'}{x}\\

        & \frac{b^2}{a^2} + (y')^2 + y \cdot  y'' = 0
    \end{cases} \implies\\
    & \implies \frac{-y \cdot  y''}{x} + (y')^2 + y\cdot y'' = 0 \implies y'' = \frac{1}{x}\cdot y' - \frac{1}{y}(y')^2
\end{split}
$$


