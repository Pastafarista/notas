---
id: 1715595745-ejercicio-4-examen-3-ecuaciones-diferenciales
aliases:
  - Ejercicio 4 examen 3 ecuaciones diferenciales
tags:
  - ecuaciones-diferenciales
---

# Determina los puntos críticos del siguiente sistema, analiza su tipo para uno de ellos, obtén la ecuación de las trayectorias y finalmente dibuja de forma aproximada el diagrama de fases asociado al sistema.

$$
\begin{cases}
    x' = y^2 - xy\\
    y' = x^2 - xy
\end{cases}
$$

Puntos críticos:

$$
\begin{split}
    & \begin{cases}
        x_{0}' = 0\\
        y_{0}' = 0
    \end{cases} \implies \begin{cases}
        y^2 - xy = 0\\
        x^2 - xy = 0
    \end{cases} \implies
    \begin{cases}
        y(y - x) = 0\\
        x(x - y) = 0
    \end{cases} \implies y = x
\end{split}
$$

Usaremos el punto crítico $(0, 0)$ para analizar su tipo:

$$
\begin{split}
    & \begin{cases}
        g_{1}(x,y) = y^2 - xy\\
        g_{2}(x,y) = x^2 - xy
    \end{cases}\\
    & \frac{\partial g_{1}}{\partial x}(x,y) = -y\\
    & \frac{\partial g_{1}}{\partial x}(x,y) = 2x - y\\
    & \frac{\partial g_{2}}{\partial x}(x,y) = 2x - y\\
    & \frac{\partial g_{2}}{\partial x}(x,y) = -x
\end{split} 
$$

Entonces si hacemos el jacobiano:

$$
\begin{split}
    & J_g(x,y) = \begin{pmatrix}
        -y & -x\\
        2x - y & -x
    \end{pmatrix} \implies\\
    & \begin{pmatrix}
        0 & 0\\
        0 & 0\\
    \end{pmatrix} = B
\end{split}
$$

$b=0\implies$ tipo centro.

Trayectorias:

$$
\begin{split}
    & \frac{dy}{dx} = \frac{\frac{dy}{dt}}{\frac{dx}{dt}} = \frac{x^2 - xy}{y^2 - xy} = \frac{x(x - y)}{y(y - x)}\\
    & \frac{dy}{dx} = -\frac{x}{y} \implies ydy = -xdx \implies y^2 = -x^2 + C \implies\\
    & \implies x^2 + y^2 = C \implies \text{circunferencias}
\end{split}
$$
