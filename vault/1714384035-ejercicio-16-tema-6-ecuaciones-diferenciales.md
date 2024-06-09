---
id: 1714384035-ejercicio-16-tema-6-ecuaciones-diferenciales
aliases:
  - Ejercicio 16 tema 6 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resolver la ecuación $y''+xy=0$ mediante serie de potencias.

$$
\begin{split}
    & y = \sum_{n=0}^{\infty} C_{n}x^{n} \implies y' = \sum_{n=1}^{\infty} C_{n}\cdot n\cdot x^{n-1} \implies y'' = \sum_{n=2}^{\infty} C_{n}\cdot n\cdot (n-1)\cdot x^{n-2}\\
    & y'' + xy = 0 \implies \sum_{n=2}^{\infty} C_{n}\cdot n\cdot (n-1)\cdot x^{n-2} + x\sum_{n=0}^{\infty} C_{n}x^{n} = 0 \implies\\
    & \implies \sum_{n=2}^{\infty} C_{n}\cdot n\cdot (n-1)x^{n-2} + \sum_{n=0}^{\infty} C_{n}x^{n+1} = 0 \implies\\ 
    & \implies 2C_{2} + \sum_{n=3}^{\infty} C_{n}\cdot n\cdot (n-1)x^{n-2} + \sum_{n=0}^{\infty} C_{n}x^{n+1} = 0\implies\\
    & \implies 2C_{2} + \sum_{k=1}^{\infty} C_{k+2}(k+2)(k+1)x^{k} + \sum_{k=1}^{\infty} C_{k-1}x^{k} = 0 \implies\\
    & \implies 2C_{2} + \sum_{k=1}^{\infty} \left( C_{k+2}(k+2)(k+1) + C_{k-1} \right)x^{k} = 0 \implies\\
    & \implies \begin{cases}
        & 2C_{2} = 0\\
        & C_{k+2}(k+2)(k+1) + C_{k-1} = 0
    \end{cases} \implies
    \begin{cases}
        & C_{2} = 0\\
        & C_{k+2} = \frac{-1}{(k+2)(k+1)}C_{k-1} \quad \text{para } k \geq 1
    \end{cases}
\end{split}
$$

$$
\begin{split}
    & k = 1 \implies C_{3} = \frac{-1}{3\cdot 2}C_{0}\\
    & k = 2 \implies C_{4} = \frac{-1}{4\cdot 3}C_{1} = 0\\
    & k = 3 \implies C_{5} = \frac{-1}{5\cdot 4}C_{2} = 0\\
    & k = 4 \implies C_{6} = \frac{-1}{30}C_{3} = \frac{1}{6\cdot 5\cdot 4\cdot 3\cdot 2}C_{0}\\
    & k = 5 \implies C_{7} = \frac{-1}{7\cdot 6}C_{4} = \frac{C_{1}}{7\cdot 6\cdot 5\cdot 4\cdot 3 }
\end{split}
$$

$$
\begin{split}
    & y = \sum_{n=0}^{\infty} C_{n}x^{n} = C_{0} + C_{1}x + C_{2}x^{2} + C_{3}x^{3} + C_{4}x^{4} + \ldots =\\
    & = C_{0} + C_{1}x - \frac{C_{0}}{3\cdot 2}x^{3} - \frac{C_{1}}{4\cdot 3} + \frac{C_{0}}{6\cdot 5\cdot 4\cdot 3\cdot 2}x^{6} + \frac{c_{1}}{7\cdot 6\cdot 5\cdot 4\cdot 3}x^{7} + \ldots =\\
    & = C_{0}\left( 1 - \frac{1}{3\cdot 2}x^3 + \frac{1}{6\cdot 5\cdot 4\cdot 3\cdot 2}x^{6} + \ldots   \right) + C_{1}\left( x - \frac{1}{4\cdot 3}x^{4} + \frac{1}{7\cdot 6\cdot 5\cdot 4\cdot 3}x^{7} + \ldots  \right) \implies\\
    & \implies y = C_{0}y_{1}(x) + C_{1}y_{2}(x)
\end{split}
$$

