---
id: 1710065932-ejercicio-2-tema-2-lgebra
aliases:
  - Ejercicio 2 tema 2 álgebra
tags:
  - álgebra
---

# Calcular el volumen del paralepípedo definido por 4 puntos

$$
A = (1,1,1), \, B=(3,1,4), \, C=(-2,-4,6) \text{ y } D=(-3,4,-1)
$$

Primero calculamos los vectores que definen el paralepípedo:

$$
\begin{split}
    & \vec{AB} = (3-1,1-1,4-1) = (2,0,3)\\
    & \vec{AC} = (-2-1,-4-1,6-1) = (-3,-5,5)\\
    & \vec{AD} = (-3-1,4-1,-1-1) = (-4,3,-2)
\end{split}
$$

![[ej2-tema-2-álgebra.png]]

Ahora sabiendo que el [[1710065520-producto-mixto|producto mixto]] es el volumen del paralepípedo, calculamos el producto mixto de los vectores $\vec{AB}, \vec{AC}, \vec{AD}$:

$$
\vec{AB}\cdot (\vec{AC} \times  \vec{AD}) =
\begin{vmatrix}
    2 & 0 & 3\\
    -3 & -5 & 5\\
    -4 & 3 & -2
\end{vmatrix} = -97
$$

Por lo tanto, el volumen del paralepípedo es 97 unidades cúbicas.

![[ej2-tema-2-álgebra-2.png]]
