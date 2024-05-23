---
id: 1708522466-ejercicio-26-ecuaciones-diferenciales-de-primer-orden
aliases:
  - Ejercicio 26 ecuaciones diferenciales de primer orden
  - Resuelve la ecuación diferencial $y' = y^2 - \frac{1}{x}y - \frac{1}{x^2}$
tags:
  - ecuaciones-diferenciales
---

# Resuelve la [[1706869334-ecuacin-diferencial|ecuación diferencial]] $y' = y^2 - \frac{1}{x}y - \frac{1}{x^2}$

$$\begin{split}
    & p(x) = 1\\
    & q(x) = -\frac{1}{x}\\
    & r(x) = -\frac{1}{x^2}\\
\end{split}$$

$m \in \mathbb{R}\;\;t.q.\;\;y=x^m$ 

$$\begin{split}
    & m x^{m-1} = x^{2m} - x^{m-1} - x^{-2}\\
    & m=-1 \implies -x^{-2} = x^{-2} - x^{-2} - x^{-2}\\
\end{split}$$

$$\begin{split}
    & y = \frac{1}{x} + \frac{1}{u} \implies y' = \frac{-1}{x^2} - \frac{u'}{u^2}\\
    & y' = y^2 - \frac{1}{x}y - \frac{1}{x^2} \implies \frac{-1}{x^2} - \frac{u'}{u^2} = \left( \frac{1}{x} + \frac{1}{u}\right)^2 - \frac{1}{x}\left(\frac{1}{x} + \frac{1}{u}\right) - \frac{1}{x^2} \implies\\
    & \implies -\frac{1}{x^2} - \frac{u'}{u^2} = \frac{1}{x^2} + \frac{2}{xu} + \frac{1}{u^2} - \frac{1}{x^2} - \frac{1}{xu} - \frac{1}{x^2} \implies u' + \frac{1}{x}u + 1 = 0 \implies u' + \frac{1}{x}u = -1\\
\end{split}$$

$$\begin{split}
    & y = \frac{1}{x}\\
    & y = x^m\\
    & y = \frac{1}{x} + \frac{1}{u} \implies y' = \frac{-1}{x^2} - \frac{u'}{u^2}\\
    & \left( - \frac{1}{x^2} - \frac{u'}{u^2} \right) = \right( \frac{1}{x} + \frac{1}{u} \left)^2 - \frac{1}{x}\left(\frac{1}{x} + \frac{1}{u} \right) - \frac{1}{x^2} \implies \cdots \implies\\
    & \implies u' + \frac{u}{x} = -1\\
\end{split}$$
