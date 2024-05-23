---
id: 1715850969-ejercicio-factorial-matemtica-discreta-ii
aliases:
  - Cuantos ceros tiene $170!$
tags:
  - matemática-discreta-II
---

# Cuantos ceros tiene $170!$

Para saber cuantos ceros tiene un número factorial, se debe dividir el número por $5$ y contar cuantas veces se puede hacer esta división. Luego se divide el resultado por $5$ y se cuenta cuantas veces se puede hacer esta división. Se sigue este proceso hasta que el resultado sea menor que $5$. Finalmente se suman los resultados de las divisiones.

Para $170!$ se tiene:

$$
\begin{align*}
\left\lfloor \frac{170}{5} \right\rfloor &= 34 \\
\left\lfloor \frac{34}{5} \right\rfloor &= 6 \\
\left\lfloor \frac{6}{5} \right\rfloor &= 1 \\
\left\lfloor \frac{1}{5} \right\rfloor &= 0 \\
\end{align*}
$$

Por lo tanto, $170!$ tiene $34+6+1=41$ ceros.

