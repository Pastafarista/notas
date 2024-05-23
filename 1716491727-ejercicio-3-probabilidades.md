---
id: 1716491727-ejercicio-3-probabilidades
aliases:
  - Ejercicio 3 Probabilidades
tags:
  - estadística
---

## Se tienen dos cajas. La caja 1 tiene cuatro bolas blancas y tres negras. La caja 2 tiene tres bolas blancas y cuatro bolas negras. Se toma una caja al azar y seguidamente se toma una bola al azar de la caja seleccionada

- Vamos a definir nuestros [[1716491727-sucesos|Sucesos]]
$$\begin{split}
	& A \equiv \text{Se escoge la caja 1}\\
	& B \equiv \text{Saca una bola blanca}
\end{split}$$
- Calculemos las [[1716491727-probabilidad-condicionada|probabilidades condicionadas]]
$$\begin{split}
	& P(B/A) = \frac{4}{4+3} = 0.5714 \\
	& P(B/\overline{A}) = \frac{3}{3+4} = 0.4285
\end{split}$$

- Dibujemos el diagrama de árbol

![[Ejercicio 3 Probabilidades 2023-11-21 21.20.33.excalidraw]]

1. ¿Cuál es la [[1716491727-probabilidad|Probabilidad]] de que la bola extraída sea blanca?

- Nos piden $P(B)$, usando el [[1716491727-teorema-de-probabilidad-total|Teorema de probabilidad total]]
$$P(B) =\sum_{i=1}^{n}P(B/A_i) \cdot P(A_i) = (P(B/A) \cdot P(A)) + (P(B/\overline{A}) \cdot P(\overline{A})) = (\frac{4}{7} \cdot \frac{1}{2}) + (\frac{3}{7} \cdot \frac{1}{2}) = \frac{1}{2}$$

2. ¿Cuál es la probabilidad de que la bola sea negra?
$$P(\overline{B})=1-P(B) = 1 -0.5 = 0.5$$

3. Asumiendo a partir de ahora que la probabilidad de elegir la caja 1 es el doble que la de elegir la caja 2, si se repite el experimento dos veces seguidas (con reemplazamiento de bolas), ¿Cuál es la probabilidad de extraer dos bolas blancas?

- Para sacar cuanto es $P(A)$ debemos resolver la siguiente ecuación 
$$\begin{cases}
	& P(A) = 2 \cdot P(\overline{A})\\
	& P(A) + P(\overline{A}) = 1
\end{cases} \implies P(A) = \frac{2}{3} $$

- Ahora la probabilidad de que la bola sea blanca será
$$P(B) =(P(B/A) \cdot P(A)) + (P(B/\overline{A}) \cdot P(\overline{A})) = (\frac{4}{7} \cdot \frac{2}{3}) + (\frac{3}{7} \cdot \frac{1}{3}) = \frac{11}{21}$$

- Como hay reemplazamiento, los dos sucesos van a ser [[1716491727-sucesos-independientes|independientes]] por lo que la intersección de ambos será igual al producto de las probabilidades por separado
$$P(B\cap B') = P(B) \cdot P(B') = \frac{11}{21} \cdot \frac{11}{21} = \frac{121}{441}$$

4. Ahora, el experimento consiste en elegir una caja, y tomar dos bolas de la misma caja. Si se toman con reemplazamiento de la misma caja seleccionada, ¿Cuál es la probabilidad de que se obtengan dos bolas blancas?

- Si definimos $C \equiv \text{Sacar dos blancas de la caja}$ podemos calcular $P(C)$ con el mismo procedimiento de antes usando el [[1716491727-teorema-de-probabilidad-total|Teorema de probabilidad total]]

$$\begin{split}
	& P(C/A) = \frac{4}{7} \cdot \frac{4}{7} = \frac{16}{49}\\
	& P(C/\overline{A}) = \frac{3}{7} \cdot \frac{3}{7} = \frac{9}{49}\\
	& P(C) = \left(\frac{16}{49} \cdot \frac{2}{3} \right) + \left(\frac{9}{49} \cdot \frac{1}{3} \right) = \frac{41}{147}
\end{split}$$

5. Si se toman sin reemplazamiento de la misma caja seleccionada, ¿Cuál es la probabilidad de que se obtengan dos bolas blancas?

- Dibujemos el diagrama de árbol

![[Ejercicio 3 Probabilidades 2023-11-21 21.58.13.excalidraw]]

- Ahora tenemos que calcular $P(B_1 \cap B_2)$, si no hay reemplazo las dos extracciones no son independientes por lo que usando la [[1716491727-probabilidad-condicionada|Probabilidad condicionada]]  sabemos que ahora $P(B_1 \cap B_2) = P(B_1 / B_2) \cdot P(B_2) = P(B_1) \cdot P(B_2 / B_1)$

$$\begin{split}
	& P(B_1 \cap B_2) = P(B_2/B_1 \cap A) \cdot P(B_1 / A)) \cdot P(A) + P(B_2 / B_1 \cap \overline{A}) \cdot P(B_1 \cap \overline{A}) \cdot P(\overline{A})\\
	& P(B_1 \cap B_2) = \frac{3}{6} \cdot \frac{4}{7} \cdot \frac{2}{3} + \frac{2}{6} \cdot \frac{3}{7} \cdot \frac{1}{3} = \frac{5}{21}
\end{split}$$