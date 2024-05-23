
**Definiciones:**

[[Conjunto abierto]]
- Un conjunto es abierto si solo tiene puntos de su [[Interior]]

[[Punto fronterizo]]
- Un punto es fronterizo si cada entorno abierto suyo tiene al menos un punto dentro y un punto fuera del conjunto

[[Clausura]]
- La clausura es la unión del conjunto con su frontera

[[Punto de acumulación]]
- Los puntos de acumulación o puntos límite $X'$, son puntos tales que su entorno tiene al menos otro punto de $X$ (Son los puntos de la clausura menos los puntos aislados)

[[Punto aislado]]
- Los elementos de $\bar{X} \setminus X'$ se llaman **puntos aislados**, los puntos aislados son los puntos del conjunto que en su entorno no tienen ningún otro punto de $X$

**Teoremas:**
- [[Cada conjunto cerrado coincide con su clausura]] 

-  [[La clausura de H es la intersección de todos los cerrados que contienen H]] 

- [[La clausura de un subespacio es el propio espacio si sólo si su intersección con cualquier abierto no es nula]] 

-  [[La unión de todos los abiertos que X contiene coincide con Int(X)]]

**Teoremas de frontera, clausura e interior**

[[La frontera de A es la intersección de su clausura con la clausura de su complementario]]

$\bar{A} = A \cup A'$

**¿Qué ocurre con la clausura si refinamos la topología?**

- Pensemos en [[Topología de Sorgenfrey]] vs la canónica, el intervalo $(2,3)$ en la canónica su clausura es $[2,3]$ pero en la [[Topología de Sorgenfrey]] es $[2,3)$
- Podemos observar que $[2,3] \subset [2,3)$, que en general significa que la clausura del más grueso es más grande que la de la más fina

**Ejemplo:**
 

- Consideremos el cuadrado $X = [0,1]  \; \times  \; [0,1]$ con el [[Orden Lexicográfico]]
- Dentro de él, veremos el borde inferior $A = \{  (x,0), \; x \in [0,1] \}$
- ¿Cuál es la clausura de $\overline{A}$?

>Consideremos $(0.5 : 1)$
>Entonces $(0.5 : 0.9) \leq (0.5 : 1) \leq (a : b)$

**Subconjuntos densos**

[[Conjunto denso]]

- Un subconjunto $H \subset X$ se llama denso si $\overline{H} = X$

>Ejemplo: $\mathbb{Q} \subset \mathbb{R}$

**Demostrar que las dos definiciones coinciden:**

1. $\implies$
Sabemos que $\bar{H} = X$. Supongamos lo contrario, que $\exists U \subset X \; tq \; U \cap H = \emptyset$, esto claramente es una contradicción.

2. $\impliedby$ 
Sabemos que $X \subset \bar{H}$, supongamos que encontramos un $x \in X$ tal que $x \notin \bar{H}$ 

**Teorema de Weierstrass**

- Los polinomios son densos en el conjunto de funciones continuas

[[Conjunto no denso en ninguna parte]]

- No es denso en ninguna parte si el interior de su clausura sea vacío
	Por ejemplo el punto ${1}$ es un conjunto no denso en ninguna parte

- El complemento de un no denso en ninguna parte es denso, pero el complementario del denso puede ser denso

**Espacios separables**

- Un espacio topológico se llama separable si tiene un subconjunto numerable denso

[[Demostración un perro no puede ser plano]]

**¿Puede una sucesión converger a varios puntos?** #TODO (mirar presentación)

Existen topologías en las que una sucesión puede converger a varios puntos:
#topología 
- Consideremos la topología de Sierpinski:  $T_{Sierpinski} = \{ \emptyset, \{0\} \{ 0,1\} \}$ 
- Una topología converge en un mundo sin distancia si para cualquier abierto que contiene nuestro punto, todos los miembros de la sucesión están ahí #TODO 
- Entonces la sucesión $1,1,1,1,1 ... ,1$ converge a $1$
- Pero la sucesión $0,0,0,0 ... ,0$ también converge a $1$
## Ejercicios

[[Ejercicio 1 Interior y Clausura]]
[[Ejercicio 2 Interior y Clausura]]
[[Ejercicio 3 Interior y Clausura]]
[[Ejercicio 4 Interior y Clausura]]
[[Ejercicio 5 Interior y Clausura]]
[[Ejercicio 6 Interior y Clausura]]
[[Ejercicio 7 Interior y Clausura]]


![[Teoría Topología - 5. Interior y clausura. Propiedad de Hausdorff 1.pptx]]