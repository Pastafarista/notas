---
id: 1716491727-cada-conjunto-cerrado-coincide-con-su-clausura
aliases:
 - Cada conjunto cerrado coincide con su clausura
---

#topología

Consideremos $C \subset X$, entonces $X \setminus C = C^{comp}$ es abierto
Supongamos que $\exists x  \in \bar{C}$ pero $x \notin C \implies X \in C^{comp}$
Esto implica que $\exists B(x) \subset C^{comp} \implies \text{X no está en la frontera}$


1. Supongamos un punto $x$ de la [[1716491727-clausura|Clausura]] $\overline{C}$ que no pertenezca al [[1716491727-conjunto-cerrado|Conjunto cerrado]] $C$
$$\exists x \in \overline{C}  \;\; x \notin C \;\; x \in Fr(C)$$
2. Entonces si $x$ no pertenece a $C$ pertenecerá a su complementario que es un [[1716491727-conjunto-abierto|Conjunto abierto]]
$$x \notin C \;\; x \in C^{comp}=X \setminus C \;\;\; C \text{ cerrado} \implies X \setminus C \text{ abierto}$$
3. Como $x$ pertenece a un abierto, tendrá un entorno completamente dentro de $X \setminus C$
$$x \in X \setminus C \;\; \exists U_n \subset X \setminus C$$
4. Contradicción: como $x \in Fr(X)$, $U(x)$ tendrá todos sus entornos con puntos de $C$ que no están completamente dentro de $X \setminus C$