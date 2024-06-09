---
id: 1714986722-ejercicio-19-tema-6-ecuaciones-diferenciales
aliases:
  - Ejercicio 19 tema 6 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resolver la [[1706869334-ecuacin-diferencial|ecuación]] $y''+\cos (x)y=0$ mediante serie de potencias.

$$
\begin{split}
    & b_{0}(x) = \cos (x), b_{1}(x)=0 \text{ son analíticas en } x=0 \implies\\
    & x = 0 \text{ es un punto ordinario.}
\end{split}
$$

$$
\begin{split}
    & y = \sum_{n=0}^{\infty} C_n x^{n} \implies y' = \sum_{n=1}^{\infty} C_n n x^{n-1} \implies y'' ? \sum_{n=2}^{\infty} C_n n (n-1)x^{n-2}\\
    & y'' + \cos (x) y = 0 \implies \sum_{n=2}^{\infty} C_n n (n-1) x^{n-2} + \cos (x) \sum_{n=0}^{\infty} C_n x^{n} = 0 \implies\\ 
    & \implies \\sum_{n=2}^{\infty} C_{n} n (n-1) x^{n-2} + \left( 1 - \frac{x^2}{2} + \frac{x^{4}}{24} - \frac{x^{6}}{720} + \ldots    \right)  \cdot \sum_{n=0}^{\infty} C_n \cdot x_n = 0 \implies\\
    & \implies (2C_{2} + 6C_{3}x + 12 C_{4}x^2 + \ldots ) + \left( 1 - \frac{x^2}{2} + \frac{x^{4}}{24} - \ldots \right) (C_{0} + C_{1}x + C_{2}x^2 + C_{3}x^{3} + \ldots ) = 0 \implies\\
    & \implies (2C_{2} + 6C_{3}x + 12C_{4}x^2 + \ldots ) + (C_{0} + C_{1}x + C_{2}x^2 + C_{3}x^3 + \ldots ) + \left( -\frac{C_{0}}{2}x^2 - \frac{C_{1}}{2}x^3 - \ldots  \right) +`\left( \frac{C_{0}}{24}x^{4} + \frac{C_{1}}{24}x^{5} + \ldots \right) = 0 \implies\\
    & \implies (2C_{2} + C_{0}) + (6C_{3} + C_{1})x + \left(12C_{4} + C_{2} - \frac{C_{0}}{2}\right)x^2 + \left( 20C_{5} + C_{3} - \frac{C_{1}}{2} \right) + \ldots = 0 \implies\\
    & \implies \begin{cases}
        2 C_{2} + C_{0} = 0 \implies C_{2} = -\frac{1}{2}C_{0}\\
        6C_{3} + C_{1} = 0 \implies C_{3} = -\frac{1}{6}C_{1}\\
        12C_{4} + C_{2} -\frac{C_{0}}{2} = 0 \implies C_{4} = \frac{1}{12}\left( \frac{1}{2C_{0} + \frac{1}{2}C_{0}} \right)  = \frac{1}{12}C_{0}\\
        20 C_{5} + C_{3} - \frac{C_{1}}{2} = 0 \implies C_{5} = \frac{1}{20}\left( \frac{1}{2}C_{1} + \frac{1}{6}C_{1} \right) = \frac{1}{30}C_{1} 
    \end{cases} \implies\\
    & y = C_{0} + C_{1}x - \frac{1}{2}C_{0}x^2 - \frac{1}{6}C_{1}x^3 + \frac{1}{12}x^{4} + \frac{1}{30}C_{1}x^{5} + \ldots =\\
    & = C_{0}\left( 1 - \frac{1}{2}x^2 + \frac{1}{12} x^{4} + \ldots   \right) + C_{1}(x - \frac{1}{6}x^3 + \frac{1}{30}x^{5} + \ldots ) \implies\\
    & y = C_{1}y_{1}(x) + C_{2}y_{2}(x)
\end{split}
$$

