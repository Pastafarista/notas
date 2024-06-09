---
id: 1716491727-la-unin-de-conexos-que-tiene-interseccin-entre-si-es-conexa
aliases:
 - La unión de conexos que tiene intersección entre si es conexa
---

#topología

- Supongamos que $X=\cup A_i, \; A_i \text{ son conexos y } \exists x \in A_i \text{(es decir, tienen intersección)}$
- Si la unión no fuera [[1716491727-espacios-conexos|conexa]], $X=P \cup Q$, unión de dos abiertos que no tienen intersección. Supongamos que $x \in P$

![[La unión de conexos que tiene intersección entre si es conexa 2023-11-16 09.58.04.excalidraw]]

- $A_1 \cap (P \cup Q) = (A_1 \cap P)\cup(A_1 \cup Q)$
- $x \in (A_1 \cap P) \implies (A_1 \cap Q) = \emptyset$

- Entonces tenemos dos [[1716491727-conjunto-abierto|abiertos]], ($A_1 \cap P$) y ($A_1 \cup Q$) disjuntos ($A_1 \cap Q) = \emptyset$ tal que $A_1 = (A_1 \cap P) \cup (A_1 \cup Q)$ $\Rightarrow\!\Leftarrow$ $A_1$ [[1716491727-espacio-compacto|compacto]]