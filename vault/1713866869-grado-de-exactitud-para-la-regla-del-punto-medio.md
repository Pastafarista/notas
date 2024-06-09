---
id: 1713866869-grado-de-exactitud-para-la-regla-del-punto-medio
aliases:
  - Grado de exactitud para la regla del punto medio
tags:
  - cálculo-numérico
---

# Grado de exactitud para la regla del punto medio

Vamos a ver el [[1713866424-grado-de-exactitud|grado de exactitud]] para la [[1713865721-regla-del-punto-medio|regla del punto medio]]:

Para los polinomios de grado $0$ de la forma $f(x) = A$, su grado de exactitud será >= 0:

$$
\begin{split}
    & \mathcal{I}(f) = \int_{a}^{b} A dx = A(b - a)\\
    & \mathcal{I}^{PM}(f) = (b - a)f\left(\frac{a + b}{2}\right) = (b - a)A
\end{split}
$$

Para polinomios de grado 1 de la forma $f(x) = A + Bx$, vemos que la aproximación es exacta, por lo tanto el grado de exactitud es $M\ge 1$:

$$
\begin{split}
    & \mathcal{I}(f) = \int_{a}^{b} (A + Bx) dx = A(b - a) + \frac{B(b^2 - a^2)}\\
    & \mathcal{I}^{PM}(f) = (b - a)f\left(\frac{a + b}{2}\right) = (b - a)\left(A + B\frac{a + b}{2}\right) =\\
    & (b - a)A + \frac{B(b+a)(b-a)}{2} = (b - a)A + \frac{B(b^2 - a^2)}{2}
\end{split}
$$

Para polinomios de grado 2 de la forma $f(x) = A + Bx + Cx^2$, vemos que la aproximación no es exacta, por lo tanto el grado de exactitud es $M=1$:

$$
\begin{split}
    & \mathcal{I}(f) = \int_{a}^{b} (A + Bx + Cx^2) dx = A(b - a) + \frac{B(b^2 - a^2)}{2} + \frac{C(b^3 - a^3)}{3}\\
    & \mathcal{I}^{PM}(f) = (b - a)f\left(\frac{a + b}{2}\right) = (b - a)\left(A + B\frac{a + b}{2} + C\left(\frac{a + b}{2}\right)^2\right) =\\
    & A(b - a) + B\frac{(b^2 - a^2)}{2} + C\frac{(a+b)(b-a)}{4}
\end{split}
$$

Por lo tanto el [[1713866424-grado-de-exactitud|grado de exactitud]] de la [[1713865721-regla-del-punto-medio|regla del punto medio]] es $M=1$.
