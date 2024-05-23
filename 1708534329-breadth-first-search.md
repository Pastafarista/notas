---
id: 1708534329-breadth-first-search
aliases:
  - Breadth First Search
  - Búsqueda en anchura
  - BFS
tags:
  - matemática-discreta-II
---

# Breadth First Search

El **Breadth First Search** (BFS) es un algoritmo de búsqueda en [[1706782930-grafo|grafos]] que recorre el grafo en anchura. Es decir, el algoritmo se desplaza a través de los vértices adyacentes antes de retroceder.

## Algoritmo

1. Numeramos los vértices si no están numerados
2. Creamos la lista vacía de aristas del [[1708533762-rbol-recubridor|árbol recubridor]], la lista vacía de vértices visitados
3. Elegimos un vértice $v_0$ al azar (normalmente el 0)
4. Añadimos **todos** los vértices adyacentes $v_i$ a la lista de vértices visitados y las aristas $v_0v_i$ a la lista de aristas del árbol recubridor
5. Para cada $v_i$ repetimos el paso 4. Si no quedan adyacentes no visitados y no hemos recorrido todos los vértices, el grafo no es [[1706786979-grafo-conexo|conexo]]

## Características

- Crea distintos [[1708533762-rbol-recubridor|árboles recubridores]] en función del vértice de partida y la numeración
- Nos permite calcular la [[1716491727-mtrica|distancia]] entre dos vértices, la excentricidad , el radio y el diámetro del grafo
- Es cómodo cuando se trata de buscar el camino más corto entre dos vértices
