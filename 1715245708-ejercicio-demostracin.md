---
id: 1715245708-ejercicio-demostracin
aliases:
  - Ejercicio demostraciones
tags:
  - matemática-discreta-II
---

# Demostrar que $4^{n} - 1$ es múltiplo de 3

1. Por inducción:

$$
\begin{split}
    & n = 1 \Rightarrow 4^{1} - 1 = 3 \quad \text{es múltiplo de 3} \\
    & n = k \Rightarrow 4^{k} - 1 = 3m \quad \text{para algún } m \in \mathbb{Z} \\
	& n = k + 1 \Rightarrow 4^{k+1} - 1 = 4 \cdot 4^{k} - 1 = 4 \cdot (3m + 1) - 1 = 12m + 4 - 1 =\\
	&  12m + 3 = 3(4m + 1) \quad \text{es múltiplo de 3}
\end{split}
$$

# Demostrar que $4^n - 3n - 1$ es múltiplo de 9

- Para $n=0$ $4^n - 3n - 1 = 0$, que es múltiplo de $9$
- Para $n=k$ supongamos que se cumple: $4^k - 3k - 1 = 9m$
- Para $n=k+1$ 

$$
\begin{split}
	& 4^{k+1} = 3\cdot 4^k + 4^k = 3\cdot 4^k + (4^k - 3k - 1) -3 =\\
	& = 3\cdot 4^k + 9m -3 = 9m + 3(4^k - 1) = 9m + 9l \quad \text{ que es múltiplo de 9}
\end{split}
$$

# Demostrar que $p^2 - 1$ es múltiplo de 24, donde $p$ es un número primo mayor que 3

- $p^2 - 1 = (p-1)(p+1)$

- $(p-1)$ será $4k$ o $4k + 2$ ya que son números primos mayores que 3, si $(p-1) = 4k+2$ entonces $(p+1)=4k+4$ por lo que siempre habrá uno múltiplo de 4 y otro múltiplo de 2, por lo que $(p-1)(p+1)$ será múltiplo de 8
- Alguno de los números $(p-1)$, $p$ o $p+1$ debe ser múltiplo de 3 porque son 3 números consecutivos, y sabemos que $p$ no lo es porque es primo y mayor que 3, por lo que $(p-1)(p+1)$ será múltiplo de 3

# Demostrar que $a^3 + b^3 + c^3$ es divisible entre $a+b+c$
$$
\begin{split}
    & a + b + c | (a+b+c)^3 = a^3 + b^3 +c^3 - 3abc + \ldots \\
    & (a+b+c)^3 = 3(a^2b + ab^2 + abc + a^2c + ac^2 + abc + b^2c + bc^2 + abx) =\\
    & = 3(ab(a+b+c) + ac(a+b+c) + bc(a+b+c) + 3abc) \quad \text{múltiplo de } a+b+c
\end{split}
$$

# Demostrar que el producto de $k$ números consecutivos es divisible por $k!$

$$
\begin{split}
    & \binom{n}{k} = \frac{n!}{k!(n-k)!} = \frac{n(n-1)\dots (n-k+1) \dots (n-k)(n-k-1) \dots}{k!(n-k)!} =\\
    & = \frac{n(n-1)(n-2)\ldots(n-k+1)}{k!} \text{ es un número entero} \\
\end{split}
$$

# Demostrar que $(p-1)! \equiv -1 \text{ mod } p$ si $p$ es primo

Supongamos que $p$ no es primo, entonces $p$ es compuesto y $p = ab$ con $a,b \neq 1$ y $a,b < p$, entonces $a,b$ son factores de $(p-1)!$ y $(p-1)! \equiv 0 \text{ mod } p$
