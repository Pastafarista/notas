---
id: 1709205707-algoritmo-de-bsqueda-de-circuito-euleriano
aliases:
  - Algoritmo de búsqueda de circuito euleriano
tags:
  - matemática-discreta-II
---

# Algoritmo de búsqueda de circuito euleriano

Este algoritmo busca un [[1709204869-grafo-euleriano|circuito euleriano]] en un grafo. 

## Descripción

1. Comprobamos que el [[1706785520-grado-de-un-vrtice|grado]] de todos los vértices es par.
2. Partiendo de cualquier vértice realizamos un recorrido hasta que volvamos al punto inicial.
3. Si hay aristas por recorrer, buscamos el primer vértice de nuestro recorrido que tenga una arista por recorrer.
4. Realizamos el recorrido hasta que volvamos al vértice de partida
5. Insertamos el segundo recorrido en el primero
6. Volvemos al paso 3
