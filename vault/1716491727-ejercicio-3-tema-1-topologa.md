---
id: 1716491727-ejercicio-3-tema-1-topologa
aliases:
 - Ejercicio 3 Tema 1 Topología
---

#topología 
## ¿Son [[1716491727-mtrica|distancias]] en $\mathbb{R}^2$?

- $d(A,B) = \sqrt{(x_2-x_1)^2 + (y_2 - y_1)^2}$

1. $d(A,A)=\sqrt{(x_1 - x_1)^2 + (y_1 - y_1)^2} = 0$
2. $d(B,A) = \sqrt{(x_1 - x_2)^2 + (y_1 - y_2)^2} = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2} = d(A,B)$
3. $d(A,C) \leq d(A,B) + d(B,C) \Longleftrightarrow$ $\sqrt{(x_3 - x_1)^2 + (y_3 - y_1)^2} \leq \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2} + \sqrt{(x_3 - x_2)^2 + (y_3 - y_2)^2}$

se trata de la [[1716491727-distancia-euclidiana|Distancia Euclidiana]]

![[Ejercicio 3 Tema 1 2023-10-28 21.07.38.excalidraw]]

- $d(A, B) = |x_2 - x_1| \times |y_2 - y_1|$

1. $A=(x_1,y_1)\;\;B=(x_1,y_2) \implies d(A,B)=|x_1 - x_1| \times |y_2 - y_1| = 0 \times |y_2 - y_1| = 0$

- $d(A,B)=|x_2 - x_1| + |y_2 - y_1|$

1. $d(A,A)=|x_1 - x_1| + |y_1 - y_1| = 0$
2. $d(B,A) = |x_1 - x_2| + |y_1 - y_2| = |x_2 - x_1| + |y_2 - y_1| = d(A,B)$
3. $d(A,C) \leq d(A,B) + d(B,C)$

![[Ejercicio 3 Tema 1 2023-10-28 21.18.45.excalidraw]]

- $d(A,B)=min(|x_2 - x_1|, |y_2 - y_1|)$

1. $A=(x_1,y_1) \;\; B=(x_1, y_2) \implies d(A,B)=min(|x-1 - x-1|,|y_2 - y_1|)=min(0,|y_2 - y_1|) = 0$

- $d(A,B)=max(|x_2 - x_1|, |y_2 - y_1|)$

1. $d(A,A)=max(|x_1 - x_1|,|y_1 - y_1|) = 0$
2. $d(B,A)=max(|x_1 - x_2|,|y_1 - y_2|) = max(|x_2 - x_1|,|y_2 - y_1|) = d(A,B)$
3. $d(A,C) \leq d(A,B) + d(B,C)$

Se trata de la [[1716491727-distancia-mximo|Distancia Máximo]]


![[Ejercicio 3 Tema 1 2023-10-28 21.27.34.excalidraw]]