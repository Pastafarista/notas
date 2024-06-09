---
id: 1714989027-ejercicio-20-tema-6-ecuaciones-diferenciales
aliases:
  - Ejercicio 20 tema 6 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resolver la [[1706869334-ecuacin-diferencial|ecuación]] $4xy''+2y'+y=0$ mediante series de potencias.

$x=0$ ess un punto singular

$$
\begin{split}
    & p(x) = x \cdot b_{1}(x) = \frac{1}{2}\\
    & q(x) = x^2b_{0}(x) = \frac{x}{4}
\end{split}
$$

Como ambas son analíticas, $x=0$ es un punto singular regular.

$$
\begin{split}
    \begin{cases}
        p_{0} = \lim_{x \to 0} p(x) = \frac{1}{2}\\
        q_{0} = \lim_{x \to 0} q(x) = 0
    \end{cases} \implies
    r(r-1) + p_{0} \cdot  r + q_{0} = 0 \implies\\
    & \implies r^2 - r + \frac{1}{2}r + 0 = 0 \implies r^2 - \frac{1}{2}r = 0 \implies\\
    & \implies \begin{cases}
        r = 0\\
        r = \frac{1}{2}
    \end{cases}
\end{split}
$$

Caso I

$$
\begin{split}
    & y = \sum_{n=0}^{\infty} C_{n}x^{n+r} \implies y' = \sum_{n=0}^{\infty} C_{n}(n+r)x^{n+r-1} \implies y'' = \sum_{n=0}^{\infty} C_{n}(n+r)(n+r-1)x^{n+r-2}\\ 
    & 4xy'' + 2y' + y = 0 \implies\\
    & \implies 4x \sum_{n=1}^{\infty}C_{n}(n+r)(n+r-1)x^{n+r-2} + 2 \sum_{n=0}^{\infty} C_{n}(n+r)x^{n+r-1} + \sum_{n=0}^{\infty} C_{n}x^{n+r} = 0 \implies\\
    &\implies 4 \sum_{n=0}^{\infty} C_{n}(n+r)(n+r-1)x^{n+r-1} + 2 \sum_{n=0}^{\infty} C_{n}(n+r)x^{n+r-1} + \sum_{n=0}^{\infty} C_{n}x^{n+r} = 0 \implies\\ 
    & \implies x^{r}\left( 4 \sum_{n=0}^{\infty} C_n(n+3)(n+r-1)x^{n-1} + 2 \sum_{n=0}^{\infty} C_n(n+r)x^{n-1} + \\sum_{n=0}^{\infty} C_nx^{n} \right) = 0 \implies\\
    & \implies x^{r}\left( 4 C_{0} r (r-1)x^{-1} + 4 \sum_{n=1}^{\infty} C_n(n+r)(n+r-1)x^{n-1} + 2C_{0}rx^{-1} + 2 \sum_{n=1}^{\infty} C_n(n+r)x^{n-1} + \sum_{n=0}^{\infty} C_n x^{n} \right) = 0 \implies\\
    & \implies x^{r}\left( (4C_{0}r(r-1) + 2C_{0}r)x^{-1} + 4 \sum_{k=0}^{\infty} C_{k+1}(k+1+r)(j+1+r-1)x^{k} + 2 \sum_{k=0}^{\infty} C_{k+1}(k+1+r)x^{k} + \sum_{k=0}^{\infty} C_k x^{k} \right) = 0\implies\\
    & \implies x^{r}\left( (2C_{0} (2(r^2-r) + r))x^{-1} + \sum_{k=0}^{\infty} (4 C_{k+1} (k+1+r)(k+r) + 2 C_{k+1}(k+1+r) + C_k )x^{k} )\right) = 0 \implies\\
    & \implies \begin{cases}
        2r^2-r = 0 \implies \begin{cases}
            r = 0\\
            r = \frac{1}{2}
        \end{cases} \\
        2C_{k+1}(2(k+1+r)(k+r) + (k+1+r)) + C_k = 0 \implies 2C_{k+1}((k+1+r)(2k+2r+1)) + C_k = 0 \implies\\
        \implies C_{k+1} -\frac{C_k}{2 (k+1+r)(2k+2r+1)}
    \end{cases}
\end{split}
$$

Para $r=0$

$$
\begin{split}
    & C_{k+1} = -\frac{C_{k}}{2(k+1)(2k+1)} \quad k \geq 0\\
    & k = 0 \implies C_{1} = -\frac{C_{0}}{2}\\
    & k =1 \implies C_{2} = -\frac{C_{1}}{2\cdot 2\cdot 3} = -\frac{C_{1}}{4\cdot 3} = \frac{C_{0}}{4\cdot 3\cdot 2}\\
    & \vdots
    & C_{n} = \frac{(-1)C_{0}}{(2n)!}
\end{split}
$$

$$
\begin{split}
    & y_{1}(x) = \sum_{n=0}^{\infty} C_{n}x^{n+r} = C_{0} \sum_{n=0}^{\infty} \frac{(-1)^{n}}{(2n)!}x^{n} \implies\\
    & \implies \sum_{n=0}^{\infty} \frac{(-1)^{n}}{(2n)!}x^{n}
\end{split}
$$

para $r = \frac{1}{2}$

$$
\begin{split}
    & C_{k+1} = -\frac{C_k}{2(k+\frac{3}{2})(2k + 2)} \quad k \geq 0\\
    & k=0 \implies C_{1} = -\frac{C_{0}}{3 \cdot 2}\\
    & k = 1 \implies C_{2} = -\frac{C_{1}}{4 \cdot \frac{5}{2} \cdot 2} = -\frac{C_{1}}{5\cdot 4} = \frac{C_{0}}{5\cdot 4\cdot 3\cdot 2}\\
    & k = 2 \implies C_{3} = -\frac{C_{2}}{4 \cdot \frac{7}{2} \cdot 3} = -\frac{C_{2}}{7 \cdot 6} = -\frac{C_{0}}{7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2}\\
    & \vdots
    & C_{n} = \frac{(-1)^{n}C_{0}}{(2n+1)!}
\end{split}
$$

$$
\begin{split}
    & y_{2}(x) = \sum_{n=0}^{\infty} C_{n}x^{n+r} = C_{0} \\sum_{n=0}^{\infty}  \frac{(-1)^{n} }{(2n+1)!}x^{n + \frac{1}{2}} \implies\\
    & \implies y_{2}(x) = \sum_{n=0}^{\infty} \frac{(-1)^{n} }{(2n+1)!}x^{n+\frac{1}{2}} 
\end{split}
$$
