---
id: 1710757268-ejercicio-27-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 27 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Resuelve la ecuación $y'' + y = \cos (x)$ utilizando el método de variación de constantes

1. SGEH:

$$
\begin{split}
    & y '' + y = 0 \implies r^2 + 1 = 0 \implies r = \pm i \implies y_{SGEH} = C_{1}\sin (x) + C_{2}\cos(x)
\end{split}
$$

2. SGEC / SPEC:

$$
\begin{split}

    & \begin{cases}
        & C_{1}'(x) y_{1}(x) + C_{2}'(x)y_{2}(x) = 0\\
        & C_{1}'(x) y_{1}'(x) + C_{2}'(x)y_{2}'(x)= S(x)
    \end{cases} \implies
    \begin{cases}
        & C_{1}'(x)\sin (x) + C_{2}'(x)\cos (x) = 0\\
        & C_{1}'(x)\cos (x) - C_{2}'(x) \sin (x) = \cos (x)
    \end{cases} \implies\\
    & \implies C_{1}'(x) = \frac{\begin{vmatrix} 0 & \cos (x)\\ \cos (x) & -\sin (x) \end{vmatrix}}{\begin{vmatrix} \sin (x) & \cos (x)\\ \cos (x) & -\sin (x) \end{vmatrix}} = \frac{-\cos ^2(x)}{-\sin ^2(x) -\cos ^2(x)} = \cos ^2(x) \implies\\
    & \implies C_{1}(x) = \int \frac{\cos ^2(x)}{dx} = \int  \frac{1 + \cos (2x)}{2} dx = \frac{x}{2} + \frac{1}{4}\sin (2x) + C_{1}\\
    & C_{2}'(x) = \frac{\begin{vmatrix} \sin (x) & 0\\ \cos (x) & \cos (x) \end{vmatrix}}{\begin{vmatrix} \sin (x) & \cos (x) \\ \cos (x) & -\sin (x)\end{vmatrix}} = -\sin (x)\cos (x) = \frac{-\sin (x)}{2} \implies C_{2}(x) = -\int \frac{\sin (2x)}{2}dx = \frac{\cos (2x)}{4} + C_{2}\\
    & Y_{SGEC} = C_{1}(x)\sin (x) + C_{2}(x)\cos (x) = \left( \frac{x}{2} + \frac{1}{4}\sin (2x) + C_{1} \right) \sin (x) + \left( \frac{\cos (2x)}{4} + C_{2} \right)\cos(x) =\\
    & = C_{1}\sin (x) + C_{2}\cos (x) + \left( \frac{x}{2}\sin (x) + \frac{1}{4}\sin (2x)\sin (x) + \frac{1}{4}\cos (2x)\cos (x) \right) =\\
    & = C_{1}\sin (x) + C_{2}\cos (x) + \frac{x}{2} \sin (x) + \frac{1}{4}\cos (x)\\
    & \frac{1}{4}\sin (2x)\sin (x) + \frac{1}{4}\cos (2x)\cos (x) = \frac{1}{4}2\sin (x)\cos (x)\sin (x) + \frac{1}{4} (\cos ^2(x)-\sin ^2(x))\cos (x)=\\
    & = \frac{1}{4}\cos (x)(2\sin ^2(x) + \cos ^2(x) - \sin ^2(x)) = \frac{1}{4}\cos (x)(\sin ^2(x)+\cos ^2(x)) = \frac{1}{4} \cos (x)
\end{split}
$$
