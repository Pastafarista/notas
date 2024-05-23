---
id: 1709025451-expresin-matricial-de-un-sistema-de-ecuaciones
aliases:
  - Expresión matricial de un sistema de ecuaciones
  - Expresión matricial
  - Ecuaciones matriciales
  - Forma matricial
  - Ecuación matricial
  - Matriz asociada un sistema de ecuaciones
  - Matriz asociada
tags:
  - álgebra
---
****
# Expresión matricial de un sistema de ecuaciones

Dado el [[1709024526-sistema-de-ecuaciones-lineales|sistema de ecuaciones lineales]]:

$$\begin{cases}
a_{11}x_1 + a_{12}x_2 + \ldots + a_{1n}x_n = b_1 \\
a_{21}x_1 + a_{22}x_2 + \ldots + a_{2n}x_n = b_2 \\
\vdots \\
a_{m1}x_1 + a_{m2}x_2 + \ldots + a_{mn}x_n = b_m
\end{cases}$$

Se puede expresar de forma matricial como $AX = B$ donde $A$ es la [[1708971486-matriz|matriz]] de los coeficientes:

$$A = 
\begin{pmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{pmatrix}$$

y $X$ es la [[1708974518-matriz-columna|matriz columna]] de las incógnitas:

$$X =
\begin{pmatrix}
x_1 \\
x_2 \\
\vdots \\
x_n
\end{pmatrix}$$
