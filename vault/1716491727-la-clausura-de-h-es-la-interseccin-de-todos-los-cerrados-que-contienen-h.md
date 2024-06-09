---
id: 1716491727-la-clausura-de-h-es-la-interseccin-de-todos-los-cerrados-que-contienen-h
aliases:
 - La clausura de H es la intersección de todos los cerrados que contienen H
---

#topología 


$\mathcal{C} = \{ C_i \in X : A \subset C_i, C_i \text{ es cerrado en } X\}$
$\overline{H} = \cap C_i \;\;  H \subseteq C_i$

![[La clausura es la intersección de todos los cerrados que contienen A 2023-10-30 20.14.41.excalidraw]]

$x \in \overline{H} \implies x \in \cap C_i$

1. $H \subset \cap C_i$
2. Supongamos que $x \in \overline{H}$ y $x\notin \cap C_i \implies$ $\exists C_i \supseteq H: x \notin C_i$
![[La clausura es la intersección de todos los cerrados que contienen A 2023-11-03 10.49.51.excalidraw]]
4. Si no pertenece  $C_i$ entonces, $x \in X \setminus C_i \implies \exists A(x) \in X \setminus C_i$
5. Esto implica que $A(x) \cap H = \emptyset$ ya que todos los entornos tienen que estar completamente dentro de $X \setminus H$ (no pueden tener puntos de $H$)
6. Pero $x \in \overline{H}$ por lo que los entornos de $x$ deben de tener puntos de $H$

$x \in \overline{H} \impliedby x \in \cap C_i$

Supongamos $\exists x : x \in \cap C_i \; x \notin \overline{H}$

- Entonces $x \in X \setminus \overline{H}$ que es abierto que no contiene a la [[1716491727-clausura|Clausura]] de $H$ y por lo tanto no contiene a $H$
- $x$ no pertenece a ninguno de los [[1716491727-conjunto-abierto|abiertos]] que no contienen a $H$ ($x \notin \cup X \setminus C_i$)
- Tenemos que $x \notin \cup X \setminus C_i$, pero $x \in X \setminus \overline{H}$ que ya es un abierto que no contiene a $H$ ¡¡¡Contradicción!!!