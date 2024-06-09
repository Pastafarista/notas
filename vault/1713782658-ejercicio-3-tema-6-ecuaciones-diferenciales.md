---
id: 1713782658-ejercicio-3-tema-6-ecuaciones-diferenciales
aliases:
  - Ejercicio 3 tema 6 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Calcular la transformada de Laplace de la función $f(x) = \sin (x)$ para $x > 0$.

$$
\begin{split}
    & f(x) = \sin(x), \quad x > 0\\
    & \mathcal{L}\{f(x)\} = \int_{0}^{\infty} e^{-sx} \sin(x) dx =\\
    & = \begin{cases} 
        & u = \sin (x) \to du = \cos(x) dx\\
        & dv = e^{-sx} \to v = -\frac{1}{s} e^{-sx}
    \end{cases} =\\
    & = \left[ -\frac{1}{s} e^{-sx} \sin(x) \right]_{0}^{\infty} + \frac{1}{s} \int_{0}^{\infty} e^{-sx} \cos(x) dx =\\
    & = \begin{cases}
        & u = \cos(x) \to du = -\sin(x) dx\\ 
        & dv = e^{-sx} \to v = -\frac{1}{s} e^{-sx}
    \end{cases} =\\
    & = \frac{1}{s}\left( -\frac{1}{s}\left[ \cos (x) \cdot e^{-sx}  \right]^{\infty}_{0} - \frac{1}{s} \int_{0}^{\infty} e^{-sx} \sin (x)dx  \right) =\\
    &= \frac{1}{s} \left( \frac{1}{s} - \frac{1}{s} I \right) = \frac{1}{s^2}(1-I) \implies\\
    & \implies I = \frac{1}{s - s^2} - \frac{1}{^2}I \implies I \left( 1 + \frac{1}{s^2} \right) = \frac{1}{s^2} \implies\\
    & \implies I = \mathcal{L}\{\sin(x)\} = \frac{1}{s^2 + 1}
\end{split}
$$

