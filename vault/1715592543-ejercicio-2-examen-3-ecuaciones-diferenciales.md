---
id: 1715592543-ejercicio-2-examen-3-ecuaciones-diferenciales
aliases:
  - Ejercicio 2 examen 3 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Resuelve la ecuación $(1-x^2)y''-2xy'+6y=0$ mediante series de potencias, proporcionando como resultado final dos soluciones $y_{1}(x)$ e $y_{2}(x)$ en forma de series.

$$
\begin{split}
    & y'' - \frac{2x}{1-x^2}y' + \frac{6}{1-x^2}y = 0 \implies\\
    & y'' + b_{1}(x)y' + b_{0}(x)y = 0
\end{split}
$$

$b_{0}(x)$ y $b_{1}(x)$ son $f$ analíticas en $x=0$ por lo que $x=0$ es un punto ordinario para esta ecuación.

$$
\begin{split}
    & y = \sum_{n=0}^{\infty} C_{n}x^{n} \implies\\
    & y' = \sum_{n=1}^{\infty} nC_{n}x^{n-1}\\
    & y'' = \sum_{n=2}^{\infty} n(n-1)C_{n}x^{n-2}
\end{split}
$$

Introducimos estas series en la ecuación diferencial:

$$
\begin{split}
    & (1-x^2)\sum_{n=2}^{\infty} C_n \cdot n (n-1)x^{n-2} - 2x \sum_{n=1}^{\infty} C_n\cdot n \cdot  x^{n-1} + 6 \sum_{n=0}^{\infty} C_n \cdot  x^n = 0 \implies\\ 
    & \implies \sum_{n=2}^{\infty} C_{n}\cdot n (n-1)x^{n-2} - \sum_{n=2}^{\infty} C_{n} \cdot n \cdot (n-1)x^{n} -2 \sum_{n=1}^{\infty} C_{n} \cdot n \cdot x^{n} +\\
    & + 6 \sum_{n=0}^{\infty} C_{n} \cdot x^{n} = 0 \implies\\
    & \implies 2 C_{2} + 6C_{3} + \sum_{n=4}^{\infty} C_{n}\cdot n \cdot (n-1)x^{n-2} - \sum_{n=2}^{\infty} C_{n} \cdot n \cdot (n-1) x^{n} - 2C_{1}x\\
    & - 2 \sum_{n=2}^{\infty} C_{n}\cdot n\cdot x^{n} + 6C_{0} + 6C_{1}x + 6 \sum_{n=2}^{\infty} C_{n} \cdot x^{n} = 0 \implies\\
    & \implies (2C_{2} + 6C_{3}x - 2C_{1}x + 6C_{0} + 6C_{1}x) + \sum_{k=2}^{\infty} C_{k+2} (k+2)(k+1)x^{k} -\\
    & \sum_{k=1}^{\infty} C_{k} \cdot  k \cdot (k-1) x^{k} - 2 \sum_{k=2}^{\infty} C_{k} \cdot k \cdot x^{k}  + 6 \sum_{k=0}^{\infty} C_{k} \cdot x^{k} = 0 \implies\\
    & \implies ((6C_{0} + 2C_{2}) + (4C_{1} + 6C_{3})x) +\\
    & \sum_{k=2}^{\infty} (C_{k+2}(k+2)(k+1) + C_{k}(-k\cdot (k-1)-2k + 6))x^{k} = 0\implies\\ 
    & \implies \begin{cases}
        6C_{0} + 2C_{2} = 0\\
        4C_{1} + 6C_{3} = 0\\
        C_{k+2} = \frac{k(k-1) + 2k - 6}{(k+2)(k+1)}C_{k}
    \end{cases} \implies\\
    & \implies \begin{cases}
        C_{2} = -3C_{0}\\
        C_{3} = -\frac{2}{3}C_{1}\\
        C_{k+2} = \frac{k^2 + k - 6}{(k+2)(k+1)}C_{k} \quad k \geq 2
    \end{cases}
\end{split}
$$

Ahora iremos dando valores a $k$ para obtener los coeficientes de la serie:

$$
\begin{split}
    & k=2 \implies C_{4} = 0\\
    & k=3 \implies C_{5} = -\frac{1}{5}C_{1}\\
    & k=4 \implies C_{6} = 0\\
    & k=5 \implies C_{7} = -\frac{4}{35}C_{1}\\
    & k=6 \implies C_{8} = 0\\
\end{split}
$$

Por lo tanto la serie de la solución es:

$$
\begin{split}
    & y = \sum_{n=0}^{\infty} C_{n}\cdot x^{n} = C_{0} + C_{1}\cdot x + C_{2}\cdot x^2 + C_{3}x^3 + \ldots =\\
    & = C_{0} + C_{1}x - 3C_{0}x^2 - \frac{2}{3}C_{1}x^3 - \frac{1}{5}C_{1}x^5 - \frac{4}{35}C_{1}x^7 + \ldots =\\
    & = C_{0}(1-3x^2) + C_{1}(x - \frac{2}{3}x^3 - \frac{1}{5}x^5 - \frac{4}{35}x^7 + \ldots)
\end{split}
$$

