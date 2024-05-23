---
id: 1707915893-ejercicio-15-ecuaciones-diferenciales-de-primer-orden
aliases:
  - Ejercicio 15 ecuaciones diferenciales de primer orden
  - Resuelve la ecuación diferencial ${ydx + 2xdy = 0}$ encontrando el factor integrante adecuado
tags:
  - ecuaciones-diferenciales
---

# Resuelve la [[1706869334-ecuacin-diferencial|ecuación diferencial]] ${ydx + 2xdy = 0}$ encontrando el factor integrante adecuado

Primero vamos a ver si es una ecuación de tipo [[1707912287-ecuaciones-diferenciales-exactas|diferencial exacta]]

$$\begin{split}
    & M(x,y) = y \;\;, N(x,y) = 2x\\
    & \frac{\partial M}{\partial y} = 1 \;\;, \frac{\partial N}{\partial x} = 2\\
    & \implies \text{No es exacta}
\end{split}$$

Ahora vamos a encontrar el factor integrante adecuado:

$$\begin{split}
    & \frac{M_y - N_x}{N} = \frac{1 - 2}{2x} = -\frac{1}{2x} \implies\\
    & \implies \mu = \mu(x) \implies \cdots \implies \mu(x) = \frac{1}{\sqrt{x}}\\
    & \frac{N_x - M_y}{M} = \frac{2 - 1}{y} = \frac{1}{y} = \mu(y) \implies\\
    & \implies \mu = \mu(y) \implies \cdots \implies \mu(y) = y\\
\end{split}$$

Vamos a usar el factor integrante \mu(y) = y, ya que es más sencillo:

$$\begin{split}
    & y^2 dx + 2xy dy = 0\\
\end{split}$$

Comprobamos que ahora la ecuación es exacta:

$$\begin{split}
    & \frac{\partial P(x,y)}{\partial y} = 2y = \frac{\partial Q(x,y)}{\partial x} \implies \text{Es exacta}
\end{split}$$

Resolvemos la ecuación:

$$\begin{split}
    & \frac{\partial F(x,y)}{\partial y} = Q(x,y) \implies F(x,y) = \int Q(x,y)dy + C(x) \implies\\
    & \implies F(x,y) = \int 2xy dy + C(x) = x^2y + C(x)\\
    & \frac{\partial F(x,y)}{\partial x} = P(x,y) \implies y^2 + C'(x) = y^2 \implies C'(x) = 0 \implies C(x) = C\\
\end{split}$$

Por lo tanto, la [[1707058998-solucin-de-una-ecuacin-diferencial-ordinaria|solución general]] de la ecuación diferencial es $F(x,y) = xy^2 + C = 0$
