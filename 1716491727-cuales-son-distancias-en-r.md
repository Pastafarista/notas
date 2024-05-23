---
id: 1716491727-cuales-son-distancias-en-r
aliases:
 - Cuales son distancias en R
---


## De las siguientes definiciones, ¿Cuáles son distancias?

- $d(x,y)=|x-2y|$
- $d(x,y) = |x-y|$
- $d(x,y)=(x-y)^2$

- Bonus:
$$
\mathrm d(x, y) = \begin{cases}
    0 & \text{if } x = y \\ % & is your "\tab"-like command (it's a tab alignment character)
    1 & \text{if } x \neq y
\end{cases}
$$
## Resolución:

### $d(x,y)=|x-2y|$

>$d(x,x) = |x - 2x| = |-x| \neq 0$

### $d(x,y)=|x-y|$

>$d(x,x) = |x-x| = 0$
>$d(y,x) = |y-x| = |-(x-y)| = |x-y| = d(x,y)$
>$d(x,y) \leq d(x,z) + d(z,y) \Longleftrightarrow |x-y| \leq |x-z| + |z-y|$

![[1716491727-desigualdad-triangular-dibujo.excalidraw]]

### $d(x,y) = (x-y)^2$

>$d(x,x)=(x-x)^2 = 0$
>$d(y,z) = (y-x)^2 = x^2 + y^2 -2xy = (x-y)^2 = d(x,y)$
>$d(x,y) \leq d(x,z) + d(z,y) \Longleftrightarrow (x-y)^2 \leq (x-z)^2 + (z-y)^2$
>$x = 1, y = -1, z = 0 \implies (1 - (-1))^2 \leq (1 - 0)^2 + (0 - (-1))^2 \Longleftrightarrow 4 \leq 2$

Luego como no cumple la desigualdad triangular, no es distancia.

### Bonus

>$d(x,x) = 0$
>$d(y,x) = 1 = d(x,y)$
>$d(x,y) \leq d(x,z) + d(z,y) \Longleftrightarrow 1 \leq 1 + 1 \Longleftrightarrow 1 \leq 2$
