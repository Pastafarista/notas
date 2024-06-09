---
id: 1716391680-propiedades-funcin-de-euler
aliases:
  - Propiedades función de Euler
tags:
  - matemática-discreta-II
---

# Propiedades función de Euler

## Enunciado

$$
\begin{split}
    & \phi(pq) = (p-1)(q-1) \quad \text{si } p, q \text{ primos} \\
    & \phi(p^{k}) = p^{k-1}(p-1) \quad \text{si } p \text{ primo}
\end{split}
$$

## Demostración

### $\phi(pq) = (p-1)(q-1)$

Sabemos que $\phi (pq)$ será $pq - 1$ (como un primo normal), pero hay que quitar los múltiplos de $p$ y $q$ menores a $pq$. En el caso de $p$ serán $q-1$ múltiplos y en el caso de $q$ serán $p-1$ múltiplos. Por lo tanto:

$$
\phi(pq) = pq - 1 - (q - 1) - (p-1) = pq - q - p + 1 = (p-1)(q-1)
$$

### $\phi(p^{k}) = p^{k-1}(p-1)$

Si $p$ es primo $\phi(p^k)$ será igual a $p^k - 1$ números menores que $p^k$ y quitando todos los múltiplos de $p^k$, que serán los $p^{k-1} - 1$ múltiplos de $p$, menores que $p^k$

$$
\phi(p^k) = p^k - 1 - (p^{k-1} - 1) = p^k - p^{k-1} = p^{k-1}p - p^{k-1} = p^{k-1}(p - 1)
$$