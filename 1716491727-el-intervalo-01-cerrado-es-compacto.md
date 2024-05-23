---
id: 1716491727-el-intervalo-01-cerrado-es-compacto
aliases:
 - El intervalo 0,1 cerrado es compacto
---

#topología

- Supongamos que $\mathcal{U}$ es un [[1716491727-recubrimiento|Recubrimiento]] de $[0,1]$
- Consideremos el conjunto de números reales $\mathcal{C}$, si demostramos que $1$ está en $\mathcal{C}$ conseguiremos demostrar que $[0,1]$ es [[1716491727-espacio-compacto|compacto]]
$${\mathcal{C} = \{x \in [0,1] \; |\; [0,x] \text{ recubierto por finitos elementos de } \mathcal{U} \;  \}  }$$

1. $\mathcal{C} \neq \emptyset$
- El conjunto $\mathcal{C}$ al menos contendrá al $0$ ya que $0 \subset u_i$, $u_i \subset \mathcal{U}$ y por lo tanto $[0,0]$ está recubierto por finitos elementos de $\mathcal{U}$ 

2. $\mathcal{C}$ está acotado superiormente por el $1$ $(\mathcal{C} = \{ x \in [0,1] ... \})$
3. Como está acotado, entonces tiene un supremo $c = sup\{ \mathcal{C} \}$
4. Supongamos que $c < 1$, como $c$ está en el intervalo $[0,1]$ existe un $u_i \in \mathcal{U}$ que contiene a $c$
5. Este [[1716491727-conjunto-abierto|abierto]] tendrá una [[1716491727-bola-abierta|Bola Abierta]] con $r>0$
$$B(c)_r = (c-r, c+r)\subset \mathcal{U}$$
6. Como $c-r < c = sup\{ \mathcal{C} \}$, entonces hay $x \in \mathcal{C}$ tal que $x > c-r$

![[El intervalo 0,1 cerrado es compacto 2024-01-21 19.35.48.excalidraw]]

7. Entonces si consideramos el intervalo $[0,c+ \frac{r}{2}]$ vemos que está cubierto por los finitos abiertos de $[0,x]$ y por el abierto $(c-r, c+r)$. Como solo le añadimos un nuevo abierto, sigue siendo finito
8. Por definición $c+\frac{r}{2}$ está en $\mathcal{C}$, pero $\Rightarrow\!\Leftarrow$ c=$sup\{ \mathcal{C} \}$ 

**Conclusión: $1 = sup\{ \mathcal{C} \}$**

Aunque ya hemos demostrado que el supremo es $1$, puede ocurrir que el supremo no esté dentro de $\mathcal{C}$, hay que demostrarlo

1. Sabemos que $\exists u_i \in \mathcal{U} : 1 \in u_i$
2. Como $u_i$ es [[1716491727-conjunto-abierto|abierto]] sabemos que $x \in (1-r,1+r) \in \mathcal{U}$
3. Como ${1-r < 1 = sup\{ \mathcal{C} \} }$, sabemos que $\exists x \in \mathcal{C} : x > b-r$
4. $[0,x] \cup (b-r, 1] = [0,1]$ y sabemos que está cubierto por los finitos abiertos de $[0,x]$ y por el abierto $(b-r, b+r)$, por lo tanto $[0,1]$ tiene un [[1716491727-recubrimiento|Recubrimiento]] finito y por lo tanto $[0,1]$ es [[1716491727-espacio-compacto|compacto]]

![[El intervalo 0,1 cerrado es compacto 2024-01-21 19.51.03.excalidraw]]