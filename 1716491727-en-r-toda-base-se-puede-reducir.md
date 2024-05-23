---
id: 1716491727-en-r-toda-base-se-puede-reducir
aliases:
 - En R toda base se puede reducir
---

#topología

Elijamos un $U \subset B$

Elijamos un par de puntos $x,y \in U, \;\; y > x$ 

Podemos cubrir $U$ con intervalos [[1716491727-conjunto-abierto|abiertos]] de longitud $y - x$ (necesitaremos al menos 2 con $x,y$ como los puntos del extremo)

$U \subset (x - (y - x), x + (y - x)) \cup (y - (y - x), y  + (y - x))$

![[En R toda base se puede reducir 2023-11-01 18.12.53.excalidraw]]

Estos intervalos como son abiertos serán elementos de la [[1716491727-base-topolgica|base]] distintos de $U$

Ejemplo:

- $B = \{(a,b) : a < b, \}$
- $(1,8) \subset B$
- $2, \; 5 \in (1,8)$
- Intervalos de longitud 3
- $(2-3, 2 + 3) = (-1,5)$ y $(5 - 3, 5 + 3) = (2, 8)$
- $(-1,5) \cup (2,8) = (-1,8) \;\; (1,8) \subset (-1,8)$