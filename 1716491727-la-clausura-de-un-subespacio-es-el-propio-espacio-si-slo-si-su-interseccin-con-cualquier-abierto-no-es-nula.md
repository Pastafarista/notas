---
id: 1716491727-la-clausura-de-un-subespacio-es-el-propio-espacio-si-slo-si-su-interseccin-con-cualquier-abierto-no-es-nula
aliases:
 - La clausura de un subespacio es el propio espacio si sólo si su intersección con cualquier abierto no es nula
---

#topología

$X$ es la [[1716491727-clausura|Clausura]] de $H$ $\Longleftrightarrow$ La intersección de H con cualquier [[1716491727-conjunto-abierto|abierto]] de $X$ no es nula  
$$\overline{H}=X \Longleftrightarrow H \cap A \neq \emptyset, \; A \text{ es abierto}, \; x \in A$$

1. $\overline{H}=X \implies H \cap A \neq \emptyset$

Supongamos lo contrario, que $\exists A \subset X : H \cap A = \emptyset$

- Si $x \in A$ entonces como $x \notin H$ y  $x \in X = \overline{H}$, entonces $x \in Fr(H)$
- Como está en la frontera tendrá sus entornos tendrán puntos fuera del abierto $A$ ¡¡¡Contradicción!!!

2. $\overline{H}=X \impliedby H \cap A \neq \emptyset$

Demostraremos que $X \setminus (H \cup Fr(H)) = \emptyset$, es decir que X no tiene puntos fuera de $H$ ni de la [[1716491727-frontera|Frontera]] de $H$

- Tenemos que $\forall x \in X \; \forall A(x) \in T \;\ A(x)\cap H \neq \emptyset$
- Esto significa que todos los puntos tienen en sus entornos puntos de $H$, solo hay dos opciones:
	- $x \in Fr(H)$
	- $x \in Int(H)$
- Por lo que efectivamente $\forall x \in X : x \in \overline{H} \implies X = \overline{H}$ 