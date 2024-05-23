---
id: 1710756414-ejercicio-26-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 26 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Resuelve la ecuación ${y'' - 3y' + 2y = e^{x}\sin (x) }$

1. SGEH:

$$
\begin{split}
    & y'' - 3y' + 2y = 0 \implies r^2 - 3r + 2 = 0 \implies \begin{cases} r_1 = 1 \\ r_2 = 2 \end{cases} \implies \\
    & \implies y_{SGEH} = c_1e^{x} + c_2e^{2x}\\
\end{split}
$$

2. SGEC / SPEC:

$$
\begin{split}
    & \begin{cases}
        & C_{1}'(x) y_1(x) + C_{2}'(x)y_{2}(x) = 0\\
        & C_1'(x) y_{1}'(x) + C_{2}'(x) y_{2}'(x) = S(x)
    \end{cases} \implies 
    \begin{cases}
        & C_{1}'(x) e^{x} + C_{2}'(x)e^{2x} = 0\\
        & C_1'(x) e^{x} + 2C_{2}'(x)e^{2x} = e^{x}\sin(x)
    \end{cases} \implies \\
    & \implies C_{2}'(x) e^{2x} = e^{x}\sin (x) \implies C_{2}'(x) = e^{-x}\sin (x)  \implies C_{2}(x) = \int e^{-x} \sin (x) dx = I\\
    & I = \int  e^{-x} \sin(x) dx =
    \begin{cases}
        & u = \sin (x) \implies du = \cos (x)dx\\
        & dv = e^{-x}dx \implies v = -e^{-x} =
        \end{cases}
        -e^{x}\sin (x) + \int e^{-x}\cos (x)dx =\\
        & = \begin{cases}
            & u = \cos (x) \implies du = -\sin (x)dx\\
            & dv = e^{-x}dx \implies v = -e^{-x}  
        \end{cases} = -e^{-x}\sin (x)-e^{-x}\cos (x) - \int e^{-x}\sin (x)dx \implies\\
        & \implies 2I = -e^{-x}(\sin(x) + \cos (x)) + K_{2} \implies I = C_{2}(x) = \frac{-e^{-x}}{2}( \sin(x) + \cos (x)) + C_{2}\\
        & C_{1}'(x) e^{x} + C_{2}'(x) e^{2x} = 0 \implies C_{1}'(x) = -C_{2}'(x) \frac{e^{2x} }{e^{x} } \implies\\
        & \implies C_{1}'(x) = (-e^{-x}\sin (x) )e^{x} = -\sin (x) \implies C_{1}(x) = \cos (x) + C_{1} \\
        & Y_{SPEC} = \frac{1}{2} e^{x} \cos (x) - \frac{1}{2} e^{x}\sin (x)     
\end{split}
$$

