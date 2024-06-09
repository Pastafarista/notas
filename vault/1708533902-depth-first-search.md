---
id: 1708533902-depth-first-search
aliases:
  - Depth First Search
  - Búsqueda en profundidad
  - DFS
tags:
  - matemática-discreta-II
---

# Depth First Search

El **Depth First Search** (DFS) es un algoritmo de búsqueda en grafos que recorre el grafo en profundidad. Es decir, el algoritmo se adentra en el grafo tanto como sea posible antes de retroceder.

## Algoritmo

1. Numeramos los vértices si no están numerados
2. Creamos la lista vacía de aristas del [[1708533762-rbol-recubridor|árbol recubridor]], la lista vacía de vértices visitados
3. Elegimos un vértice $v_0$ al azar (normalmente el 0)
4. Entre sus adyacentes elegimos el de menor número $v_i$ no visitado y nos desplazamos allí (añadimos el vértice $v_i$ a la lista de vértices visitados y la artista $v_0v_i$ a la lista de artistas del árbol recubridor). Si no hay adyacentes no visitados, volvemos al vértice anterior. Si hemos vuelto al $v_0$, no tiene adyacentes no visitados y no hemos recorrido todos los vértices, el grafo no es [[1706786979-grafo-conexo|conexo]]
5. Si no hemos recorrido todos los vértices, volvemos al punto 4

## Características

- Crea distintos [[1708533762-rbol-recubridor|árboles recubridores]] en función del vértice de partida y la numeración
- Busca "la autopista más larga" posible
- Es cómodo cuando se trata de crear un camino con el mínimo de ramificaciones (por ejemplo, para construir vías de tren o tranvía)
