---
id: 1710761451-ejercicio-31-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 31 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Resuelve la ecuación $y''' - 2y'' - 21y' - 18y = 3 + 4e^{-x}$ utilizando el método de variación de constantes

1. SGEH:

$$
\begin{split}
    & y''' - 2y'' - 21y' - 18y = 0 \implies r^3  - 2r^2 - 21r -18 = 0 \implies \begin{cases} & r=-1 \\ & r=-3\\ & r=6\end{cases} \implies\\
    & \implies y_{SGEH} = C_{1}e^{-x} + C_{2}e^{-3x} + C_{3}e^{6x}   
\end{split}
$$

2. SGEC / SPEC:

$$
\begin{split}
    & \begin{cases}
        & C_{1}'(x)y_{1}(x) + C_{2}'(x)y_{2}(x) + C_{3}'(x)y_{3}(x) = 0\\
        & C_{1}'(x)y_{1}'(x) + C_{2}'(x)y_{2}'(x) + C_{3}'(x)y_{3}'(x) = 0\\
        & C_{1}'(x)y_1''(x) + C_{2}'(x)y_2''(x) + C_{3}'(x)y_{3}''(x) = S(x)
    \end{cases} \implies\\
    & \begin{cases}
        & C_{1}'(x)e^{-x} + C_{2}'(x)e^{-3x} + C_{3}'(x) e^{6x} = 0\\
        & -C_{1}e^{-x} - 3C_{2}'(x)e^{-3x} + 6C_{3}'(x)e^{6x} = 0\\
        & C_{1}'(x)e^{-x} + 9C_{2}'(x)e^{-3x} + 36 C_{3}'(x) e^{6x} = 3 + 4 e ^{-x}   
    \end{cases} \implies\\
    & \implies C_{1}'(x) = -\frac{3}{14}e^{x} - \frac{2}{7} \implies C_{1}(x) = -\frac{3}{14}e^{x}-\frac{2}{7}x + C_{1}\\
    & C_{2}'(x) = \frac{1}{6}e^{3x} + \frac{2}{9}e^{2x} \implies C_{2}(x) = \frac{1}{18} e^{3x} + \frac{1}{9} e^{2x}\\
    & C_{3}'(x) = \frac{1}{21}e^{-6x} + \frac{4}{63}e^{-7x} \implies C_{3}(x) = -\frac{1}{126}e^{-6x} - \frac{4}{441}e^{-7x} + C_{3}\\
    & Y_{SGEC} = C_{1}e^{-x}+ C_{2}e^{-3x} + C_{3}(x)e^{6x} =\\
    & = \left( -\frac{3}{14}e^{x} - \frac{2}{7}x + C_{1}  \right)e^{-x} + \left( \frac{1}{18}e^{3x} + \frac{1}{9}e^{2x} + C_{2}   \right)e^{-3x} + \left( -\frac{1}{126} e^{-6x} - \frac{4}{441}e^{-7x} + C_{3}  \right)e^{6x} =\\
    & = C_{1}e^{-x} + C_{2}e^{-3x} + C_{3}e^{6x} + \left( -\frac{1}{6} + \left( \frac{5}{49} - \frac{2}{7}x \right)e^{-x}   \right)\\
    & Y_{p2} = x(B e^{-x} )\\
    & S_{1}(x) = 3 \implies y_{p1} = A\\
\end{split}
$$

