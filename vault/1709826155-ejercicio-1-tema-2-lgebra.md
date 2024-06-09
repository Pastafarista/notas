---
id: 1709826155-ejercicio-1-tema-2-lgebra
aliases:
  - Ejercicio 1 tema 2 álgebra
tags: []
---

# Calcular la proyección de u y v

$$
\vec{u} = (3,1,0) \text{ y } \vec{v} = (1,2,1)
$$

Para calcular la [[1709815513-proyeccin-de-un-vector-sobre-otro|proyección]] vamos a descomponer $\vec{v}$ en dos vectores, uno paralelo a $\vec{u}$ y otro perpendicular a $\vec{u}$.

$$
\begin{split}
    & \vec{v} = \vec{v_1} + \vec{v_2} \text{ donde } \vec{v_1} \| \vec{u} \text{ y } \vec{v_2} \perp \vec{u} \iff \\
    & (1,2,1) = \lambda(3,1,0) + v_2 \text{ donde } v_2 \cdot u = 0 \\
    & v_2 \cdot u = 0 \iff (v - v_1) \cdot u = 0 \iff ((1,2,1) - \lambda(3,1,0))\cdot(3,1,0) = 0 \iff \\
    & \iff (1-3\lambda, 2-\lambda, 1) \cdot (3,1,0) = 0 \iff 3(1-3\lambda) + 1(2-\lambda) = 0 \iff \\
    & \iff 3 - 9\lambda + 2 - \lambda = 0 \iff 5 - 10\lambda = 0 \iff \lambda = \frac{5}{10} = \frac{1}{2}
\end{split}
$$

Entonces, la proyección de $\vec{v}$ sobre $\vec{u}$ es:

$$
\text{proy}_{\vec{u}}(\vec{v}) = \vec{v_1} = \lambda \vec{u} = \frac{1}{2}(3,1,0) = \left(\frac{3}{2}, \frac{1}{2}, 0\right)
$$
