---
id: 1713782172-ejercicio-1-tema-6-ecuaciones-diferenciales
aliases:
  - Ejercicio 1 tema 6 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Calcular la transformada de Laplace de la función $f(x) = x$ para $x > 0$.

$$
\begin{split}
    & f(x) = x, \quad x > 0\\
    & \mathcal{L}\{f(x)\} = \int_{0}^{\infty} e^{-sx} x dx =\\
    & = \begin{cases}
        & u = x \to du = dx\\
        & dv = e^{-sx} \to v = -\frac{1}{s} e^{-sx}
    \end{cases} =\\
    & = \left[\frac{-1}{s}xe^{-sx} \right]_{0}^{\infty} + \frac{1}{s} \int_{0}^{\infty} e^{-sx} dx =\\
    & s > 0 \implies \frac{-1}{s}\left( \frac{\infty}{e^{s \infty} } - 0 \cdot 1 \right) + \frac{1}{s} \left[ \frac{-1}{s} e^{-sx} \right]_{0}^{\infty} =\\ 
    & = \frac{1}{s^2} \quad \text{para } s > 0
\end{split}
$$

