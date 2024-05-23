---
id: 1707917956-ejercicio-16-ecuaciones-diferenciales-de-primer-orden
aliases:
  - Ejercicio 16 ecuaciones diferenciales de primer orden
  - Resuelve ${(e^{x+y} - y)dx + (xe^{x+y} + 1)dy = 0}$ encontrando el factor integrante adecuado
tags:
  - ecuaciones-diferenciales
---

# Resuelve ${(e^{x+y} - y)dx + (xe^{x+y} + 1)dy = 0}$ encontrando el factor integrante adecuado

Primero vamos a ver si es una ecuación de tipo [[1707912287-ecuaciones-diferenciales-exactas|diferencial exacta]]:

$$\begin{split}
    & M(x,y) = e^{x+y} - y \;\;, N(x,y) = xe^{x+y} + 1\\
    & \frac{\partial M}{\partial y} = e^{x+y} - 1 \;\;, \frac{\partial N}{\partial x} = e^{x+y} + xe^{x+y} = (x+y)e^{x+y}\\
    & \implies \text{No es exacta}
\end{split}$$

Ahora vamos a encontrar el factor integrante adecuado:

$$\begin{split}
    & \frac{M_y(x,y) - N_x(x,y)}{N(x,y)} = -1 = f(x) \implies\\
    & \implies \mu = \mu(x) \implies \cdots \implies \mu(x) = e^{-x}\\
    & \frac{N_x(x,y) - M_y(x,y)}{M(x,y)} = \frac{(x+1)e^{x+y} - (e^{x+y} - 1)}{e^{x+y} - y} =\\
    & = \frac{xe^{x+y} - 1}{e^{x+y}-y} \neq g(y)\\
\end{split}$$

Escogemos el factor integrante $\mu(x) = e^{-x}$:

$$\begin{split}
    & e^{-x}(e^{x+y} - y)dx + e^{-x}(xe^{x+y} + 1)dy = 0 \implies\\
    & \implies (e^{y} - ye^{-x})dx + (xe^{y} + e^{-x})dy = 0\\
\end{split}$$

Comprobamos que ahora la ecuación es exacta:

$$\begin{split}
    & e^{-x}(e^{x+y} - y)dx + e^{-x}(xe^{x+y} + 1)dy = 0 \implies\\
    & \implies (e^{y} - ye^{-x})dx + (xe^y + e^{-x})dy = 0\\
    & \frac{\partial P(x,y)}{\partial y} = e^y - e^{-x}\\
    & \frac{\partial Q(x,y)}{\partial x} = e^y - e^{-x}\\
    & \implies \text{La ecuación es exacta}
\end{split}$$

Ahora vamos a resolver la ecuación:

$$\begin{split}
    & \frac{\partial F(x,y)}{\partial x} = P(x,y) \implies F(x,y) = \int P(x,y) dx + C(y) \implies \\
    & \implies F(x,y) = \int(e^y - ye^{-x})dx + C(y) = xe^y + ye^{-x} + C(y)\\
    & \frac{\partial F(x,y)}{\partial y} = Q(x,y) \implies xe^y + e^{-x} + C'(y) = \\
    & = xe^y + e^{-x} \implies C'(y) = 0 \ inplies C(y) = C \\
    & F(x,y) = xe^y + ye^{-x} + C = 0\\
\end{split}$$
