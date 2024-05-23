---
id: 1716396317-lema-de-euclides
aliases:
  - Lema de Euclides
tags:
  - matemática-discreta-II
---

# Lema de Euclides

## Enunciado

Si $p | ab$ entonces $p | a$ o $p | b$. Es decir, si un número primo es múltiplo de un número $a\cdot b$ entonces es múltiplo de $a$ o de $b$.

## Demostración

- Supongamos que $p$ no es ni múltiplo de $a$ ni de $b$. Entonces, $mcd(a,p) = 1$ y $mcd(b,p) = 1$.

- Por la [[1716393883-identidad-de-bezout|identidad de Bezout]], existen $x,y$ tal que $ax + py = 1$.

- Si multiplicamos por $b$ ambos lados de la ecuación, obtenemos:

$$
abx + pby = b
$$

- Como $p | ab$, entonces $ab = pk$ para algún $k \in \mathbb{Z}$.

Por lo tanto, $pkx + pby = b$, y factorization $p$:

$$
p(kx + by) = b
$$

Esto implica que $p | b$, lo cual es una contradicción. Por lo tanto, si $p | ab$ entonces $p | a$ o $p | b$. $\blacksquare$
