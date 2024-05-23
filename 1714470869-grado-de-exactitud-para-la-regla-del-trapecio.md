---
id: 1714470869-grado-de-exactitud-para-la-regla-del-trapecio
aliases:
  - Grado de exactitud para la regla del trapecio
tags:
  - cálculo-numérico
---

# Grado de exactitud para la regla del trapecio

Vamos a ver el [[1713866424-grado-de-exactitud|grado de exactitud]] para la [[1713865822-regla-del-trapecio|regla del trapecio]]:

Para los polinomios de grado $0$ de la forma $f(x)=A$, su grado de exactitud será $\ge 0$

$$
\begin{split}
    & \mathcal{I}(f)=\int_{a}^{b}Adx = A(b-a)\\ 
    & \mathcal{I}^{T}(f) = \frac{b-a}{2}(f(a)+f(b)) = f \left( \frac{a+b}{2} \right)(b-a)= A(b-a)
\end{split}
$$

Para los polinomios de grado $1$ de la forma $f(x)=A+Bx$, su grado de exactitud será $\ge 1$

$$
\begin{split}
    & \mathcal{I}(f)=\int_{a}^{b}(A + Bx)dx = A(b-a) + \frac{B}{2}(b^{2}-a^{2})\\
    & \mathcal{I}^{T}(f) = \frac{b-a}{2}(f(a)+f(b)) = \frac{b-a}{2}(Aa+B + Ab+Bb) =\\
    & = \frac{b-a}{2}\left( \frac{A}{2}\left( b - a + b -a \right) + \frac{B}{2}(b^2 - a^2) \right) = A(b-a) + \frac{B}{2}(b^2 - a^2)
\end{split}
$$

Para los polinomios de grado $2$ de la forma $f(x)=A+Bx+Cx^{2}$, vemos que la regla del trapecio no es exacta para polinomios de grado $2$. Por lo tanto su grado de exactitud será $M=1$.

$$
\begin{split}
    & \mathcal{I}(f)=\int_{a}^{b}(A + Bx + Cx^{2})dx = A(b-a) + \frac{B(b^{2}-a^{2})}{2} + \frac{C(b^{3}-a^{3})}{3}\\
    & \mathcal{I}^{T}(f) = \frac{b-a}{2}(f(a)+f(b)) = \frac{b-a}{2}(C(a^2+b^2)+B(a+b)+2A) =\\
    & = A(b-a) + \frac{B(b-a)(b+a)}{2} + \frac{C(b-a)(b^2+a^2)}{2} =\\
    & = A(b-a) + \frac{B(b^2-a^2)}{2} + \frac{C(b-a)(b^2+a^2)}{2}=\\
    & = A(b-a) + \frac{B(b^2-a^2)}{2} + \frac{C(b^3 - a^3 + a^2b - b^2a)}{2}
\end{split}
$$
