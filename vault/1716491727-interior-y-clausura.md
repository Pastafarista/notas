---
id: 1716491727-interior-y-clausura
aliases:
  - Interior y Clausura
tags:
  - topología
---


**Definiciones:**

[[1716491727-conjunto-abierto|Conjunto abierto]]
- Un conjunto es abierto si solo tiene puntos de su [[1716491727-interior|Interior]]

[[1716491727-punto-fronterizo|Punto fronterizo]]
- Un punto es fronterizo si cada entorno abierto suyo tiene al menos un punto dentro y un punto fuera del conjunto

[[1716491727-clausura|Clausura]]
- La clausura es la unión del conjunto con su frontera

[[1716491727-punto-de-acumulacin|Punto de acumulación]]
- Los puntos de acumulación o puntos límite $X'$, son puntos tales que su entorno tiene al menos otro punto de $X$ (Son los puntos de la clausura menos los puntos aislados)

[[1716491727-punto-aislado|Punto aislado]]
- Los elementos de $\bar{X} \setminus X'$ se llaman **puntos aislados**, los puntos aislados son los puntos del conjunto que en su entorno no tienen ningún otro punto de $X$

**Teoremas:**
- [[1716491727-cada-conjunto-cerrado-coincide-con-su-clausura|Cada conjunto cerrado coincide con su clausura]] 

-  [[1716491727-la-clausura-de-h-es-la-interseccin-de-todos-los-cerrados-que-contienen-h|La clausura de H es la intersección de todos los cerrados que contienen H]] 

- [[1716491727-la-clausura-de-un-subespacio-es-el-propio-espacio-si-slo-si-su-interseccin-con-cualquier-abierto-no-es-nula|La clausura de un subespacio es el propio espacio si sólo si su intersección con cualquier abierto no es nula]] 

-  [[1716491727-la-unin-de-todos-los-abiertos-que-x-contiene-coincide-con-intx|La unión de todos los abiertos que X contiene coincide con Int(X)]]

**Teoremas de frontera, clausura e interior**

[[1716491727-la-frontera-de-a-es-la-interseccin-de-su-clausura-con-la-clausura-de-su-complementario|La frontera de A es la intersección de su clausura con la clausura de su complementario]]

$\bar{A} = A \cup A'$

**¿Qué ocurre con la clausura si refinamos la topología?**

- Pensemos en [[1716491728-topologa-de-sorgenfrey|Topología de Sorgenfrey]] vs la canónica, el intervalo $(2,3)$ en la canónica su clausura es $[2,3]$ pero en la [[1716491728-topologa-de-sorgenfrey|Topología de Sorgenfrey]] es $[2,3)$
- Podemos observar que $[2,3] \subset [2,3)$, que en general significa que la clausura del más grueso es más grande que la de la más fina

**Ejemplo:**
 

- Consideremos el cuadrado $X = [0,1]  \; \times  \; [0,1]$ con el [[1716491727-orden-lexicogrfico|Orden Lexicográfico]]
- Dentro de él, veremos el borde inferior $A = \{  (x,0), \; x \in [0,1] \}$
- ¿Cuál es la clausura de $\overline{A}$?

>Consideremos $(0.5 : 1)$
>Entonces $(0.5 : 0.9) \leq (0.5 : 1) \leq (a : b)$

**Subconjuntos densos**

[[1716491727-conjunto-denso|Conjunto denso]]

- Un subconjunto $H \subset X$ se llama denso si $\overline{H} = X$

>Ejemplo: $\mathbb{Q} \subset \mathbb{R}$

**Demostrar que las dos definiciones coinciden:**

1. $\implies$
Sabemos que $\bar{H} = X$. Supongamos lo contrario, que $\exists U \subset X \; tq \; U \cap H = \emptyset$, esto claramente es una contradicción.

2. $\impliedby$ 
Sabemos que $X \subset \bar{H}$, supongamos que encontramos un $x \in X$ tal que $x \notin \bar{H}$ 

**Teorema de Weierstrass**

- Los polinomios son densos en el conjunto de funciones continuas

[[1716491727-conjunto-no-denso-en-ninguna-parte|Conjunto no denso en ninguna parte]]

- No es denso en ninguna parte si el interior de su clausura sea vacío
	Por ejemplo el punto ${1}$ es un conjunto no denso en ninguna parte

- El complemento de un no denso en ninguna parte es denso, pero el complementario del denso puede ser denso

**Espacios separables**

- Un espacio topológico se llama separable si tiene un subconjunto numerable denso

[[1716491727-demostracin-un-perro-no-puede-ser-plano|Demostración un perro no puede ser plano]]

**¿Puede una sucesión converger a varios puntos?** (mirar presentación)

Existen topologías en las que una sucesión puede converger a varios puntos:

- Consideremos la topología de Sierpinski:  $T_{Sierpinski} = \{ \emptyset, \{0\} \{ 0,1\} \}$ 
- Una topología converge en un mundo sin distancia si para cualquier abierto que contiene nuestro punto, todos los miembros de la sucesión están ahí
- Entonces la sucesión $1,1,1,1,1 ... ,1$ converge a $1$
- Pero la sucesión $0,0,0,0 ... ,0$ también converge a $1$
## Ejercicios

[[1716491727-ejercicio-1-interior-y-clausura|Ejercicio 1 Interior y Clausura]]
[[1716491727-ejercicio-2-interior-y-clausura|Ejercicio 2 Interior y Clausura]]
[[1716491727-ejercicio-3-interior-y-clausura|Ejercicio 3 Interior y Clausura]]
[[1716491727-ejercicio-4-interior-y-clausura|Ejercicio 4 Interior y Clausura]]
[[1716491727-ejercicio-5-interior-y-clausura|Ejercicio 5 Interior y Clausura]]
[[1716491727-ejercicio-6-interior-y-clausura|Ejercicio 6 Interior y Clausura]]
[[1716491727-ejercicio-7-interior-y-clausura|Ejercicio 7 Interior y Clausura]]


![[Teoría Topología - 5. Interior y clausura. Propiedad de Hausdorff 1.pptx]]