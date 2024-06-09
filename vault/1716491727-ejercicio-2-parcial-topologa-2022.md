---
id: 1716491727-ejercicio-2-parcial-topologa-2022
aliases:
 - Ejercicio 2 Parcial topología 2022
---

#topología 

## ¿Son [[1716491728-topologa|topologías]]? ¿Son [[1716491727-base-topolgica|bases]]? Si son topologías, ¿Son [[1716491727-espacio-hausdorff|Hausdorff]]?

1. $T = \{ \emptyset, \mathbb{R}^+, \left( \frac{1}{a},a\right):a>1 \}$
¿Es topología?

1. Si que contiene a $\emptyset$ y a $X = \mathbb{R}^+$
2. $\exists \cup \left( \frac{1}{a},a\right) = (0,\infty) \subset \mathbb{R}^+$
3. $\exists \cap \left( \frac{1}{a},a\right) \text{ (finita)} = \left( \frac{1}{a_n},a_0\right) \in T$
De hecho como es [[1716491728-topologa-de-tipo-matryoshka|de tipo Matryoshka]], es topología 

¿Es base?

Como cada topología es su propia base, también es base

¿Es Hausdorff?

Supongamos que si es Hausdorff, entonces para todo par de puntos $x,y$ tenemos $x \in \left( \frac{1}{a_1},a_1\right), \; y \in \left( \frac{1}{a_2},a_2\right) : \left( \frac{1}{a_1},a_1\right) \cap \left( \frac{1}{a_2},a_2\right) = \emptyset$

si $a_1 > a_2$ entonces $\left( \frac{1}{a_1},a_1\right) \cap \left( \frac{1}{a_2},a_2\right) = \left( \frac{1}{a_2},a_2\right)$

si $a_2 > a_1$ entonces $\left( \frac{1}{a_1},a_1\right) \cap \left( \frac{1}{a_2},a_2\right) = \left( \frac{1}{a_1},a_1\right)$

Por lo que vemos que en ningún caso la intersección es nula ¡¡¡Contradicción!!!

2. $T = \{ \emptyset, \{a\}, \{c\}, \{a,b\}, \{a,b,c\} \}$

¿Es topología?

No existe $\{a\} \cup \{c\} = \{a,c\}$

¿Es base?

- Si $X = \{a,b,c\}$ vemos que $a \in \{a\}, \; b \in \{a,b\} \text{ y } c \in \{c\}$ 
- Si $x \in X$ está en la intersección de los alguno de los elementos de la base como $x \in \{a\} \cap \{a,b\}$ vemos que siempre uno de los elementos de la intersección es ya un $B_3$ tal que $B_3 \subseteq B_1 \cap B_2, \;\; x \in B_3$

¿Es Hausdorff?

Ninguno de los [[1716491727-conjunto-abierto|entornos]] de $a \text{ y } b$ tienen una intersección nula (todos los entornos de $b$ contienen a $a$) 

3. $T = \{\emptyset, \{a\}, \{b\}, \{a,c\}, \{b,c\}, \{a,b,c\} \}$

¿Es topología?

No existe $\{a\} \cup \{b\} = \{a,b\}$

¿Es base?

No es base ya que para el elemento $c \in \{b,c\} \cap \{a,b,c\} = \{c\}$ no existe un $B_3 = \{c\} \in T$

¿Es Hausdorff?

Si es Hausdorff: el punto $a$ tiene el entorno $\{a\}$, el punto $b$ el entorno $\{b\}$ y el punto $c$ los entornos $b \notin \{a,c\}$ y $a \notin \{b,c\}$