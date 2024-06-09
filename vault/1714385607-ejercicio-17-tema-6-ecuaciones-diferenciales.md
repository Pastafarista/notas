---
id: 1714385607-ejercicio-17-tema-6-ecuaciones-diferenciales
aliases:
  - Ejercicio 17 tema 6 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resolver la ecuación $(x^2 + 1)y'' + xy' - y = 0$ mediante series de potencias.

$$
y'' + \frac{x}{x^2 + 1}y' - \frac{1}{x^2 + 1}y = 0
$$

$b_{0}(x)$ y $b_{1}(x)$ son analíticas en $x=0$ y $x=0$ es punto ordinario de la ecuación.

$$
\begin{split}
    & y = \sum_{n=0}^{\infty} C_{n}x^{n} \implies y' = \sum_{n=1}^{\infty} C_{n}\cdot n\cdot x^{n-1} \implies y'' = \sum_{n=2}^{\infty} C_{n}\cdot n\cdot (n-1)\cdot x^{n-2}\\
    & = (x^2 + 1)y'' + xy' - y = 0 \implies (x^2 + 1)\sum_{n=2}^{\infty} C_{n}\cdot n\cdot (n-1)\cdot x^{n-2} + x\sum_{n=1}^{\infty} C_{n}\cdot n\cdot x^{n-1} - \sum_{n=0}^{\infty} C_{n}x^{n} = 0 \implies\\
    & \implies \sum_{n=2}^{\infty} C_{n}\cdot n(n-1)x^{n} + \sum_{n=1}^{\infty} C_{n}\cdot n\cdot x^{n} - \sum_{n=0}^{\infty} C_{n}x^{n} = 0 \implies\\
    & \implies \sum_{n=2}^{\infty} C_{n}\cdot n(n-1)x^{n} + 2C_{2} + 6C_{3}x + \sum_{n=4}^{\infty} C_{n}\cdot n(n-1)x^{n-2} + C_{1}x + \sum_{n=2}^{\infty} C_{n} \cdot n x^{n} - \left( C_{0}+ C_{1}x + \sum_{n=2}^{\infty} C_{n}x^{n} \right) = 0\implies\\
    & (2C_{2} + 6C_{3}x - C_{0}) + \sum_{k=2}^{\infty} C_{k}\cdot k\cdot (k-1)x^{k} + \sum_{k=2}^{\infty} (k+2)(k+1)x^{k} + \sum_{k=2}^{\infty} C_{k}\cdot k\cdot x^{k} - \sum_{k=2}^{\infty} C_{k}x^{k} = 0\implies\\
    & \implies (2C_{2} - C_{0} + 6C_{3}x) + \sum_{k=2}^{\infty} \left( C_{k}\cdot k\cdot (k-1) + C_{k+2}(k+2)(k+1) + C_k \cdot  k - C_k \right) x^{k} = 0 \implies\\
    & \implies (2C_{2} - C_{0} + 6C_{3}x)+ \sum_{k=2}^{\infty} \left( C_{k+2}(k+2)(k+1) + C_k(k^2 - k + k + 1) \right) x^{k} = 0
\end{split}
$$

$$
\begin{split}
    & \begin{cases}
        & 2C_{2} - C_{0} = 0\\
        & 6C_{3} = 0\\
        & C_{k+2}(k+2)(k+1) + C_k(k^2 + 1) = 0
    \end{cases} \implies
    \begin{cases}
        & C_{2} = \frac{1}{2}C_{0}\\
        & C_{3} = 0\\
        & C_{k+2} = \frac{(1 - k^2)}{(k+2)(k+1)C_k} \quad \text{para } k \geq 2
    \end{cases}
\end{split}
$$

$$
\begin{split}
    & k = 2 \implies C_{4} = \frac{-3}{3\cdot 4} = \frac{-1}{8}C_{0}\\
    & k=3 \implies C_{5} = \frac{-8}{4\cdot 5}C_{3} = 0\\
    & k=4 \implies C_{6} = \frac{-15}{5 \cdot 6}C_{4} = -\frac{1}{16}C_{0}\\
    & k=5 \implies C_{7} = \frac{-24}{6\cdot 7}C_{5} = 0\\
    & k=6 \implies C_{8} = \frac{-35}{7\cdot 8}C_{6} = \frac{-5}{128}C_{0}
\end{split}
$$

$$
\begin{split}
    & y = \sum_{n=0}^{\infty} C_{n}x^{n} = C_{0} + C_{1}x + C_{2}x^{2} + C_{3}x^{3} + C_{4}x^{4} + \ldots =\\
    & = C_{0} + C_{1}x + \frac{1}{2}C_{0}x^{2} + 0 - \frac{1}{8}C_{0}x^{4} - \frac{1}{16}C_{0}x^{6} - \frac{5}{128}C_{0}x^{8} + \ldots =\\
    & = C_{0}\left( 1 + \frac{1}{2}x^2 - \frac{1}{8}x^{4} - \frac{1}{16}x^{6} - \frac{5}{128}x^{8} +\ldots  \right) + C_{1}x \implies\\
    & \implies y = C_{0}y_{0}(x) + C_{1}y_{1}(x)
\end{split}
$$

El radio de convergencia es 1.
