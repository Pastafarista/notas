---
id: 1713782408-ejercicio-2-tema-6-ecuaciones-diferenciales
aliases:
  - Ejercicio 2 tema 6 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Calcular la transformada de Laplace de la función $f(x)= cosh(x) $ para $x > 0$.

$$
\begin{split}
    & f(x) = cosh(x), \quad x > 0\\
    & \mathcal{L}\{f(x)\} = \int_{0}^{\infty} e^{-sx} cosh(x) dx =\\
    & = \int_{0}^{\infty} e^{-sx} \left( \frac{e^x + e^{-x}}{2} \right) dx =\\
    & = \frac{1}{2} \int_{0}^{\infty} e^{-(s-1)x} + e^{-(s+1)x} dx =\\
    & = \frac{1}{2} \left[ \frac{e^{-(s-1)x}}{-(s-1)} + \frac{e^{-(s+1)x}}{-(s+1)} \right]_{0}^{\infty} =\\
    & s > x \implies \frac{1}{2} \left( \frac{-1}{s-1}\left( \frac{1}{e^{(s-1)\infty} -1} \right) - \frac{1}{s+1}\left( \frac{1}{e^{(s+1)\infty} } - 1\right)  \right) =\\
    & = \frac{1}{2} \left( \frac{1}{s-1} + \frac{1}{s+1} \right) = \frac{s}{s^2-1} 
\end{split}
$$


