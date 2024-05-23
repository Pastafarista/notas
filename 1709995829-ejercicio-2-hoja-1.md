---
id: 1709995829-ejercicio-2-hoja-1
aliases:
  - Ejercicio 2 hoja 1
tags:
  - matemática-discreta-II
---

# Describe (es decir, nombra, dibuja...) o explica por qué no puede existir:

1. Un [[1706782930-grafo|grafo]] con 7 vértices, todos de [[1706785520-grado-de-un-vrtice|grado]] 3.

No puede existir, ya que el número de vértices de grado impar debe ser par.

2. Un grafo con 15 vértices y 105 aristas.

El número máximo de aristas que puede tener un grafo con 15 vértices es $\binom{15}{2} = 105$, que es el número de aristas que estamos buscando. Por lo tanto, el grafo es $K_{15}$.

3. Dos grafos no [[1709997137-grafos-isomorfos|isomorfos]], cada uno con 6 vértices, todos de grado 2.

![[1709995829-ejercicio-2-hoja-1 2024-03-09 16.06.05.excalidraw]]

5. Un [[1706786979-grafo-conexo|grafo conexo]] con 8 vértices y cuya sucesión de grados sea $(1,1,1,2,3,4,5,7)$

No existe, teniendo en cuenta que tenemos un vértice de grado 7 y 3 de grado 3, el resto es como si fuese un grafo de 4 vértices (el resto de vértices ya no se les puede añadir aristas). Este grafo de 4 vértices puede tener como mucho vértices de grado 3 y sin embargo se nos pide que uno de sus vértices sea de grado 4 (5 menos la arista del vértice de grado 7).

6. Un grafo con 20 vértices y sucesión de grados:

$$(1,1,1,2,2,2,2,2,2,2,2,2,3,3,3,3,3,4,4,5)$$

No puede ser ya que el número de vértices de grado impar es $3+5+1=9$ que es impar, por lo tanto no existe.

6. Un grafo conexo con 25 vértices y sucesión de grados:

$$(1,1,1,1,1,1,1,1,1,1,1,1,2,2,2,2,2,2,2,2,2,3,3,4,4)$$

No puede existir, ya que al ser conexo van a tener que estar todos conectados, pero como hay 12 de grado 1, estos no pueden estar conectados entre ellos. Al conectar los 12 que si que se pueden conectar, como 9 de ellos son de grado 2, ya no se pueden conectar más vértices. Solo se podrían conectar 6 vértices de los dos vértices de grado 4 y 4 de los vértices de grado 3. Como aun nos quedarían 2 vértices de grado 1 sin conectar, no puede existir.
