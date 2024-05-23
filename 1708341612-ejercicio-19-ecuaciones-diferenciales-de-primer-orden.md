---
id: 1708341612-ejercicio-19-ecuaciones-diferenciales-de-primer-orden
aliases:
  - Ejercicio 19 ecuaciones diferenciales de primer orden
  - Resuelve la ecuación ${y' + 2xy = 4x}$
tags:
  - ecuaciones-diferenciales
---

# Resuelve la [[1706869334-ecuacin-diferencial|ecuación]] ${y' + 2xy = 4x}$

Es una [[1708333648-ecuacin-diferencial-lineal|ecuación lineal]] completa de primer [[1706869571-orden-ecuacin-diferencial|orden]]

1. SGEH

$$\begin{split}
    & y' + 2xy = 0 \implies \frac{dy}{dx} = -2xy \implies \frac{1}{y}dy ) -2x dx \implies \\
    & \implies \int \frac{1}{y}dy = - \int 2x dx \implies ln|y| = -x^2 + C_1 \implies \\
    & \implies e^{ln|y|} = e^{-x^2 + C_1} \implies |y| =  C_2 e^{-x^2}, \; C \in \mathbb{R}\\
\end{split}$$

2. SPEC / SGEC

$$\begin{split}
    & y = Ce^{-x} \implies y = C(x) e^{-x^2}\\
    & y' + 2xy = 4x \implies (C'(x) e^{-x^2} - 2x C(x) e^{-x^2}) + 2x C(x)e^{-x^2} = 4x \implies \\
    & \implies C'(x) = 4x e^{x^2} \implies C(x) = 2e^{x^2} + C \\
\end{split}$$

$$\begin{split}
    & y_{SGEC} = C(x)e^{-x^2} = (2x^{x^2} + C)e^{-x^2} = 2 + Ce^{-x^2}\\
    & SPEC = 2\\
    & SGEH = C e^{-x^2}\\
\end{split}$$
