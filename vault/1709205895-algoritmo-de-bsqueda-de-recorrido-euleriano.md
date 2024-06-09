---
id: 1709205895-algoritmo-de-bsqueda-de-recorrido-euleriano
aliases:
  - Algoritmo de búsqueda de recorrido euleriano
tags:
  - matemática-discreta-II
---

# Algoritmo de búsqueda de recorrido euleriano

Este algoritmo busca un recorrido euleriano en un [[1706782930-grafo|grafo]].

## Descripción

1. Comprobamos que el [[1706785520-grado-de-un-vrtice|grado]] de todos los vértices es par menos dos (pongamos, $Y$ y $Z$)
2. Creamos el vértice adicional $X$ y las aristas $XY$ y $XZ$. ¡Ahora hay un [[1709204869-grafo-euleriano|circuito euleriano]]!
3. Partiendo del vértice $X$ realizamos el algoritmo anterior.
4. Borramos el circuito $XY$ y $XZ$. Ahora tenemos un recorrido euleriano.
