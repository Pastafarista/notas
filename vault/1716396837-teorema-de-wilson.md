---
id: 1716396837-teorema-de-wilson
aliases:
  - Teorema de Wilson
tags:
  - matemática-discreta-II
---

# Teorema de Wilson

## Enunciado

Si $(n-1)! \equiv -1 \pmod{n}$ entonces $n$ es primo.

## Demostración

Supongamos que $n$ no es primo, entonces $n = p\cdot k$ con $2 \le p \le n-2$  y $p$ primo.

Si $(n-1)! \equiv 1 \pmod{pk}$ entonces $(n-1)! \equiv -1 \pmod{p}$:
- $(n-1)! - 1 \equiv 0 \pmod{pk} \implies$ $pk$ es múltiplo de $(n-1)! - 1$, por lo tanto $p$ también es múltiplo de $(n-1)! - 1$.

Pero como $p < n$, tenemos la siguiente contradicción: $$(n-1)! = n(n-1)\dots p \dots (n - k)! \equiv 0 \pmod{p}$$