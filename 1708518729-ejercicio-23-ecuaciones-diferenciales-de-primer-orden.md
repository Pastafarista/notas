---
id: 1708518729-ejercicio-23-ecuaciones-diferenciales-de-primer-orden
aliases:
  - Ejercicio 23 ecuaciones diferenciales de primer orden
  - Resuelve la ecuación $\left(\frac{y}{3x} + y^4ln(x)\right)dx - dy=0$
tags:
  - ecuaciones-diferenciales
---

# Resuelve la ecuación $\left(\frac{y}{3x} + y^4ln(x)\right)dx - dy=0$

$$\begin{split}
    & \left(\frac{y}{3x} + y^4ln(x)\right)dx - dy=0 \implies y' - \frac{1}{3x}y = (ln(x))y^4 \\
    & u = y^{1-\alpha} = y^{1 - 4} \implies u' = -3y^{-4}y' \implies y' = -\frac{u'}{3y^{-4}} \\
    & y'- \frac{1}{3x}y = (ln(x))y^{4} \implies \frac{-u'}{3y^{-4}} - \frac{1}{3x}y = (ln(x))y^4 \implies \frac{-u'}{3}y^4 - \frac{1}{3x}y = (ln(x))y^4 \implies \\
    & \frac{-u'}{3} - \frac{1}{3x}y^{-3} = ln(x) \implies u' + \frac{1}{x}u = -3ln(x) \; \; \text{Ecuación lineal completa en } u\\
\end{split}$$

1. SGEH:

$$\begin{split}
    & u' + \frac{1}{x}u = 0 \implies \frac{du}{dx} = \frac{-u}{x} \implies\\
    & \implies \int \frac{1}{du}du = \int \frac{-1}{x}dx \implies ln(u) = -ln(x) + C \implies u = \frac{C}{x} \\
   & \implies |u| = \frac{C_2}{|x|} \implies u = \frac{c}{x}\\
   & u' + \frac{1}{x}u = -3ln(x) \implies \frac{x C'(x)}{x^2} - \frac{C(x)}{x^2} + \frac{1}{x}\frac{C(x)}{x} = -3ln(x) \implies\\
   & \implies C'(x) = -3xln(x) \implies C(x) = -3\int x ln(x) dx =\\
   & = \cdots = \frac{-3x^2}{2}ln(x) + \frac{3}{2}\frac{x^2}{2} + C\\
   & u = \frac{C(x)}{x} = \frac{1}{x}\left(\frac{-3x^2}{2}ln(x) + \frac{3}{4}x^2 + C\right) = \frac{-3x}{2}ln(x) + \frac{3}{4}x + \frac{C}{x} \\
   & \begin{cases} & u = \frac{-3x}{2}ln(x) + \frac{3}{4}x + \frac{C}{x}\\ & u=y^{-3}\\ \end{cases} \implies \frac{1}{y^3} = \frac{-3x}{2}ln(x) + \frac{3}{4}x + \frac{C}{x}\\
   & y=0 \text{ es solución singular}
\end{split}$$
