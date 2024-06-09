---
id: 1710155503-ejercicio-16-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 16 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Resuelve la ecuación ${x^2y'' + 3xy' + y = 0}$

$$
\begin{split}
    &  y = x^{m} \implies y' = m \cdot  m^{m-1} \implies y'' = m(m-1)x^{m-2}\\
    & x^2y'' + 3xy' + y = 0 \implies x^2m(m-1)x^{m-2} + 3x\cdot mx^{m-1} + x^{m} = 0 \implies\\
    & \implies x^{m}(m^2 - m + 3m + 1) = 0 \implies x^{m}(m^2+2m+1)=0 \implies\\
    & \implies m=1 \text{ (doble)}\\
    & y = C_{1}x^{-1}+ C_{2}\ln |x| \cdot x^{-1} \implies\\
    & \implies y = C_{1}\cdot \frac{1}{x} + C_{2} \cdot \frac{\ln |x|}{x}\\
    & \mathcal{W}(y_{1},y_{2}) =
    \begin{vmatrix}
        y_1 & y_2\\
        y_1' & y_2'
    \end{vmatrix} =
    \begin{vmatrix}
        x^{m} & \ln (x) \cdot  x^{m}\\
        m \cdot  x^{m-1} & \frac{1}{x} \cdot  x^{m} + m \cdot \ln (x) \cdot x^{m-1}   
    \end{vmatrix} =\\
    & = x^{m}(x^{m-1} + m\cdot \ln (x)\cdot x^{m-1}  ) - m \cdot x^{m-1} \cdot \ln (x) \cdot x^{m} =\\
    & = x^{2m - 1}  + m \cdot  x^{2m - 1}\cdot \ln (x) - m\cdot x^{2m - 1}  \cdot \ln (x) =\\
    & = x^{2m-1} \neq 0 \forall x \neq  0 
\end{split}
$$
