---
id: 1714844915-ejercicio-7-tema-5-ecuaciones-diferenciales
aliases:
  - Ejercicio 7 tema 5 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Determina los [[1714749330-punto-crtico-de-un-sistema-autnomo|puntos críticos]] del siguiente sistema y analiza su estabilidad o inestabilidad:

$$
\begin{cases}
    & x' = -2x \\
    & y' = -2y
\end{cases}
$$

Puntos críticos:

- El único punto crítico es el origen $(0, 0)$.

Autovalores:

$$
\begin{split}
    & \begin{vmatrix}
        -2-\lambda & 0 \\
        0 & -2-\lambda
    \end{vmatrix} = 0 \\
    & (-2-\lambda)(-2-\lambda) = 0 \\
    & \lambda_1 = -2, \lambda_2 = -2
\end{split}
$$

Se trata de una estrella estable ya que ambos autovalores son negativos e iguales, y además la matriz es diagonalizable.

Autovectores asociados a $\lambda_1 = -2$:

$$
\begin{split}
    & \left(\begin{array}{cc|c}
        0 & 0 & 0 \\
        0 & 0 & 0
    \end{array}\right) \implies\\
    & B_{S_{\lambda = -2}} = \{ (1, 0), (0, 1) \}
\end{split}
$$

Por lo tanto:

$$
\begin{split}
    & \binom{x}{y} = C_1 \binom{1}{0} e^{-2t} + C_2 \binom{0}{1} e^{-2t} \implies\\
    & \begin{cases}
        & x = C_1 e^{-2t} \\
        & y = C_2 e^{-2t}
    \end{cases}\\
    & t \to \infty \implies (x,y) \to (0,0)
\end{split}
$$

Eucuación:

$$
\begin{split}
    & \frac{dy}{dx} = \frac{y}{x} \implies\\
    & \ln |y| = \ln |x| + C \implies\\
    & y = C\cdot x
\end{split}
$$
