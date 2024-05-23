---
id: 1716491727-ejercicio-5-probabilidades
aliases:
  - Ejercicio 5 Probabilidades
tags:
  - estadística
---

## Una gestora administra 3 fondos (fondo A, B y C). El patrimonio que gestiona es de $1400$ millones de euros en el fondo $A$, $850$ millones en el $B$ y $750$ millones en el $C$. Dada la evolución de los tipos de interés, la [[1716491727-probabilidad|probabilidad]] de que la gestora obtenga rendimientos anuales relativos positivos es del $99 \%$, $60 \%$ y $75 \%$ respectivamente en cada uno de los fondos

1. Si un partícipe invirtió en un fondo y obtuvo una rentabilidad real negativa, ¿Cuál es la probabilidad de que invirtiera en el fondo $C$?

- Primero definamos nuestros sucesos:
$$\begin{split}
	& A \equiv \text{Invierte en el fondo A} \\
	& B \equiv \text{Invierte en el fondo B} \\
	& C \equiv \text{Invierte en el fondo C}\\
	& R \equiv \text{Obtiene una rentabilidad positiva}
\end{split}$$
- Para calcular cual es la probabilidad de que invirtiese en cada uno de los fondos tenemos que usar la [[1716491727-definicin-clsica-probabilidad|definición clásica de probabilidad]]
$$\begin{split}
	& P(A) = \frac{1400}{1400+850+750} = \frac{7}{15}\\
	& P(B) = \frac{850}{3000} = \frac{17}{60}\\
	& P(C) = \frac{750}{3000} = \frac{1}{4}
\end{split}$$

- Primero calcularemos la probabilidad de $\overline{R}$ usando el [[1716491727-teorema-de-probabilidad-total|teorema de probabilidad total]]
$$\begin{split}
	& P(\overline{R}) = P(\overline{R}/A) \cdot P(A) + P(\overline{R}/B) \cdot P(B) + P(\overline{R}/C) \cdot P(C) = \\
	& = \frac{7}{15} \cdot (1 - 0.99) + \frac{17}{60} \cdot (1 - 0.6) + \frac{1}{4} \cdot (1 - 0.75) = 0.1805
	\end{split}$$

- Nos piden $P(C/\overline{R})$, usando el [[1716491727-teorema-de-bayes|teorema de Bayes]]
$$P(C/{\overline{R}}) = \frac{P(\overline{R}/C) \cdot P(C)}{P(\overline{R})} = \frac{0.25 \cdot \frac{1}{4}}{0.1805} = 0.3462$$