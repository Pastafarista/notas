---
id: 1716491727-ejercicio-6-probabilidades
aliases:
  - Ejercicio 6 Probabilidades
tags:
  - estadística
---

Examen extraordinario MAIS 1A

## De un test para detectar la presencia de un determinado virus se sabe que la [[1716491727-probabilidad|probabilidad]] de que resulte positivo en personas enfermas es del 96%, y la probabilidad de que el test falle en personas sanas es del 5%. Se sabe también que las personas infectadas por el virus ascienden al 0.1% de la población.

- Definamos nuestros [[1716491727-sucesos|sucesos]]
$$\begin{split}
	& A \equiv \text{Probabilidad de que una persona aleatoria padezca la enfermedad}\\
	& B \equiv \text{Probabilidad de que el test de positivo}	
\end{split}$$
![[Ejercicio 6 Probabilidades 2023-11-22 10.06.32.excalidraw]]


1. Si una persona ha obtenido un test negativo, ¿Cuál es la probabilidad de que esté equivocado?

- Nos piden $P(\overline{A}/\overline{B})$

- Primero vamos a calcular $P(\overline{B})$ usando el [[1716491727-teorema-de-probabilidad-total|teorema de probabilidad total]]
$$P(\overline{B}) =\sum_{i=1}^{n}P(\overline{B}/A_i) \cdot P(A_i) = 0.001 \cdot 0.04 + 0.999 \cdot 0.95 = 0.9490 $$

- Ahora vamos a calcular $P(A/\overline{B})$ usando el [[1716491727-teorema-de-bayes|teorema de Bayes]]
$$P(A/\overline{B}) = \frac{P(\overline{B}/A) \cdot P(A)}{P(\overline{B})} = \frac{0.04 \cdot 0.001}{0.9490} = 0.000042149$$

Entonces la probabilidad de que el test está equivocado si a la persona le ha salido un test negativo es del $0.0042149 \%$

2. ¿Cuál es el porcentaje de positivos que se obtienen con ese test?

- Nos piden $P(B)$ usando que $P(B) = 1 - P(\overline{B})$
$$P(B) = 1 - 0.9490 = 0.051$$

Se obtiene un $5.09 \%$

Hay un $5.1\%$ de positivos

3. ¿Cuáles son los coeficientes de falso-positivo y falso-negativo del test?

- El coeficiente de falso-positivo será la probabilidad de que ocurra $B$ sabiendo que $\overline {A}$
$$P(B/\overline{A}) = 0.05$$

- El de falso-negativo será $P(\overline{B}/A)$
$$P(\overline{B}/A) = 0.04$$

El coeficiente de falso-positivo es del $5 \%$ y el de falso-negativo del $4\%$