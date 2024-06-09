---
id: 1708971315-rango-de-una-matriz
aliases:
  - Rango de una matriz
  - Rango
tags:
  - álgebra
---

# Rango de una matriz

El rango de una [[1708971486-matriz|matriz]] de orden $m \times n$ es el número de filas que tiene linealmente independientes; también es el número de columnas linealmente independientes.

$$
    A = \begin{pmatrix}
    a_{11} & a_{12} & \cdots & a_{1n} \\
    a_{21} & a_{22} & \cdots & a_{2n} \\
    \vdots & \vdots & \ddots & \vdots \\
    a_{m1} & a_{m2} & \cdots & a_{mn} \\
    \end{pmatrix} = (a_{ij}) \; i = 1, 2, \ldots, m; \; j = 1, 2, \ldots, n
$$

$$rang(A) \leq \min(m, n)$$

## Propiedades

1. $rang(A \cdot B) \leq min(rang(A), rang(B))$
2. ${rang(A^t) = rang(A)}$
3. Una [[1708972968-matriz-cuadrada|matriz cuadrada]] tiene [[1708971370-matriz-inversa|inversa]] si y sólo si $rang(a)=n$
4. Una matriz cuadrada tiene rango $n$ si y sólo si su [[1708976016-determinante|determinante]] no es cero.
5. El rango de una [[1708971486-matriz|matriz]] $A$ es el mismo que el de cualquier matriz obtenida mediante [[1708977689-operaciones-elementales|operaciones elementales]].
6. Dos [[1708977581-matrices-equivalentes|matrices equivalentes]] tienen el mismo rango.

## Teoremas

Si el rango de una [[1708972968-matriz-cuadrada|matriz cuadrada]] $A$ coincide con su orden, entonces $A$ se puede transformar en la [[1708973072-matriz-identidad|matriz identidad]] mediante operaciones elementales en sus filas.

El rango de una [[1708971486-matriz|matriz]] $A$ es el número de filas no nulas de cualquier [[1709020490-matriz-escalonada|matriz escalonada]] obtenida a partir de $A$ a partir de [[1708977689-operaciones-elementales|operaciones elementales]]


