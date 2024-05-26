---
id: 1716660069-grado-de-exactitud-para-la-regla-del-trapecio
aliases:
  - Grado de exactitud para la regla del trapecio
tags:
  - cálculo-numérico
---

# Grado de exactitud para la regla del trapecio

Vamos a ver el [[1713866424-grado-de-exactitud|grado de exactitud]] para la [[1713865822-regla-del-trapecio|regla del trapecio]]:

Para $n=0$ tenemos $f(x)=A$, vemos que el grado de exactitud será mayor o igual de $0$:

$$
\begin{split}
	& \mathcal{I}(f) = \int_{a}^{b} f(x)dx = \int_{a}^{b} Adx = \left[ Ax \right]_{a}^{b} = Ab - Aa\\
	& \mathcal{I}^{T}(f) = \frac{b-a}{2}[A + A] = A(b-a) = Ab - Aa
\end{split}
$$

Para $n=1$ tenemos $f(x) = A + Bx$, vemos que el grado de exactitud será mayor o igual que $1$:

$$
\begin{split}
	& \mathcal{I}(f) = \int_{a}^{b}f(x)dx = \int_{a}^{b} A + Bx dx = \left[ Ax \right]_{a}^{b} + \left[ \frac{Bx^2}{2} \right]_{a}^{b} = A(b-a) + \frac{B}{2}(b^2 - a^2)\\
	& \mathcal{I}^{T}(f) = \frac{b-a}{2}(A + Ba + A + Bb) = \frac{b-a}{2}(2A + B(a+b)) = A(b-a) + \frac{B(b-a)(b+a)}{2} =\\
	& A(b-a) + \frac{B}{2}(b^2 - a^2)
\end{split}
$$

Para $n=2$ tenemos $f(x)=x^2$, vemos que la regla de cuadratura difiere de la integral de $f$.

$$
\begin{split}
	& \mathcal{I}(f) = \int_{a}^{b}x^2 dx = \left[ \frac{x^3}{3} \right]_{a}^{b} = \frac{b^3 - a^3}{3}\\
	& \mathcal{I}^{T}(f) = \frac{b-a}{2}(f(a)+f(b)) = \frac{b-a}{2}(a^2 + b^2)
\end{split}
$$

Por lo tanto podemos asegurar que el [[1713866424-grado-de-exactitud|grado de exactitud]] de la [[1713865822-regla-del-trapecio|regla del trapecio]] es $M=1$.

