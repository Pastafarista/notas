---
id: 1710275962-ejercicio-4-examen-parcial-lgebra
aliases:
  - Ejercicio 4 examen parcial álgebra
tags:
  - álgebra
---

# Dados los vectores u, v u w

$$
\begin{split}
    & \vec{u} = (-1, 2, -1)\\
    & \vec{v} = (3, -1, 1)\\
    & \vec{w} = (a, 0, 1)
\end{split}
$$

1. Hallar el valor de $a$ para que los [[1709799641-vector-fijo|vectores]] sean [[1709800386-vectores-linealmente-independientes|linealmente independiente]]

La manera más rápida de comprobar si tres vectores son independientes es con el [[1708976016-determinante|determinante]] ya que si es igual a cero, los vectores son linealmente dependientes. Entonces:

$$
\begin{split}
    & \begin{vmatrix}
        -1 & 2 & -1\\
        3 & -1 & 1\\
        a & 0 & 1
    \end{vmatrix} = 
    \begin{vmatrix}
    5 & 0 & 1\\
    3 & -1 & 1\\
    a & 0 & 1
    \end{vmatrix} =
    - \begin{vmatrix}
    5 & 1\\
    a & 1
    \end{vmatrix} = 5 - a = 0 \iff a = 5
\end{split}
$$

2. Hallar el área del triángulo que tiene por aristas $\vec{u}$ y $\vec{v}$

Si recordamos, el [[1709799713-mdulo-de-un-vector|módulo]] del [[1709828386-producto-vectorial|producto vectorial]] nos da el área del paralelogramo que forman dos vectores. Si dividimos ese área entre dos, obtendremos el área del triángulo. Entonces:

Calculamos el producto vectorial de $\vec{u}$ y $\vec{v}$:

$$
\begin{split}
    & \vec{u} \times \vec{v} = 
    \begin{vmatrix}
    \vec{i} & \vec{j} & \vec{k}\\
    -1 & 2 & -1\\
    3 & -1 & 1
    \end{vmatrix} = 
    2\vec{i} + \vec{k} - 3\vec{j} - 6\vec{k} - \vec{i} + \vec{j} = 
    \vec{i} - 2\vec{j} - 5\vec{k} \equiv (1, -2, -5)\\
\end{split}
$$

Entonces el área del triángulo será:

$$
\frac{\|(1,-2,-5)\|}{2} = \frac{\sqrt{1^2 + (-2)^2 + (-5)^2}}{2} = \frac{\sqrt{1 + 4 + 25}}{2} = \frac{\sqrt{30}}{2} = \frac{\sqrt{30}}{2} \approx 2.74
$$

![[ej4-parcial-álgebra.png]]


