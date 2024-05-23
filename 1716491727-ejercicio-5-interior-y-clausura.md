---
id: 1716491727-ejercicio-5-interior-y-clausura
aliases:
  - Ejercicio 5 Interior y Clausura
tags:
  - topología
---

## Es verdad que:

1. $\overline{A \cup B} = \overline{A} \cup \overline{B}$

$x \in Fr(A \cup B)$
$\text{Supongamos que } a \in U_A(x) \;\; b \notin U_A(x) \text{ y que } b \in U_B(x) \; a \notin U_B(x) \text{ entonces } U_A(x) \cap U_B(x) \text{ no tiene puntos de a ni puntos de b}$
Hemos encontrado un elemento de la [[1716491727-frontera|frontera]] que no tiene elementos de $A$ ni $B$ en su [[1716491727-conjunto-abierto|entorno]], y la definición de frontera es que al menos tiene elementos de $A$ o de $B$ $\implies$ Contradicción !!!

Por lo tanto, es verdad.

2. $\cup \overline{A_i} = \overline{\cup A_i}$

$A_i = \{ \frac{1}{i} \}$

Por lo tanto, es falso.