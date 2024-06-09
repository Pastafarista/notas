---
id: 1710153233-ejercicio-13-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 13 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Resuelve la ecuación ${y^{iv)} + 2y'' + y = 0}$

$$
\begin{split}
    & r^4 + 2r^2 + 1 = 0 \implies \ldots \implies \begin{cases} & r = i\\ & r = -i \text{ (doble)}\end{cases}\\
    & t = C_{1}e^{ix} + C_{2}xe^{ix} + C_{3}e^{-ix} + C_{4}xe^{-ix} =\\
    & = C_{1}( \cos (x) + i\sin (x) )  + C_{2}x(\cos (x) +i\sin (x)) + \\
    & + C_{3}(\cos (x) - i\sin (x)) + C_{4}x(\cos (x) - i \sin (x)) =\\
    & = (C_{1} + C_{3})\cos (x) + i(C_{1} - C_{3})\sin (x) + (C_{2} + C_{4})x\cos (x) + i(C_{2} - C_{4})x\sin (x) =\\
    & = K_{1}\cos (x) + K_{2}\sin (x) + K_{3}x\cos (x) + K_{4}x\sin (x), \; K_{1},K_{2},K_{3},K_{4} \in \mathbb{R}
\end{split}
$$
