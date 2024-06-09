---
id: 1710154940-ejercicio-15-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 15 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Resuelve la ecuación ${x^2y'' - 3xy' + 3y = 0}$

$$
\begin{split}
    & y = x^{m} \implies y' = mx^{m-1} \implies y'' = m(m-1)x^{m-2}\\
    & x^2y'' - 3xy' + 3y = 0\implies\\
    & \implies x^2m(m-1)x^{m-2} - 3xmx^{m-1} 3x^{m}=0\implies\\
    & \implies x^{m}(m^2 - m - 3m + 3)  = 0 \implies x^{m}(m^2 - 4m + 3) = 0 \implies\\
    & \implies m^2 - 4m + 3 = 0 \implies
    \begin{cases}
        & m = 1\\
        & m = 3
    \end{cases}\\
    & y = C_{1}x + C_{2}x^{3} \implies y' = C_{1} + 3C_{2}x^2 \implies y'' = 6C_{2}x\\
    & \mathcal{W}(y_{1},y_{2}) =
    \begin{vmatrix}
        y1 & y2\\
        y1' & y2'
    \end{vmatrix} =
    \begin{vmatrix}
        x^{m1} & x^{m_{2}}\\
        m_{1}x^{m_{1}-1} & m_{2}x^{m_{2}-1}  
    \end{vmatrix}
    = m_{2}x^{m_{1}}x^{m_{2} - 1} - m_{1}x^{m_{1} - 1} x^{m_{2}} =\\
    & = m_{2}x^{m_{1} + m_{2} - 1} - m_{1}x^{m_{1} + m_{2} -1} =\\
    & = (m_{1} - m_{2})x^{m_{1} + m2 - 1} \neq 0 \text{ si } m_{1} \neq m_{2}
\end{split}
$$
