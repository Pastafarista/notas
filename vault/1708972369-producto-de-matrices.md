---
id: 1708972369-producto-de-matrices
aliases:
  - Producto de matrices
tags: []
---

## Producto de [[1708971486-matriz|matrices]]

Sean $A$ una matriz de orden $m \times n$ y $B$ una matriz de orden $n \times p$. El producto de $A$ por $B$ es una matriz de orden $m \times p$ cuyos elementos son el producto de los elementos de la fila $i$ de $A$ por los elementos de la columna $j$ de

$$
\sum_{k=1}^{n} a_{ik}b_{kj} = a_{i1}b_{1j} + a_{i2}b_{2j} + \cdots + a_{in}b_{nj}
$$

## Propiedades del producto de matrices

1. ${\forall A,B,C \in M_{m \times n}, \; A(B + C) = AB + AC}$
2. ${\forall A,B \in M_{m \times n}, \; \text{ y } \forall k \in \mathbb{R}, \; k(AB) = (kA)B = A(kB)}$
3. ${\forall A \in M_{m \times n},}$ existen matrices $I_m$ e $I_N$, denominadas matrices de identidad, cuadradas de tamaño $m \times m$ y $n \times n$ respectivamente, cuyas diagonales son todo unos y el resto de los elementos cero, que cumplen que ${I_mA = A = AI_n}$.
4. El producto de matrices no es conmutativo, es decir, ${AB \neq BA}$ en general.
