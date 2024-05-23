---
id: 1714841859-ejercicio-6-tema-5-ecuaciones-diferenciales
aliases:
  - Ejercicio 6 tema 5 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Determina los [[1714749330-punto-crtico-de-un-sistema-autnomo|puntos críticos]] del siguiente sistema y analiza su estabilidad o inestabilidad:

$$
\begin{cases}
    & x' = 2x + y \\
    & y' = 2x - y
\end{cases}
$$

Autovalores:

$$
\begin{split}
    & \begin{vmatrix}
        2-\lambda & 1 \\
        2 & -1-\lambda
    \end{vmatrix} = 0 \\
    & (2-\lambda)(-1-\lambda) - 2 = 0 \\
    & -2 - 2\cdot \lambda  + \lambda + \lambda^2 - 2 = 0 \implies\\
    & \lambda^2 - \lambda - 4 = 0 \implies\\
    & \lambda = \frac{1 \pm \sqrt{1 + 16}}{2} \implies\\
    & \lambda_{1} = \frac{1 + \sqrt{17}}{2}, \; \lambda_{2} = \frac{1 - \sqrt{17}}{2}
\end{split}
$$

Se trata de un punto silla ya que uno de los autovalores es positivo y el otro negativo.

Autovectores asociados a $\lambda_{1} = \frac{1 + \sqrt{17}}{2}$:

$$
\begin{split}
    & \begin{pmatrix}
        & 2 - \left( \frac{1 + \sqrt{17}}{2} \right) & 1 \\
        & 2 & -1 - \left( \frac{1 + \sqrt{17}}{2} \right)
    \end{pmatrix} \sim\\
    & \begin{pmatrix}
        & \frac{3 - \sqrt{17}}{2} & 1 \\
        & 1 & \frac{-3 -\sqrt{17}}{4}
    \end{pmatrix} \sim\\
    & \begin{pmatrix}
        & 1 & \frac{-3 - \sqrt{17}}{4} \\
        & \frac{3 - \sqrt{17}}{2} & 1
    \end{pmatrix} \sim\\
    & \begin{pmatrix}
        & 1 & -\frac{3 - \sqrt{17}}{4} \\
        & 0 & \frac{-3 + \sqrt{17}}{2}\cdot \frac{-3 - \sqrt{17}}{4} + 1
    \end{pmatrix} =\\
    & \begin{pmatrix}
        & 1 & -\frac{3 - \sqrt{17}}{4} \\
        & 0 & \frac{9 - 17}{8} + 1
    \end{pmatrix} =\\
    & \begin{pmatrix}
        & 1 & -\frac{3 - \sqrt{17}}{4} \\
        & 0 & 0
    \end{pmatrix} \implies
    B_{S_{\lambda = \frac{1 + \sqrt{17}}{2}}} = \left\{ \left( 1, \frac{-3 + \sqrt{17}}{4}\right)\right\} =\\
    & = \left\{ \left( \frac{3 - \sqrt{17}}{2}, -\frac{3 - \sqrt{17} }{2}\cdot \frac{3 - \sqrt{17}}{4} \right)  \right\} = \\
    & =\left\{ \left( \frac{3 - \sqrt{17}}{2}, -\frac{9 - 17}{8} \right) \right\} = \left\{ \left( \frac{3 - \sqrt{17}}{2}, 1 \right) \right\} 
\end{split}
$$

Autovectores asociados a $\lambda_{2} = \frac{1 - \sqrt{17}}{2}$:

$$
\begin{split}
    & \begin{pmatrix}
        & 2 - \left( \frac{1 - \sqrt{17}}{2} \right) & 1 \\
        & 2 & -1 - \left( \frac{1 - \sqrt{17}}{2} \right)
    \end{pmatrix} \sim\\
    & \begin{pmatrix}
        & \frac{3 + \sqrt{17}}{2} & 1 \\
        & 2 & \frac{-3 + \sqrt{17}}{2}
    \end{pmatrix} \sim\\
    & \begin{pmatrix}
        & \frac{3 + \sqrt{17}}{2} & 1 \\
        & 0 & -\frac{4}{3 + \sqrt{17}} + \frac{-3 + \sqrt{17}}{2}
    \end{pmatrix} =\\
    & \begin{pmatrix}
        & \frac{3 + \sqrt{17}}{2} & 1 \\
        & 0 & \frac{-8 + (-3 + \sqrt{17})(3 + \sqrt{17})}{2(3 + \sqrt{17})}
    \end{pmatrix} =\\
    & \begin{pmatrix}
        & \frac{3 + \sqrt{17}}{2} & 1 \\
        & 0 & \frac{-8 - 9 + 17}{2(3 + \sqrt{17})}
    \end{pmatrix} =\\
    & \begin{pmatrix}
        & \frac{3 + \sqrt{17}}{2} & 1 \\
        & 0 & 0
    \end{pmatrix} \implies\\
    & B_{S_{\lambda = \frac{1 - \sqrt{17}}{2}}} = \left\{ \left( \frac{3 + \sqrt{17} }{2}, 1 \right)\right\}
\end{split}
$$

Eucación:

$$
\begin{split}
    & \frac{dy}{dx} = \frac{2x-y}{2x+y}
\end{split}
$$
