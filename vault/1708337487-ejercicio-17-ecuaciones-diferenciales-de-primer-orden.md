---
id: 1708337487-ejercicio-17-ecuaciones-diferenciales-de-primer-orden
aliases:
  - Ejercicio 17 ecuaciones diferenciales de primer orden
  - Resuelve la ecuación $y^2 + (xy + 1)y'=0$ sabiendo que admite un factor integrante que es función de $xy$
tags: []
---

# Resuelve la [[1706869334-ecuacin-diferencial|ecuación]] $y^2 + (xy + 1)y'=0$ sabiendo que admite un factor integrante que es función de $xy$

$$\begin{split}
    & \mu = \mu(xy)\\
    & y^2 + (xy + 1)y' = 0 \implies y^2dx + (xy + 1)dy = 0\\
    & \frac{\partial M(x,y)}{\partial y} = 2y\\
    & \frac{\partial N(x,y)}{\partial x} = y\\
    & \implies \text{No es exacta}
\end{split}$$

Vamos a encontrar el factor integrante adecuado:

$$\begin{split}
    & \mu = \mu(x,y) = \mu(z), \; z=xy\\
    & \mu(x,y)y^2 dx + \mu(x,y)(xy + 1)dy = 0\\
    & \frac{\partial P(x,y)}{\partial y} = \frac{\partial Q(x,y)}{\partial x} \implies \frac{\partial}{\partial y}(\mu(x,y)y^2) = \frac{\partial}{\partial x}(\mu(x,y)(xy + 1)) \implies \\
    & \implies \frac{\partial \mu(z)}{\partial y} y^2 + \mu(z)2y = \frac{\partial \mu(z)}{\partial x} (xy + 1) + \mu(z)y \implies \\
    & \implies \frac{\partial \mu(z)}{dz} \frac{\partial z}{\partial y} y^2 + \mu(z)2y = \frac{d \mu(z)}{dz} \frac{\partial z}{\partial x} (xy + 1) + \mu(z)y \implies \\
    & \implies \frac{d \mu}{dz} dxy^2 + \mu 2y = \frac{d \mu}{dz} y(xy + 1) + \mu y \implies \\
    & \implies \frac{d \mu}{dz} (xy^2 - xy^2 - y) = \mu(y - 2y) \implies \\
    & \implies \frac{d \mu}{dz} y = \mu y \implies \frac{1}{\mu} d \mu \implies \\
    & \implies \int \frac{1}{\mu} d \mu = \int y dz \implies ln|\mu| = z + C_1 \implies \\
    & \implies e^{ln|\mu|} = e^{z + C_1} \implies |\mu| = C_z e^z \implies \mu(z) = e^z = e^{xy}\\
\end{split}$$

Comprobamos que es el factor integrante adecuado (que la ecuación es [[1707912287-ecuaciones-diferenciales-exactas|exacta]])

$$\begin{split}
    & e^{xy}y^2 dx + e^{xy}(xy + 1)dy = 0\\
    & \frac{P(x,y)}{\partial y} = xe^{xy}y^2 + 2ye^{xy}\\
    & \frac{Q(x,y)}{\partial x} = ye^{xy}y^2 + 2ye^{xy}\\
    & \implies \text{Es exacta}
\end{split}$$

Resolvemos la ecuación:

$$\begin{split}
    & \frac{\partial F(x,y)}{\partial x} = P(x,y) \implies F(x,y) = \int P(x,y)dx + C(y) = \int y^2 e^{xy}dx + C(y) \implies \\
    & \implies F(x,y) = ye^{xy} + C(y)\\
    & \frac{\partial F(x,y)}{\partial y} = Q(x,y) \implies e^{xy} +xye^{xy} + C'(y) = xy e^{xy} + e^{xy} \implies C(y) = C\\
\end{split}$$
