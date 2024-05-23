---
id: 1715963663-los-restos-estn-correctamente-definidos
aliases:
  - Los restos están correctamente definidos
tags:
  - matemática-discreta-II
---

# Los restos están correctamente definidos

## Enunciado

Si hay dos divisiones distintas de un número $n$ entre $m$, estas tienen que coincidir. Es decir, para una división solo hay un cociente y un resto.

## Demostración

Consideremos los dos cocientes y restos distintos de la división de $n$ entre $m$:

$$
\begin{split}
    & n = k_{1} \cdot m + r_{1} \\
    & n = k_{2} \cdot m + r_{2}\\
    & 0 \le r_1,r_2 < m
\end{split}
$$

Si las restamos:

$$
(k_{1} - k_{2}) \cdot m = r_{2} - r_{1} \implies m | r_{2} - r_{1}
$$

Vemos que $r_{1}-r_{2}$ es múltiplo de $m$, pero $-m < r_{1}-r_{2}<m$, por lo que $r_{1}-r_{2}=0$ y $r_{1}=r_{2}$. Por tanto, los restos están correctamente definidos.
- Entonces, si los restos son iguales, los cocientes también lo son.
