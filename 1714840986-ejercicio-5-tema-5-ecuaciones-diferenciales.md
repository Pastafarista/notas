---
id: 1714840986-ejercicio-5-tema-5-ecuaciones-diferenciales
aliases:
  - Ejercicio 5 tema 5 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Determina los [[1714749330-punto-crtico-de-un-sistema-autnomo|puntos críticos]] del siguiente sistema y analiza su estabilidad o inestabilidad:

$$
\begin{cases}
    & x' = -x \\
    & y' = 4y
\end{cases}
$$

Autovalores:

$$
\begin{split}
    & \begin{vmatrix}
        -1-\lambda & 0 \\
        0 & 4-\lambda
    \end{vmatrix} = 0 \\
    & (-1-\lambda)(4-\lambda) = 0 \\
    & \lambda_1 = -1, \lambda_2 = 4
\end{split}
$$

Se trata de un punto silla ya que uno de los autovalores es positivo y el otro negativo.

Autovectores asociados a $\lambda_1 = -1$:

$$
\begin{split}
    & \begin{array}{cc|c}
        0 & 0 & 0 \\
        0 & 5 & 0
    \end{array} \\
    & B_{S_{\lambda = -1}} = \{ (0, 1) \}
\end{split}
$$

Autovectores asociados a $\lambda_2 = 4$:

$$
\begin{split}
    & \begin{array}{cc|c}
        -5 & 0 & 0 \\
        0 & 0 & 0
    \end{array} \\
    & B_{S_{\lambda = 4}} = \{ (1, 0) \}
\end{split}
$$

Por lo tanto:

$$
\begin{split}
    & \binom{x}{y} = C_1 \binom{0}{1} e^{-t} + C_2 \binom{1}{0} e^{4t} \\
    & \begin{cases}
        x = C_2 e^{4t} \\
        y = C_1 e^{-t}
    \end{cases}
\end{split}
$$

La ecuación se nos quedaría de la siguiente forma:

$$
\begin{split}
    & \frac{dy}{dx} = -\frac{4y}{x} \implies \frac{dy}{y} = -\frac{4dx}{x} \\
    & \int \frac{dy}{y} = -4 \int \frac{dx}{x} \\
    & \ln |y| = -4 \ln |x| + C \\
    & y = \frac{C}{x^4} 
\end{split}
$$
