---
id: 1708338607-ejercicio-ecuaciones-diferenciales-examen-mayo-2022
aliases:
  - Ejercicio ecuaciones diferenciales examen mayo 2022
  - Dada la ecuación ${(x^2 - 2xy) + (xy - 2y^2)y' = 0}$ completa los siguientes apartados
tags:
  - ecuaciones-diferenciales
---

# Dada la ecuación ${(x^2 - 2xy) + (xy - 2y^2)y' = 0}$ completa los siguientes apartados

1. Demuestra que la ecuación tiene un factor integrante que depende de $x-2y$

${(x^2 - 2xy) + (xy - 2y^2)y' = 0 \implies (x^2 -2xy)dx + (xy - 2y^2)dy = 0}$ con $z = x - 2y$

Comprobamos si es [[1707912287-ecuaciones-diferenciales-exactas|exacta]]

$$\begin{cases}
    & \frac{\partial M(x,y)}{\partial y} =  -2x\\
    & \frac{\partial N(x,y)}{\partial x} = y \\
\end{cases} \implies \text{no es exacta}$$

Calculamos un factor integrante

$$\begin{split}
    & \mu(x,y)(x^2 - 2xy)dx + \mu(x,y)(xy - 2y^2)dy = 0\\
    & \frac{\partial P(x,y)}{\partial y} = \frac{\partial Q(x,y)}{\partial x} \implies \frac{\partial}{\partial y} (\mu(x,y) (x^2 - 2xy)) = \frac{\partial}{\partial x}(\mu(x,y) (xy - 2y^3)) \implies \\
    & \implies \frac{\partial \mu(z)}{\partial y} (x^2 - 2xy) + \mu(z)(-2x) = \frac{\partial \mu(z)}{\partial x}(xy - 2y^3) + \mu(z) y \implies \\
    & \implies \frac{d \mu(z)}{dz}\frac{\partial z}{\partial y}(x^2 - 2xy) + \mu(z)(-2x) = \frac{d \mu(z)}{dz} \frac{\partial z}{\partial x}(xy - 2y^3) + \mu(z) y \implies \\
    & \implies \frac{d \mu}{dz}(-2)(x^2 - 2xy) + \mu (-2x) = \frac{d \mu}{dz}(1)(xy - 2y^3) + \mu y \implies \\
    & \implies z = x - 2y \implies \frac{d \mu}{dz}(-2x^2 + 4xy - xy + 2y^2) = \mu(y + 2x) \implies \\
    & \implies \frac{d\mu}{dz}(-2x^2 + 3xy + 2y^2) = \mu(y + 2x) \implies\\
    & \implies - \frac{d \mu}{dz} z = \mu \implies \frac{1}{\mu}d\mu = \frac{-1}{z}dz \implies \\
    & \implies \int \frac{1}{\mu}d\mu = -\int \frac{1}{z}dz \implies ln|\mu| = - ln|z| + C_1 \implies \\
    & \implies e^{ln|\mu|} = e^{-ln|z| + C_1} \implies e ^{ln|\mu|} = C_2 e^{(ln|z|)^{-1}} \implies \\
    & \implies |\mu| = C_2 \frac{1}{|z|} \implies \mu(z) = \frac{1}{z} \implies \mu(x,y) = \frac{1}{x-2y}\\
\end{split}$$

Ahora usamos el factor integrante para resolver la ecuación

$$\begin{split}
    & (x^2 - 2y)dx + (xy - 2y^2)dy = 0 \implies \frac{1}{x -2y} x(x-2y) + \frac{1}{x-2y}y(x-2y)dy = 0 \implies \\ 
    & \implies x dx + y dy = 0 \implies \cdots \implies x^2 + y^2 = k\\
\end{split}$$

2. Resuelve la ecuación con la condición inicial $y(0) = 1$

$$\begin{split}
    & y(0) = 1 \implies 0^2 + 1^2 = k \implies k = 1 \implies x^2 + y^2 = 1\\
\end{split}$$

3. ¿Existe alguna solución singular?

$$\begin{split}
    & z = 0 \implies x - 2y = 0 \implies y = \frac{x}{2} \implies\\
    & \implies \text{es una solución singular}
\end{split}$$
