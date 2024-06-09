---
id: 1716392171-teorema-de-euclides
aliases:
  - Teorema de Euclides
tags:
  - matemática-discreta-II
---

# Teorema de Euclides

## Enunciado

$$
mcd(a,b) = mcd(b, r) \quad\text{para } a = bk + r
$$

## Demostración

$\implies$

- Si $d | a$ y $d | b$ ($d$ es el máximo común divisor de $a$ y $b$) entonces si $a = bk + r$ podemos descomponer $a$ y $b$ en $da' = db'k + r$, por lo que $r = d(a' - b'k)$.
- Esto implica que $d | r$ ($d$ es múltiplo de $r$).
- Como $d$ también tiene el mismo máximo común divisor que $b$, podemos sustituir:

$$
mcd(a,b) = mcd(b,r)
$$

$\impliedby$

- Si $d|r$ y $d|b$, si $a = bk + r$ entonces $a = b'dk + r'd = d(b'k+r')$, por lo que $d|a$. Por lo tanto:

$$
mcd(b,r) = mcd(a,b)
$$
