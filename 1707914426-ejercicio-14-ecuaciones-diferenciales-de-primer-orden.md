---
id: 1707914426-ejercicio-14-ecuaciones-diferenciales-de-primer-orden
aliases:
  - Ejercicio 14 ecuaciones diferenciales de primer orden
  - Resuelve la ecuación diferencial ${(1-x^2y)dx + x^2(y-x)dy = 0}$ sabiendo que admite un factor integrante de la forma $\mu = \mu(x)$
tags:
  - ecuaciones-diferenciales
---

# Resuelve la [[1706869334-ecuacin-diferencial|ecuación diferencial]] ${(1-x^2y)dx + x^2(y-x)dy = 0}$ sabiendo que admite un factor integrante de la forma $\mu = \mu(x)$

$$\begin{split}
    & M(x,y) = 1-x^2y \;\;, N(x,y) = x^2(y-x)\\
    & \frac{\partial M}{\partial y} = -x^2 \;\;, \frac{\partial N}{\partial x} = 2xy - 3x^2\\
    & \implies \text{No es exacta}
\end{split}$$


Primero vamos a hacer una demostración:

$$\begin{split}
    & \frac{\partial P(x,y)}{\partial y} = \frac{\partial Q(x,y)}{\partial x} \implies \frac{\partial}{\partial y} (\mu(x,y) \cdot M(x,y)) = \frac{\partial}{\partial x} (\mu(x,y) \cdot N(x,y)) \implies \\
    & \implies \frac{\partial \mu(x,y)}{\partial y} M(x,y) + \mu(x,y) \frac{\partial M(x,y)}{\partial y} = \frac{\partial}{\partial x}\mu(x,y) \cdot N(x,y) + \mu(x,y) \cdot \frac{\partial N(x,y)}{\partial x} \implies \\
    & \implies \mu(x,y) \left( \frac{\partial M(x,y)}{\partial y} \cdot \frac{\partial N(x,y)}{\partial x}\right) = \frac{\partial \mu(x,y)}{\partial x} N(x,y) - \frac{\partial \mu(x,y)}{\partial y} M(x,y) \implies \\
    & \implies \frac{1}{\mu(x,y)} = \frac{\frac{\partial M(x,y)}{\partial y} - \frac{\partial N(x,y)}{\partial x}}{\frac{\partial \mu(x,y)}{\partial x} \cdot N(x,y) - \frac{\partial \mu(x,y)}{\partial y} \cdot M(x,y)} = \frac{M_y - N_x}{M_x \cdot N - M_y \cdot M} = \frac{N_x - M_y}{\mu_y \cdot M - \mu_x \cdot N}\\
    & \text{Caso 1:} \mu = \mu(x) \implies \frac{1}{\mu} = \frac{N_x - M_y}{- \frac{du}{dx} \cdot N} \implies \frac{1}{\mu}\cdot d_\mu= \frac{M_y - N_x}{N}dx\\
    & \text{Caso 2:} \mu = \mu(y) \implies \frac{1}{\mu} = \frac{N_x - M_y}{\frac{d\mu}{dy}\cdot M} \implies \frac{1}{\mu} \cdot d\mu = \frac{N_x - M_y}{M}dy  \\
    & \text{Caso 3:} \mu = \mu(z), \; z = f(x,y) \implies \frac{1}{\mu} = \frac{N_x - M_y}{\frac{d\mu}{dz} \cdot \frac{\partial z}{\partial y} \cdot M - \frac{d\mu}{dz}\cdot \frac{\partial z}{\partial x} \cdot N} = \\
    & = \frac{N_x - M_y}{\frac{d\mu}{dz} \left( \frac{\partial z}{\partial y} \cdot M - \frac{\partial \mu}{\partial x}\cdot N\right)} \implies \frac{1}{\mu} \cdot d\mu = \frac{N_x - M_y}{\frac{\partial z}{\partial y} \cdot M - \frac{\partial \mu}{\partial x} \cdot N }dz
\end{split}$$

Vamos a convertir la ecuación diferencial a una [[1707912287-ecuaciones-diferenciales-exactas|diferencial exacta]]:

$$\begin{split}
    & \frac{\partial P(x,y)}{\partial y} = \frac{\partial Q(x,y)}{\partial x} \implies \mu(x) (-x^2) = \mu'(x)(x^2y - x^3) + \mu(x) (2xy - 3x^2), \; \mu'(x) = \frac{d \mu}{dx} \implies \\
    & \implies \mu(x)(-x^2 - 2xy + 3x^2) = \mu ' (x)(x^2y - x^3) \implies \\
    & \implies \frac{1}{\mu} d\mu = \frac{2x^2 - 2xy}{x^2y - x^3}dx = \frac{2x(x-y)}{x^2(y-x)}dx = \frac{-2}{x}dx\\
    & \int \frac{1}{\mu} d\mu = \int -\frac{2}{x}dx \implies \ln|\mu| = -2\ln|x| + C \implies e^{\ln|\mu|} = e^{ln|x|^{-2}}\cdot e^C \implies \\
    & \implies |\mu| = \frac{1}{|x^2|}\cdot K \implies \mu(x) = \frac{1}{x^2}
\end{split}$$

A continuación, comprobaremos que ahora la ecuación es exacta:

$$\begin{split}
    & \frac{1}{x^2}(1 - x^2y)dx + \frac{1}{x^2}(x^2 y - x^3)dy = 0 \implies (\frac{1}{x^2} - y)dx + (y - x)dy = 0\\
    & \frac{\partial P(x,y)}{\partial y} = -1 = \frac{\partial Q(x,y)}{\partial x}
\end{split}$$

Por último, resolvemos la ecuación:

$$\begin{split}
    & \frac{\partial F(x,y)}{\partial x} = P(x,y) \implies F(x,y) = \int P(x,y)dx + C(y) =\\
    & = \int \left(\frac{1}{x^2} - y\right)dx + C(y) = -\frac{1}{x} - xy + C(y)\\
    & \frac{\partial F(x,y)}{\partial y} = Q(x,y) \implies -x + C'(y) = y - x \implies C'(y) = \frac{y^2}{2} + C \implies\\
    & \implies F(x,y) = -\frac{1}{x} - xy + \frac{y^2}{2} + C = 0\\
\end{split}$$
