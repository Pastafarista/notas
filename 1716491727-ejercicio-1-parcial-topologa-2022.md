---
id: 1716491727-ejercicio-1-parcial-topologa-2022
aliases:
 - Ejercicio 1 Parcial topología 2022
---

#topología  

## ¿Son [[1716491727-mtrica|distancias]]?

1. $d(x,y) = |x^2 - y^2| \text{ en } \mathbb{R}$

	$d(x,-x)=|(x)^2 - (-x)^2| = |x^2 - x^2| = 0$
	Luego no es distancia

2. "La cantidad de caracteres de la unión menos la de la intersección"
$$\begin{split}
& \text{Ejemplo:} \\ \\
& \text{"mapa"} \cup \text{"mama"} = \{\text{m}, \text{a}, \text{p} \} \\
& \text{"mapa"} \cap \text{"mama"} = \{\text{m}, \text{a}\} \\
& d(\text{"mapa"},\text{"mama"}) = 3 - 2 = 1\\
\end{split}$$

	$d(A,A) = |A \cup A| - |A \cap A| = |A| - |A| = 0$
	$d(B,A)=|B \cup A| - |B \cap A| = |A \cup B| - |A \cap B| = d(A,B)$
	$d(A,B) \leq d(A,C) + d(B,C) \Longleftrightarrow |A \cup B| - |A \cap B| \leq |A \cup C| - |A \cap C| + |B \cup C| - |B \cap C|$
	![[Ejercicio 1 Parcial topología 2022 2023-11-04 17.15.33.excalidraw]]
	Como vemos claramente $A \cup B - A \cap B \subset (A \cup C - A \cap C) \cup (B \cup C - B \cap C)$ por lo que se ve que $d(A,B) \leq d(A,C) + d(B,C)$

[[Ejercicio 1 Parcial topología 2022 2023-11-04 17.15.33.excalidraw|]]