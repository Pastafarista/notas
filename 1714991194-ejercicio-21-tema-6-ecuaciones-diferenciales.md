---
id: 1714991194-ejercicio-21-tema-6-ecuaciones-diferenciales
aliases:
  - Ejercicio 21 tema 6 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resolver la [[1706869334-ecuacin-diferencial|ecuación]] $xy'' + y' -y = 0$ mediante series de potencias.

$x=0$ es un punto singular regular (ni $b_{1}(x)$ ni $b_{0}(x)$ son anaítics en $x=0$)

$$
\begin{split}
    & p(x) = x \cdot b_{1}(x) = 1\\
    & q(x) = x^2 \cdot b_{0}(x) = -x
\end{split}
$$

Ambas analíticas en $x=0\implies x=0 \text{ punto singular regular}$

$$
\begin{split}
    & \begin{cases}
    p_{0} = \lim_{x \to 0} p(x) = 1\\
    q_{0} = \lim_{x \to 0} q(x) = 0
    \end{cases} \implies r(r-1) + p_{0}r + q_{0} = 0 \implies\\
    & \implies r^2 -r + r = 0 \implies r = 0 \text{ (doble)}
\end{split}
$$

Este sería el caso II

$$
\begin{split}
    & y = \sum_{n=0}^{\infty} C_{n}x^{n+r} = y' = \sum_{n=0}^{\infty} C_{n}(n+r)x^{n+r-1} = y'' = \sum_{n=0}^{\infty} C_{n}(n+r)(n+r-1)x^{n+r-2}\\
    & xy'' + y' - y = 0 \implies x \sum_{n=0}^{\infty} C_{n}(n+r)(n+r-1)x^{n+r-2} + \sum_{n=0}^{\infty} C_{n}(n+r)x^{n+r-1} - \sum_{n=0}^{\infty} C_{n}x^{n+r} = 0 \implies\\
    & \implies x^{r}\left( \sum_{n=0}^{\infty} C_n(n+r)(n+r-1)x^{n-1} + \sum_{n=0}^{\infty} C_n(n+r)x^{n-1} - \sum_{n=0}^{\infty} C_n x^{n} \right)= 0 \implies\\
    & \implies x^{r} \left( C_{0} r (r-1) x^{-1} + \sum_{n=1}^{\infty} C_n(n+r)(n+r-1)x^{n-1} + C_{0}r x^{-1} + \sum_{n=1}^{\infty} C_n(n+r)x^{n-1} + \sum_{n=0}^{\infty} C_n x^{n}\right) = 0 \implies\\
    & \implies x^{r}\left( C_{0}(r(r-1) + r)x^{-1} + \sum_{k=0}^{\infty}( C_{k+1}(k+1+r)(k+1+r-1) + C_{k+1}(k+1+r) + C_k)x^{k}  \right )= 0 \implies\\
    & \implies \begin{cases}
        r(r-1) + r = 0 \implies r = 0 \text{ (doble) Caso II}\\
        C_{k+1} (k+1+r)(k+r+1) - C_k = 0 \implies C_{k+1} = \frac{C_k}{(k+1+r)^2} \quad k \geq 0
    \end{cases}
\end{split}
$$
