---
id: 1709729117-ejercicio-4-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 4 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Obtén la solución general de la [[1706869334-ecuacin-diferencial|ecuación]] $y' + y'' = x$

Falta $y \to $ Reducible tipo 1

$$
\begin{split}
    & y' = u \implies y'' = u'\\
    & y' + y'' = xa \implies u + u' = x \implies u' + u = x\\
\end{split}
$$

$u' + u =x$ es lineal completa de primer orden

1. SGEH:

$$\begin{split}
    & u + u' = 0 \implies  u + \frac{du}{dx} = 0 \implies \frac{du}{dx} = -u \implies \\
    & \implies \int \frac{1}{u} du = -\int dx \implies \ldots  \implies u = C e^{-x}\\
\end{split}$$

2. SPEC:

$$\begin{split}
    & u = C(x) e^{-x} \implies u' = C'(x)e^{-x} - C(x) e^{-x}\\
    & u + u' = x \implies C(x)e^{-x} + C'(x)e^{-x} - C(x)e^{-x} = x \implies \\
    & \implies C'(x) = xe^{x} \implies \ldots  \implies C(x) = (x-1)e^x + C\\
    & u = C(x)e^{-x} = ((x-1)e^{x} + C)e^{-x} = Ce^{-x} + (x-1) \text{ SGEC}\\
    & y' = u \implies y' = Ce^{-x} +x -1 \implies\\
    & \implies y = \frac{x^2}{2} - x - Ce^{-x} + K \;\; C_1, \; k \in \mathbb{R}
\end{split}$$
