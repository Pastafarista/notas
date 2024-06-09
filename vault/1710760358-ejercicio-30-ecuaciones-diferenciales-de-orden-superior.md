---
id: 1710760358-ejercicio-30-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 30 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Resuelve la ecuación $y''' - 3y' + 2y = -4e^{-x}$ utilizando el método de variación de constantes

1. SGEH:

$$
\begin{split}
    & y''' - 3y' + 2y = 0 \implies r^3  - 3r + 2 = 0 \implies \begin{cases} & r = -2\\ & r = 1 \; (doble)\end{cases} \implies Y_{SGEH} = C_{1}e^{x} + + C_{2}xe^{x} + C_{3}e^{-2x}
\end{split}
$$

2. SGEC / SPEC:

$$
\begin{split}
    & y = C_{1}(x)e^{x} + C_{2}(x)xe^{x} + C_{3}(x)e^{-2x}\\
    & \begin{cases}
        & C_{1}'(x)y_{1}(x) + C_{2}'(x)y_{2}(x) + C_{3}'(x)y_{3}(x) = 0\\
        & C_{1}'(x)y_{1}'(x) + C_{2}'(x)y_{2}'(x) + C_{3}'(x)y_{3}'(x) = 0\\
        & C_{1}'(x)y_1''(x) + C_{2}'(x)y_2''(x) + C_{3}'(x)y_{3}''(x) = S(x)
    \end{cases} \implies \\
    & \begin{cases}
        & C_{1}'(x)e^{x} + C_{2}'(x)xe^{x} + C_{3}'(x) e^{-2x} = 0\\
        & C_{1}'(x)e^{x} + C_{2}'(x)(x+1)e^{x} - 2C_{3}'(x) e^{-2x}=0\\
        & C_{1}'(x)e^{x} + C_{2}'(x)(x+2)e^{x} + 4C_{3}'(x) e^{-2x} = 4e^{-x}   
    \end{cases} \implies\\
    &\implies \begin{cases}
        & C_{1}'(x) = \frac{4}{3}(x + \frac{1}{3})e^{-2x} \implies C_{1}(x) = \int \frac{4}{3}\left( x + \frac{1}{3} \right) e^{-2x} dx  \\
        & C_{2}'(x) = C_{2}(x) = \int -\frac{4}{3}e^{-2x}dx = \frac{2}{3}e^{-2x} + C_{2} = \ldots = -\frac{1}{9}(6x + 5)e^{-2x} + C_{1}   \\
        & C_{3}'(x) = -\frac{4}{9}e^{x}  \implies C_{3}(x) = \int -\frac{4}{9}e^{x} dx = -\frac{4}{9}e^{x} + C_{3}  
    \end{cases}\\

    & Y_{SGEC} = C_{1}(x)e^{x} + C_{2}(x)xe^{x} + C_{3}(x)e^{-2x} =\\
    & = \left( -\frac{1}{9}(6x + 5)e^{-2x} + C_{1} \right)e^{x} + \left( \frac{2}{3}e^{-2x} + C_{2}  \right)x e^{x} + \left( -\frac{4}{9}e^{x} + C_{3}  \right)e^{-2x} = \\
    & = C_{1}e^{x} + C_{2}xe^{x} + C_{3}e^{-2x} - e^{-x}\\
    & s(x) = -4e^{-x} \implies y_p = Ae^{-x}  

\end{split}
$$

