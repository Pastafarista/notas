---
id: 1710174452-ejercicio-4-primer-parcial-examen-final-lgebra
aliases:
  - Ejercicio 4 primer parcial examen final álgebra
tags:
  - álgebra
---

# Dados los vectores u y v se pide

$$
\begin{split}
    & u = (1, 0, 0)\\
    & v = (1, 1, 0)
\end{split}
$$

1. El [[1709802244-ngulo-de-dos-vectores|ángulo]] que forman $\vec{u}$ y $\vec{v}$

Recordemos que la fórmula alternativa del [[1709801827-producto-escalar-de-dos-vectores|producto escalar]] es:

$$
< \vec{u},\vec{v}> = \|\vec{u}\| \cdot \|\vec{v}\| \cdot \cos(\alpha)
$$

Despejando $\alpha$:

$$
\cos(\alpha) = \frac{< \vec{u},\vec{v}>}{\|\vec{u}\| \cdot \|\vec{v}\|}
$$

Sustituyendo:

$$
\begin{split}
    & \cos(\alpha) = \frac{1 \cdot 1 + 0 \cdot 1 + 0 \cdot 0}{\sqrt{1^2 + 0^2 + 0^2} \cdot \sqrt{1^2 + 1^2 + 0^2}} = \frac{1}{\sqrt{2}} \iff\\
    & \iff \alpha = \frac{\pi}{4} \approx 45\degree
\end{split}
$$

![[ej4-primer-parcial-álgebra.png]]

2. Hallar la [[1709799713-mdulo-de-un-vector|magnitud]] de la [[1709815513-proyeccin-de-un-vector-sobre-otro|proyección]] de $\vec{u}$ sobre $\vec{v}$

$$
\begin{split}
    & \text{proy}_{\vec{v}}(\vec{u}) = \vec{u_1}\\
    & \vec{u} = \vec{u_1} + \vec{u_2} \text{ donde } \vec{u_1} \| \vec{v} \text{ y } \vec{u_2} \perp \vec{v}\\
    & (1,0,0) = \lambda(1,1,0) + u_2 \iff u_{2} = (1,0,0) - \lambda(1,1,0) = (1-\lambda, -\lambda, 0)\\
    & <u_2,v> \, = 0 \iff (1-\lambda, -\lambda, 0) \cdot (1,1,0) = 0 \iff 1-\lambda - \lambda = 0\\
    & \iff 1-2\lambda = 0 \iff \lambda = \frac{1}{2}\\
    & \text{proy}_{\vec{v}}(\vec{u}) = \vec{u_1} = \lambda (1,1,0) = \frac{1}{2}(1,1,0) = \left(\frac{1}{2},\frac{1}{2},0\right)
\end{split}
$$Entonces la magnitud será:

$$
\left\|\left(\frac{1}{2},\frac{1}{2},0\right)\right\| = \sqrt{\frac{1}{4} + \frac{1}{4}} = \frac{1}{\sqrt{2}}
$$

Otra forma sería utilizando la fórmula:

$$
\text{proy}_{\vec{v}}(\vec{u}) = \frac{\vec{u} \cdot \vec{v}}{\|\vec{v}\|^2} \vec{v} = \frac{1 \cdot 1 + 0 \cdot 1 + 0 \cdot 0}{1^2 + 1^2 + 0^2} \cdot (1,1,0) = \frac{1}{2} \cdot (1,1,0) = \left(\frac{1}{2},\frac{1}{2},0\right)
$$

3. Hallar un vector $(x,y,z) \neq (0,0,0)$ que sea combinación lineal de $\vec{u}$ y $\vec{v}$ y que sea perpendicular a $(1,0,0)$

Para que el [[1709799641-vector-fijo|vector]] sea perpendicular a $(1,0,0)$, el producto escalar entre ambos debe ser $0$:

$$
(x,y,z) \cdot (1,0,0) = x \cdot 1 + y \cdot 0 + z \cdot 0 = x = 0
$$

Que el vector sea combinación lineal de $\vec{u}$ y $\vec{v}$ significa que existen $\lambda$ y $\mu$ tales que:

$$
\lambda \vec{u} + \mu \vec{v} = (x,y,z) \iff \lambda(1,0,0) + \mu(1,1,0) = (x,y,z)
$$

Expandiendo:

$$
\begin{cases}
	& \lambda + \mu = x = 0\\
	& \mu = y\\
	& 0 = z
\end{cases}
$$

Resolviendo el sistema:

$$
\begin{cases}
    & x = 0\\
    & \mu = y\\
    & z = 0
\end{cases}
$$

Por lo tanto nuestro vector tendrá la forma $(0,y,0), \; y \in  \mathbb{R} \setminus \{0\}$, por ejemplo $(0,1,0)$.
