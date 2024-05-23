---
id: 1710152250-ejercicio-10-ecuaciones-diferenciales-de-orden-superior
aliases:
  - Ejercicio 10 ecuaciones diferenciales de orden superior
tags:
  - ecuaciones-diferenciales
---

# Resuelve la ecuación ${y'' + 2y' +y=0}$

$$
\begin{split}
    & r^2 + 2r + 1 = 0 \implies \ldots  \implies r=-1 \text{ (doble)}\\
    & y = C_{1}e^{-x}+C_{2}\cdot x\cdot e^{-x} \implies y' = -C_{1}e^{-x} + C_{2}(e^{-x} -xe^{-x})=\\
    & = -C_{1}e^{-x} + C_{2}e^{-x}(1-x)\implies\\
    & \implies y'' = C_{1}e^{-x} - C_{2}e^{-x}(1-x) +C_{2}e^{-x}(-1)=C_{1}e^{-x} C_{2}e^{-x}(-1+x-1)\\
    & y'' = C_{1}e^{-x} +(x-2)e^{-x}\\
    & y=0 \implies C_{1}e^{-x} + (x-2) e^{-x} - 2C_{1}e^{-x} + 2C_{2}e^{-x}(1-x)+C_{1}e^{-x}+C_{2}xe^{-x}=0      
\end{split}
$$
