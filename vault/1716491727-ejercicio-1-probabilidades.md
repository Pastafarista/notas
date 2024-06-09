---
id: 1716491727-ejercicio-1-probabilidades
aliases:
  - Ejercicio 1 Probabilidades
tags:
  - estadística
---

## Se está realizando un estudio de pagos de préstamos. La [[1716491727-probabilidad|probabilidad]] de que una persona solicite un préstamos es de 0.3. De los préstamos de hipotecas, el $10\%$ no se paga, y para otro tipo de préstamos, el $80\%$ se paga

![[Ejercicio 1 Probabilidades 2023-11-21 19.42.40.excalidraw]]

1. Calcular la probabilidad de que una persona haya solicitado préstamos para hipoteca sabiendo que el pago se ha realizado

- Definamos los [[1716491727-sucesos|sucesos]]:
	
	- $A \equiv \text{Solicita hipoteca}$
	- $B \equiv Paga$

- Calculemos la probabilidad de $B$ usando el [[1716491727-teorema-de-probabilidad-total|teorema de probabilidad total]]
$$P(B) =\sum_{i=1}^{n}P(B/A_i) \cdot P(A_i) = (0.9 \cdot 0.3) + (0.8 \cdot0.7) = 0.83$$

- Nos piden calcular $P(A/B)$, para ello usaremos el [[1716491727-teorema-de-bayes|teorema de Bayes]]

$$P(A/B) = \frac{P(B/A) \cdot P(A)}{P(B)} = \frac{0.9 \cdot 0.3}{0.83} = 0.3253$$
2. Calcular la probabilidad de que no haya solicitado hipoteca sabiendo que no ha pagado el préstamo

- Nos piden $P(\overline{A}/\overline{B})$, usando Bayes
$$P(A/B) = \frac{P(\overline{B}/\overline{A}) \cdot P(\overline{A})}{P(\overline{B})} = \frac{0.2\cdot0.7}{1 - 0.83} = 0.8235$$