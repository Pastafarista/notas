---
id: 1709815513-proyeccin-de-un-vector-sobre-otro
aliases:
  - Proyección de un vector sobre otro
tags:
  - álgebra
---

# Proyección de un vector sobre otro

La proyección de un vector $v$ sobre otro vector $u$ se define como el producto del [[1709799713-mdulo-de-un-vector|módulo]] de $\vec{v}$ por el coseno del ángulo que forman $\vec{v}$ y $\vec{u}$.

$$
\text{proy}_{\vec{u}}(\vec{v}) = \mid v \mid \cos(\alpha )  
$$

La proyección es un vector paralelo a $\vec{u}$ que sumado a otro perpendicular a $\vec{u}$, forma el vector $\vec{v}$.

$$
\begin{split}
    & \text{proy}_{\vec{u}}(\vec{v}) = \vec{v_1}\\
    & \vec{v} = \vec{v_1} + \vec{v_2} \text{ donde } \vec{v_1} \| \vec{u} \text{ y } \vec{v_2} \perp \vec{u}\\
    & \text{Entonces } \vec{v_1} = \lambda \vec{u} \text{ y } \vec{v_2} \cdot \vec{u} = 0\\
    & \text{Como } \vec{v_2} = \vec{v} - \vec{v_1} \implies \vec{v_2} \cdot \vec{u} = (\vec{v} - \vec{v_1}) \cdot  \vec{u} = (\vec{v} - \lambda \vec{u}) \cdot \vec{u} = 0 \iff \\
    & \iff \vec{v} \cdot \vec{u} - \lambda \vec{u} \cdot \vec{u} = 0 \iff \\
    & \iff \lambda = \frac{\vec{v} \cdot \vec{u}}{\vec{u} \cdot \vec{u}} = \frac{\vec{v} \cdot \vec{u}}{\|u\|^2}
\end{split}
$$

Entonces la proyección de $\vec{v}$ sobre $\vec{u}$ es:

$$
\text{proy}_{\vec{u}}(\vec{v}) = \frac{\vec{v} \cdot \vec{u}}{\|u\|^2} \vec{u}
$$
