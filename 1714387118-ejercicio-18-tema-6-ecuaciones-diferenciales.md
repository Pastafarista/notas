---
id: 1714387118-ejercicio-18-tema-6-ecuaciones-diferenciales
aliases:
  - Ejercicio 18 tema 6 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resolver la ecuación $y''-(1+x)y = 0$ mediante series de potencias.

- $x=0$ es un punto ordinario de la ecuación, ya que $b_{0}(x)$ es analítica en $x=0$

$$
\begin{split}
    & y = \sum_{n=0}^{\infty} C_n x^{n} \implies y' = \sum_{n=1}^{\infty} C_n \cdot n \cdot x^{n-1} \implies y'' = \sum_{n=2}^{\infty} C_n \cdot n \cdot (n-1) \cdot x^{n-2}\\ 
    & y'' - (1+x)y = 0 \implies \sum_{n=2}^{\infty} C_n \cdot n \cdot (n-1) \cdot x^{n-2} - \sum_{n=0}^{\infty} C_n x^{n} = 0 \implies\\
    & \implies 2C_{2} + \sum_{n=3}^{\infty} C_n \cdot n\cdot (n-1)x^{n-2} - C_{0} - \sum_{n=1}^{\infty} C_{n}x^{n} - \sum_{n=0}^{\infty} C_n\cdot x^{n+1} = 0\implies\\
    & \implies (2 C_{2} - C_{0}) + \sum_{k=1}^{\infty} C_{k+2}\cdot (k+2)(k+1)x^{k} - \sum_{k=1}^{\infty} C_k x^{k} - \sum_{k=1}^{\infty} C_{k-1}x^{k} = 0 \implies\\
    & \implies (2 C_{2} - C_{0}) + \sum_{k=1}^{\infty} \left( C_{k+2}\cdot (k+2)(k+1) - C_k - C_{k-1} \right)x^{k} = 0 \implies\\
\end{split}
$$

$$
\begin{split}
    & \begin{cases}
        & 2C_{2} - C_{0} = 0\\
        & C_{k+2}\cdot (k+2)(k+1) - C_k - C_{k-1} = 0
    \end{cases} \implies
    \begin{cases}
        & C_{2} = \frac{1}{2}C_{0}\\
        & C_{k+2} = \frac{C_k + C_{k-1}}{(k+2)(k+1)} \quad \text{para } k \geq 1
    \end{cases}
\end{split}
$$

$$
\begin{split}
    & k = 1 \implies C_{3} = \frac{C_{1} + C_{0}}{6} = \frac{1}{6}C_{0} + \frac{1}{6} C_{1}\\
    & k=2 \implies C_{4} = \frac{C_{2} + C_{1}}{12} = \frac{1}{24}C_{0} + \frac{1}{12}C_{1}\\
    & k = 3 \implies C_{5} = \frac{C_{3} + C_{2}}{20} = \frac{1}{40}C_{0} + \frac{1}{20}\left( \frac{1}{6}C_{0} + \frac{1}{6}C_{1} \right) = \frac{1}{30}C_{0} + \frac{1}{120}C_{1}\\
    & \vdots
\end{split}
$$

$$
\begin{split}
    & y = \sum_{n=0}^{\infty} C_n x^{n} = C_{0} + C_{1}x + C_{2}x^{2} + C_{3}x^{3} + C_{4}x^{4} + \ldots =\\
    & = C_{0} + C_{1}x + \frac{1}{2}C_{0}x^{2} + \frac{1}{6}C_{0}x^{3} + \frac{1}{6}C_{1}x^{3}+ \frac{1}{24}C_{0}x^{4} +\frac{1}{12}C_{1}x^{4}+\ldots =\\
    & = C_{0}\left( 1 + \frac{1}{2}x^2 + \frac{1}{6}x^{3} + \frac{1}{24}x^{4} + \frac{1}{30}x^{5} + \ldots     \right) + C_{1}\left( x + \frac{1}{6}x^{3} + \frac{1}{12}x^{4} + \frac{1}{120}x^{5} + \ldots  \right) \implies\\
    & \implies y = C_{0}y_{1}(x) + C_{1}y_{2}(x)
\end{split}
$$

