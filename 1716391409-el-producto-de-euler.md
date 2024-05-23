---
id: 1716391409-el-producto-de-euler
aliases:
  - El producto de Euler
tags:
  - matemática-discreta-II
---

# El producto de Euler

## Enunciado

$$
\phi(n) = n \cdot \prod_{p_i | n}\left( 1 - \frac{1}{p_i}\right) 
$$

## Demostración

- Sabemos que $\phi(p^{k})=p^{k-1}(p-1)$, donde $p$ primo.
- Por lo tanto, $\phi(p^{k}) = p^{k}\left( 1 - \frac{1}{p} \right)$
- También sabemos que $\phi(p) = p-1$


