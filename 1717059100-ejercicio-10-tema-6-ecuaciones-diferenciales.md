---
id: 1717059100-ejercicio-10-tema-6-ecuaciones-diferenciales
aliases:
  - Ejercicio 10 tema 6 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resolver el problema de valor inicial $\begin{cases}y'-4y=0\\y(0)=3\end{cases}$ mediante transformadas de Laplace.

$$
\begin{split}
    & \mathcal{L}\{y'\} = sY(s) - y(0) = sY(s) - 3\\
    & \mathcal{L}\{4y\} = \frac{4}{s^2}
\end{split}
$$

Por lo tanto:

$$
\begin{split}
    & \mathcal{L}\{y'\} = \mathcal{L}\{4y\} \iff sY(s) - 3  = \frac{4}{s^2} \iff sY(s) = \frac{4}{s^2} + 3 \iff Y(s) = \frac{4}{s^3} + \frac{3}{s}\\
    & \mathcal{L}^{-1}\{Y(s)\} = \mathcal{L}^{-1}\left\{\frac{4}{s^3} + \frac{3}{s}\right\} = y(x) = 2x^2 + 3
\end{split}
$$

