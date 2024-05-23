---
id: 1710759257-ejercicio-29-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 29 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Resuelve la ecuación $y''' + y' = \sec (x)$ utilizando el método de variación de constantes

1. SGEH:

$$
\begin{split}
    & y''' + y' = 0 \implies r^3  + r = 0 \implies r(r^3  + 1) = 0 \implies \begin{cases} & r = 0\\ r = \pm i\end{cases} =\\
    = C_{1}+ C_{2}\sin (x) + C_{3}\cos (x)
\end{split}
$$

2. SGEC / SPEC:

$$
\begin{split}
    & y = C_{1}(x) + C_{2}(x) \sin (x) + C_{3}\cos (x)\\
    & \begin{cases}
        & C_{1}'(x)y_{1}(x) + C_{2}'(x)y_{2}(x) + C_{3}'(x)y_{3}(x) = 0\\
        & C_{1}'(x)y_{1}'(x) + C_{2}'(x)y_{2}'(x) + C_{3}'(x)y_{3}'(x) = 0\\
        & C_{1}'(x)y_1''(x) + C_{2}'(x)y_2''(x) + C_{3}'(x)y_{3}''(x) = S(x)
    \end{cases} \implies\\
    & \begin{cases}
        & C_{1}'(x) + C_{2}'(x)\sin (x) + C_{3}'(x)\cos (x) = 0\\
        & 0 + C_{2}'(x)\cos (x) - C_{3}'(x)\sin (x) = 0\\
        & 0 - C_{2}'(x)\sin (x) - C_{3}'(x)\cos (x) = \frac{1}{\cos (x)}
    \end{cases} \implies\\
    & \implies \begin{cases}
        & C_{1}'(x) = \frac{1}{\cos (x)} = C_{1}(x) = \int \frac{1}{\cos (x)}dx = \begin{cases} & t = \sin (x)\\ & dt = \cos (x)dx\end{cases} = \int \frac{dt}{\cos ^2(x)} = \int \frac{dt}{1 - t^2} = \int  \left( \frac{\frac{1}{2}}{1 + t} + \frac{\frac{1}{2}}{1 - t}\right) = \frac{1}{2}\ln |1+t| - \frac{1}{2} \ln |1-t| + C_{1} = \ln \sqrt{\frac{1 + \sin (x)}{1 - \sin (x)}} + C_{1}  \\
        & C_{2}'(x) = -\frac{\sin (x)}{\cos (x)} \implies C_{2}(x) -\int \frac{\sin (x)}{\cos (x)} dx = -\ln |\cos (x)| + C_{2}\\
        & C_{3}'(x) = -1 \implies C_{3}(x) = -x + C_{3}
    \end{cases}\\
    & y = C_{1}(x)+ C_{2}\sin (x) + C_{3}(x)\cos (x) = \left( \ln \sqrt{\frac{1 + \sin (x)}{1 - \sin (x)}} + C_{1}  \right) + \left( -\ln |\cos (x)| + C_{2} \right)\sin (x) + (-x + C_{3})\cos (x) =\\
    & = C_{1} + C_{2}\sin (x) + C_{3}\cos (x) + \ln \sqrt{\frac{1+\sin (x)}{1 - \sin (x)}} - (\ln |\cos (x)|)\sin (x) - x\cos (x)\\
    & SGEH \equiv C_{1} + C_{2}\sin (x) + C_{3}\cos (x)\\
    & SPEC \equiv \ln \sqrt{\frac{1+\sin (x)}{1 - \sin (x)}} - (\ln |\cos (x)|)\sin (x) - x\cos (x)
\end{split}
$$
