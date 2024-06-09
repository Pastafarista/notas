---
id: 1710190313-bsqueda-de-puentes-con-dfs
aliases:
  - Búsqueda de puentes con DFS
tags:
  - matemática-discreta-II
---

# Búsqueda de puentes con [[1708533902-depth-first-search|DFS]]

La arista $XY$ es un [[1708534542-puente|puente]] si sólo si $Y$ ni ninguno de sus descendientes en el [[1708533762-rbol-recubridor|árbol recubridor]] tiene un **back-edge** a $X$ ni ninguno de sus ancestros (padres).

Un **back-edge** es una arista $(u,v)$ tal que $v$ es un ancestro de $u$ pero no está en el árbol recubridor.
