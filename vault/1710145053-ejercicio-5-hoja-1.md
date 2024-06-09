---
id: 1710145053-ejercicio-5-hoja-1
aliases:
  - Ejercicio 5 hoja 1
tags:
  - matemática-discreta-II
---

# ¿Cuántos grafos no isomorfos con tres vértices pueden construirse? ¿Y con cuatro vértices? ¿Y con cinco?

Sabemos que el número de aristas de un [[1706782930-grafo|grafo]] es ${\binom{n}{2}}$. Si consideramos solo [[1706783358-grafo-simple|grafo simples]] sin [[1706977267-lazo-grafo|lazos]], como cada arista tiene dos estados (estar o no estar), el número total de combinaciones será:

$$
\text{número de grafos de } n \text{ vértices} = 2^{\binom{n}{2}} 
$$

El problema es que no consideramos los grafos [[1709997137-grafos-isomorfos|isomorfos]]. Sabiendo que dos grafos son isomorfos si permutando las filas (o columnas) de la matriz de adyacencia de uno de ellos se obtiene la matriz de adyacencia del otro, entonces sabemos que el número de grafos isomorfos de $n$ vértices es $n!$.

Por lo tanto, nuestra nueva formula para el número de grafos no isomorfos de $n$ vértices es:

$$
\text{número de grafos no isomorfos de } n \text{ vértices} = \frac{2^{\binom{n}{2}}}{n!}
$$

Por lo tanto, el número total de grafos con 3 vértices es $2^{\binom{3}{2}}=2^3=8$, el número de grafos no isomorfos con 4 vértices es $2^{\binom{4}{2}}=2^6 =64$ y el número de grafos con 5 vértices es $2^{\binom{5}{2}}=2^{10} = 1024$ 

El problema es que no consideramos los grafos [[1709997137-grafos-isomorfos|isomorfos]]. Sabiendo que dos grafos son isomorfos si permutando las filas (o columnas) de la matriz de adyacencia de uno de ellos se obtiene la matriz de adyacencia del otro, entonces sabemos que el número de grafos isomorfos de $n$ vértices es $n!$.

[Solución](https://oeis.org/A000088)
