---
id: 1709828386-producto-vectorial
aliases:
  - Producto vectorial
tags:
  - álgebra
---

# Producto vectorial

El producto vectorial de dos vectores $\vec{u}$ y $\vec{v}$ se define como un vector perpendicular a ambos, cuyo módulo es igual al área del paralelogramo que forman $\vec{u}$ y $\vec{v}$. Sólo está definido en $\mathbb{R}^3$.

$$
\vec{u} \times \vec{v} = \begin{vmatrix}
\vec{i} & \vec{j} & \vec{k} \\
u_1 & u_2 & u_3 \\
v_1 & v_2 & v_3
\end{vmatrix}
$$

Donde $\vec{i}$, $\vec{j}$ y $\vec{k}$ son los [[1709815455-vector-unitario|vectores unitarios]] en la dirección de los ejes $x$, $y$ y $z$ respectivamente.

## Características

- El [[1709799713-mdulo-de-un-vector|módulo]] del producto vectorial es igual al área del paralelogramo que forman $\vec{u}$ y $\vec{v}$. Se puede calcular como:

$$
\| \vec{u} \times \vec{v} \| = \| \vec{u} \| \| \vec{v} \| \sin(\alpha)
$$

- La [[1709799858-direccin-de-un-vector|dirección]] del producto vectorial es perpendicular al plano que forman $\vec{u}$ y $\vec{v}$.

- El [[1709799958-sentido-de-un-vector|sentido]] del producto vectorial se puede calcular con la regla del sacacorchos o la regla de la mano derecha.

## Propiedades

- El producto vectorial de dos vectores es un vector perpendicular a ambos.
- El producto vectorial cumple la propiedad distributiva:

$$
\vec{u} \times (\vec{v} + \vec{w}) = \vec{u} \times \vec{v} + \vec{u} \times \vec{w}
$$

- El producto vectorial es anticonmutativo:

$$
\vec{u} \times \vec{v} = -(\vec{v} \times \vec{u})
$$

- El producto vectorial cumple la propiedad asociativa:

$$
\alpha (\vec{u} \times \vec{v}) = (\alpha \vec{u}) \times \vec{v} + \vec{u} \times (\alpha \vec{v})
$$
