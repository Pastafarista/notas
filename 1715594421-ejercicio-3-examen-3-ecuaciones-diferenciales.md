---
id: 1715594421-ejercicio-3-examen-3-ecuaciones-diferenciales
aliases:
  - Ejercicio 3 examen 3 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resolver el problema del valor inicial mediante transformadas de Laplace.

$$
\begin{cases}
    y'' + 6y' + 8y = 10e^{-2x}\\
    y(0) = 3\\
    y'(0) = -13
\end{cases}
$$

$$
\begin{split}
    & \mathcal{L}\{y'' + 6y' + 8y\} = \mathcal{L}\{10e^{-2x}\}\implies\\
    & \implies (s^2 \cdot \mathcal{Y}(s) - s \cdot y(0) - y'(0)) + 6(s \cdot \mathcal{Y}(s) - y(0)) + 8\mathcal{Y}(s) = \frac{10}{s + 2}\implies\\
    & \implies s^2 \cdot \mathcal{Y}(s) - 3s + 13 + 6s \cdot \mathcal{Y}(s) - 18 + 8\mathcal{Y}(s) = \frac{10}{s + 2}\implies\\
    & \mathcal{Y}(s) \cdot (s^2 + 6s + 8) = \frac{10}{s + 2} + 3s - 13 + 18\implies\\
    &  \mathcal{Y}(s) = \frac{10}{(s + 2)(s^2 + 6s + 8)} + \frac{3s - 13 + 18}{s^2 + 6s + 8}\implies\\ 
    & \mathcal{Y}(s) = \frac{10 + (3s + 5)(s+2)}{(s + 2)(s + 4)(s + 2)} = \frac{3s^2 + 11s + 20}{(s + 2)^2(s + 4)} =\\
    & = \frac{A}{s + 2} + \frac{B}{(s + 2)^2} + \frac{C}{s + 4}\implies\\
    & \frac{A(s + 2)(s + 4) + B(s + 4) + C(s + 2)^2}{(s + 2)^2(s + 4)} = \ldots = \\
    &\implies \begin{cases}
        A = -3\\
        B = 5\\
        C = 6
    \end{cases}
\end{split}
$$

Este último paso también se puede hacer mediante límites:

$$
\begin{split}
    & B = \lim_{s \to -2} (s+2)^2 \cdot  \mathcal{Y}(s)\\
    & C = \lim_{s \to -4} (s+4) \cdot  \mathcal{Y}(s)\\
\end{split}
$$

Por lo tanto, la solución final sería:

$$
\begin{split}
    & \mathcal{Y} = \frac{-3}{s + 2} + \frac{5}{(s + 2)^2} + \frac{6}{s + 4} \implies\\
    & y(x) = -3e^{-2x} + 5xe^{-2x} + 6e^{-4x}  \\
\end{split}
$$
