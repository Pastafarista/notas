---
id: 1709201234-algoritmo-de-ford-fulkerson
aliases:
  - Algoritmo de Ford-Fulkerson
tags:
  - matemática-discreta-II
---

# Algoritmo de Ford-Fulkerson

El algoritmo de Ford-Fulkerson es un algoritmo para encontrar el [[1709201970-flujo|flujo]] máximo en una red de flujo.

## Descripción

1. Creamos una **copia de [[1706782930-grafo|grafo]]** y fijamos todos los flujos a 0.
2. Buscamos un [[1706786847-camino|camino]]  entre el origen y el destino en el grafo original. Restamos este valor a las demás aristas. A esta arista le damos la vuelta, a las demás dibujamos el flujo inverso (si potencialmente pueden ir en otra dirección).
3. Copia del grafo: actualizamos los valores del flujo.
4. Repetimos el procedimiento hasta que no queden caminos entre el origen y el destino.
