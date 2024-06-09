---
id: 1716491727-ejercicio-2-espacios-topolgicos
aliases:
 - Ejercicio 2 Espacios Topológicos
---


## ¿Son [[1716491728-topologa|Topología]]'s?

1. $X = [0, +\infty ), \; T_a=\{(a, +\infty), \text{ donde a } \geq 0\}$

Si es topología ya que se trata claramente de una [[1716491728-topologa-de-tipo-matryoshka|Topología de tipo Matryoshka]], esta topología es conocida como [[1716491728-topologa-de-semirrectas-derechas|Topología de semirrectas derechas]]

2. $X = (-\infty, +\infty), \; T = \{\{(a, +\infty)\} \cup \{-\infty,a)\} \cup \{\emptyset,X\} \}$

No es topología ya que por ejemplo no existe $\{(2, +\infty)\} \cap \{(-\infty, 1)\} = \{(1,2)\}$

3. $T_a = \{U \subset X: \; |U| = \infty\}$

No es topología ya que por ejemplo, la intersección de $(-\infty,2]$ y $[2, +\infty)$ que es igual a 2, no tiene infinitos elementos
$$(-\infty, 2], [2, +\infty) \subset X, \; \{(-\infty, 2]\} \cap \{[2, +\infty)\} = \{2\}, \; |2| \neq \infty$$

4. $T_a = \{U \subset X: \; |X \setminus U| < \infty\}$

$U_1, U_2 \subset X : X \setminus U_1 = \{p_1, p_2, ..., p_n\} \;\; X \setminus U_2 = \{q_1, q_2, ..., q_k\}$

Entonces si en $U_1$ faltan $n$ elementos y en $U_2$ faltan $k$ elementos, en $U_1 \cup U_2$ faltan como mucho el menor de $n$ y $k$

Esta topología se la conoce como la [[1716491728-topologa-cofinita|Topología Cofinita]]