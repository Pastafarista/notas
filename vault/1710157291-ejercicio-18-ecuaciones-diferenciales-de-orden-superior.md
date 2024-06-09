---
id: 1710157291-ejercicio-18-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 18 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Resuelve la ecuación ${y'' + y = x}$ utilizando el método de coeficientes indeterminados.

1. SGEH:

$$
\begin{split}
    & y'' + y = 0\\
    & r^2 + 1 = 0 \implies r \pm i \implies Y_{SGEH} = C_{1}\sin (x) + C_{2}\cos (x)\\
\end{split}
$$

2. SPEC:

$$
\begin{split}
    & S(x) = e^{\alpha x}(P_m(x) \sin (\beta x) + Q_n(x)\cos (\beta x))\\
    & S(x) = x \implies
    \begin{cases}
        & \alpha = 0\\
        & \beta = 0\\
        & P_m(x) = 0 \implies m=0\\
        & Q_n(x) = 1 \implies n=0\\
    \end{cases} \implies t=0, \;\; k=0 \implies\\

    & \implies y_{p} = Ax + B \implies y_{p}' = A \implies y_{p}'' = 0\\
    & y'' + y' = x \implies 0 + Ax + B = x \implies 
    \begin{cases}
        & A = 1\\
        & B = 0\\
    \end{cases} \implies y_{p} = x\\
    & Y_{SGEC} = Y_{SGEH} + Y_{SPEC} = C_{1}\sin (x) + C_{2}\cos (x) + x 
\end{split}
$$
