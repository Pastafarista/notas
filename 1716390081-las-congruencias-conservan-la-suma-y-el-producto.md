---
id: 1716390081-las-congruencias-conservan-la-suma-y-el-producto
aliases:
  - Las congruencias conservan la suma y el producto
tags:
  - matemática-discreta-II
---

# Las congruencias conservan la suma y el producto

## Enunciado

Dadas la congruencia $a_{1} \equiv a_{2} \pmod{m}$ se tiene que:

1. $a_{1} + c \equiv a_{2} + c \pmod{m}$
2. $a_{1} \cdot c \equiv a_{2} \cdot c \pmod{m}$

## Demostración

Para la suma:

$$
\begin{split}
    & a_{1} \equiv a_{2} \pmod{b} \iff a_{1} = a_{2} + bk\\
    & a_{1} + c = a_{2} + c + bk \iff \\
    & a_{1} + c \equiv a_{2} + c + 0 \pmod{b}
\end{split}
$$

Para la multiplicación:

$$
\begin{split}
    & a_{1} \equiv a_{2} \pmod(b) \iff a_{1} = a_{2} + bk\\
    & a_{1} \cdot c = (a_{2} + bk) \cdot c = a_{2} \cdot c + bck \iff \\
    & a_{1} \cdot c \equiv a_{2} \cdot c + 0 \pmod{b}
\end{split}
$$
