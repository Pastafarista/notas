---
id: 1710152547-ejercicio-11-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 11 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Resuelve la ecuación ${y'' + 4y' + 5y = 0}$

$$
\begin{split}
    & r^2 + 4r + 5 = 0 \implies \ldots \implies r = -2 \pm i\\
    & y = C_{1}e^{r_{1}x} + C_{2}e^{r_{2}x}=C_{1}e^{(-2+i)x}  + C_{2} e^{(-2-i)x} =\\  
    & = C_{1}e^{-2x}e^{ix} + C_{2}e^{-2x}e^{-ix} = \\
    & = C_{1}e^{-2x}(\cos (x) + i \sin (x)) + C_{2}e^{-2x}(\cos (x) - i\sin (x)) =\\  
    & = e^{-2x} (C_{1} + C_{2})\cos (x) + e^{-2x}(C_{1}i - C_{2}i)\sin (x) =\\
    & = K_{1}e^{-2x}\cos (x) + K_{2}e^{-2x}\sin (x), \; K_{1},K_{2} \in \mathbb{R}  
\end{split}
$$
