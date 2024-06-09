---
id: 1716491727-ejercicio-4-probabilidades
aliases:
  - Ejercicio 4 Probabilidades
tags:
  - estadística
---

## Sólo 1 de 1000 adultos padece una enfermedad rara para la que se ha creado una prueba de diagnóstico. La prueba es tal que cuando un individuo está enfermo, se presenta un resultado positivo el 99% de las veces, mientras que en individuos sanos el examen será positivo sólo en el 2% de las ocasiones.

1. Si se somete a la prueba un individuo seleccionado al azar y da positivo ¿Cuál es la probabilidad de que realmente tenga la enfermedad?

- Definamos los [[1716491727-sucesos|sucesos]]

	$A \equiv \text{Padece la enfermedad}$
	$B\equiv \text{La prueba da positivo}$

![[Ejercicio 4 Probabilidades 2023-11-22 09.01.42.excalidraw]]

- Primero calculemos $P(B)$ usando el [[1716491727-teorema-de-probabilidad-total|teorema de probabilidad total]]
$$P(B) =\sum_{i=1}^{n}P(B/A_i) \cdot P(A_i) = (0.99 \cdot 0.001) + (0.999 \cdot 0.02) = 0.02097$$

- Nos piden $P(A/B)$, usando el [[1716491727-teorema-de-bayes|teorema de Bayes]]
$$P(A/B) = \frac{P(B/A) \cdot P(A)}{P(B)} = \frac{0.99 \cdot 0.001}{0.02097} = 0.04721$$