---
id: 1714382822-ejercicio-15-tema-6-ecuaciones-diferenciales
aliases:
  - Ejercicio 15 tema 6 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resolver la ecuación $y'-2xy=0$ mediante series de potencias.

- $x=0$ es punto ordinario de la [[1706869334-ecuacin-diferencial|ecuación]]

$$
\begin{split}
    & y = \sum_{n=0}^{\infty} C_{n}x^{n} \implies y' = \sum_{n=1}^{\infty} C_{n}\cdot n\cdot x^{n-1}\\
    & y' - 2xy = 0 \implies \sum_{n=1}^{\infty} C_{n}\cdot n\cdot x^{n-1} - 2x\sum_{n=0}^{\infty} C_{n}x^{n} = 0 \implies\\
    & \implies \sum_{n=1}^{\infty} C_{n}\cdot n\cdot x^{n-1} - 2 \sum_{n=0}^{\infty} C_{n}x^{n+1} = 0 \implies\\
    & \implies C_{1}\cdot 1 + \sum_{n=2}^{\infty} C_{n}\cdot n\cdot x^{n-1} - 2 \sum_{n=0}^{\infty} C_{n}x^{n+1} = 0 \implies\\ 
    & C_{1} + \sum_{k=1}^{\infty} C_{k+1}(k+1)x^{k} - 2 \sum_{k=1}^{\infty} C_{k-1}x^{k} = 0 \implies\\
    & \implies C_{1} + \sum_{k=1}^{\infty} \left( C_{k+1}(k+1) - 2C_{k-1} \right)x^{k} = 0 \implies\\
    & \implies \begin{cases}
        & C_{1} = 0\\
        & C_{k+1}(k+1) - 2C_{k-1} = 0
    \end{cases} \implies
    \begin{cases}
        & C_{1} = 0\\
        & C_{k+1} = \frac{2}{k+1}C_{k-1} \quad \text{para } k \geq 1
    \end{cases}\\
    \end{split}
$$

$$
\begin{split}
    & k = 1 \implies C_{2} = \frac{2}{2}C_{0} = C_{0}\\
    & k = 2 \implies C_{3} = \frac{2}{3}C_{1} = 0\\
    & k = 3 \implies C_{4} = \frac{2}{4}C_{2} = \frac{1}{2}C_{0}\\
    & k = 4 \implies C_{5} = \frac{2}{5}C_{3} = 0\\
    & k = 5 \implies C_{6} = \frac{2}{6}C_{4} = \frac{1}{6}C_{0}\\
\end{split}
$$

$$
\begin{split}
    & y = \sum_{n=0}^{\infty} C_{n}x^{n} = C_{0} + C_{1}x + C_{2}x^{2} + C_{3}x^{3} + C_{4}x^{4} + \ldots =\\
    & = C_{0} + 0 + C_{0}x^{2} + 0 + \frac{1}{2}C_{0}x^{4} + \frac{1}{6}C_{0}x^{6} + \ldots =\\
    & = C_{0}\left( 1 + x^2 + \frac{1}{2}x^{4} + \frac{1}{6}x^{6} +\ldots \right) =\\
    & = C_{0}e^{x^2} \implies y = C\cdot e^{x^2} 
\end{split}
$$
