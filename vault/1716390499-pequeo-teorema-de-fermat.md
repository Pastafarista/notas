---
id: 1716390499-pequeo-teorema-de-fermat
aliases:
  - Pequeño teorema de Fermat
tags:
  - matemática-discreta-II
---

# Pequeño teorema de Fermat

## Enunciado

Sea $a \in \mathbb{Z}$ y $p$ un número primo que no lo divide ($p \nmid a$), entonces se cumple que:

$$
a^{p-1} \equiv 1 \pmod{p}
$$

## Demostración

Es fácil ver que $a, 2a, 3a, \ldots, (p-1)a$ dan restos distintos:
- Dados $k,m \in \mathbb{N}: k,m < p$, si $ka \equiv ma \pmod{p}$, entonces $a(k-m)\equiv 0 \pmod{p}$, es decir o $a$ es divisor de $p$ (imposible) o $k-m$ es múltiplo de $p$ (imposible), por lo que $k-m=0$, es decir $k=m$.

- Por lo tanto, el producto de estos restos es el producto de todos los restos posibles:

$$
a\cdot 2a\cdot 3a \dots (p-1)a \equiv 1\cdot 2\cdot 3 \dots (p-1) \pmod{p}
$$

Dividiendo entre $(p-1)!$:
$$
a^{p-1} \equiv 1 \pmod{p}
$$


