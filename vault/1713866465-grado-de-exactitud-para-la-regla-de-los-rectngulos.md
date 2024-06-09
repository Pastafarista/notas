---
id: 1713866465-grado-de-exactitud-para-la-regla-de-los-rectngulos
aliases:
  - Grado de exactitud para la regla de los rectángulos
tags:
  - cálculo-numérico
---

# Grado de exactitud para la regla de los rectángulos

Vamos a ver el [[1713866424-grado-de-exactitud|grado de exactitud]] para la [[1713865627-regla-de-los-rectngulos|regla de los rectángulos]]:

Para los polinomios de grado $0$ de la forma $f(x) = A$, su grado de exactitud será >= 0:

$$
\begin{split}
    & \mathcal{I}(f) = \int_{a}^{b} A dx = A(b - a)\\
    & \mathcal{I}^{R}(f) = (b - a)A
\end{split}
$$

Para polinomios de grado 1 de la forma $f(x) = A + Bx$, vemos que la aproximación no es exacta:

$$
\begin{split}
    & \mathcal{I}(f) = \int_{a}^{b} (A + Bx) dx = A(b - a) + \frac{B}{2}(b^2 - a^2)\\
    & \mathcal{I}^{R}(f) = (b - a)f(a) = (b - a)(A + B \cdot a)
\end{split}
$$

Por lo tanto el [[1713866424-grado-de-exactitud|grado de exactitud]] de la [[1713865627-regla-de-los-rectngulos|regla de los rectángulos]] es $M=0$.
