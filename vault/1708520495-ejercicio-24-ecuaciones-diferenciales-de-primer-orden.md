---
id: 1708520495-ejercicio-24-ecuaciones-diferenciales-de-primer-orden
aliases:
  - Ejercicio 24 ecuaciones diferenciales de primer orden
tags:
  - ecuaciones-diferenciales
---

# Resuelve la ecuación $y' + \frac{y}{x+1} = -\frac{1}{2}(x+1)^3y^2$

$$\begin{split}
    & y' + \frac{y}{x+1} = -\frac{1}{2}(x+1)^3y^2\\
    & p(x) = \frac{y}{x+1}\\
    & r(x) = -\frac{1}{2}(x+1)^3\\
    & \alpha = 2\\
\end{split}$$

$$\begin{split}
    & u = y^{1-\alpha} = y^{1-2} = y^{-1} \implies u' = -y^{-2}y' \implies y' = \frac{-u'}{y^{-2}}\\
    & y' + \frac{y}{x+1} = -\frac{1}{2}(x+1)^3y^2 \implies \frac{-u'}{y^{-2}} + \frac{y}{x+1} = -\frac{1}{2}(x+1)^3y^2 \implies u' - \frac{1}{x+1}u = \frac{1}{2}(x+1)^3\\
    & \text{Ecuación lineal completa en } u\\
\end{split}$$

1. SGEH:

$$\begin{split}
    & u' - \frac{1}{x+1}\;\; , u=0 \implies \frac{du}{dx} = \frac{u}{x+1} \implies \frac{1}{u}du = \frac{1}{x+1}dx \implies\\
    & \implies \int \frac{1}{u}dy = \int \frac{1}{x+1}dx \implies ln|u| = ln|x+1| + C_1 \implies u = C(x+1)\\
\end{split}$$

2. SGEC/SPEC (variación de constantes):

$$\begin{split}
    & u = C(x)(x+1) \implies u' = C'(x)(x+1) + C(x) \\
    & u' - \frac{1}{x+1}u = \frac{(x+1)^3}{2} \implies C'(x)(x+1) + C(x) - \frac{1}{x+1}C(x)(x+1) = \frac{(x+1)^3}{2} \implies\\
    & \implies C'(x) = \frac{(x+1)^2}{2} \implies C(x) = \frac{(x+1)^3}{6} + C\\
    & u = C(x)(x+1) = \left(\frac{(x+1)^3}{6} + C\right)(x+1) = \frac{(x+1)^4}{6} + C (x+1)\\
    & u = y^{-1} \implies \frac{1}{y} = \frac{(x+1)^4}{6} + C (x+1)\\
    & C_y=0 \text{ es solución singular}\\
\end{split}$$
