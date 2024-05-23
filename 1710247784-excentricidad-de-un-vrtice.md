---
id: 1710247784-excentricidad-de-un-vrtice
aliases:
  - Excentricidad de un vértice
  - Excentricidad
tags:
  - matemática-discreta-II
---

# Excentricidad de un vértice

La **excentricidad** de un vértice $v$ es la máxima [[1710247403-distancia-entre-dos-vrtices|distancia]] entre $v$ y cualquier otro vértice del [[1706782930-grafo|grafo]].

Para calcular la excentricidad de un vértice, realizamos [[1708534329-breadth-first-search|BFS]] desde él y calculamos el nivel del vértice más alejado en el [[1708533762-rbol-recubridor|árbol resultante]].
