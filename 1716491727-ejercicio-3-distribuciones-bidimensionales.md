---
id: 1716491727-ejercicio-3-distribuciones-bidimensionales
aliases:
  - Ejercicio 3 Distribuciones bidimensionales
tags:
  - estadística
---

Examen extraordinario INSO 3W

## En una empresa se pretende analizar la relación existente entre las ventas totales $X$ y las exportaciones $Y$, expresadas en Millones de euros.

- Las dos [[1716491727-regresin-lineal|rectas]] se cortan en el punto $(6,4)$
- Por cada millón de euros que se incrementan las exportaciones, el incremento de las ventas totales, bajo el [[1716491727-mtodo-de-mnimos-cuadrados|modelo lineal ]] de $Y$ sobre $X$, es de $1.15M$ euros
- Si se incrementan en un millón de euros las ventas totales, las exportaciones aumentarían en $860 0000$ euros
- La dispersión relativa de las exportaciones $Y$, medida en términos de  [[1716491727-coeficiente-de-variacin-de-pearson|coeficiente de variación]], ha sido de $50\%$

1. Con estos supuestos, predecir las exportaciones de la empresa en un período en que las ventas totales han sido de $25$ millones de euros y dar una medida de fiabilidad de dicha predicción

De los datos concluimos:

- $\overline{x} = 6, \;\; \overline{y}=4$
- $\frac{s_{xy}}{s_x^2} = 0.86$
- $\frac{s_{xy}}{s_y^2} = 1.15$
- $C.V._y = \frac{s_y}{\overline{y}} = 0.5$

Sacar el resto de los datos:

$$s_y = 0.5 \cdot \overline{y} = 0.5 \cdot 4 = 2 \implies s_y^2=4$$
$$s_{xy}=1.15 \cdot s_y^2=1.15 \cdot 4 = 4.6$$
$$s_x^2= \frac{s_{xy}}{0.86}=\frac{4.6}{0.86}=5,3488$$

Predecir exportaciones ($Y$) con unas ventas ($X$) de $25$ millones de euros

- [[1716491727-mtodo-de-mnimos-cuadrados|Recta de regresión]] de $Y$ sobre $X$

$$\begin{split}
	& r: y - \overline{y} = \frac{s_{xy}}{s_x^2}(x-\overline{x})\\
	& y - 4 = 0.86(x - 6)
\end{split}$$

- Si $x=25$, entonces
$$y-4=0.86(25-6)  \Longleftrightarrow y =4 + 0.86 \cdot 19 = 20,34$$

- [[1716491727-coeficiente-de-relacin-de-pearson|Coeficiente de relación de Pearson]]

$$r_{xy} = \frac{s_{xy}}{s_x \cdot s_y} = \frac{4.6}{\sqrt{4}\cdot\sqrt{5.3488}}=0.9944$$

- [[1716491727-coeficiente-de-determinacin-lineal|Coeficiente de determinación lineal]]

$$R^2 = r^2 = 0.9944^2 =0.9890$$

La fiabilidad de la predicción es del $98.90\%$

2. Calcular el coeficiente de correlación e interpretarlo

- Ya lo hemos calculado, vamos a interpretarlo:
	- Se trata de una dependencia directa muy fuerte
	- La recta se ajusta perfectamente a la recta de puntos
	- Los variables teóricos son muy próximos que los observados
	- Rectas de regresión casi coincidentes
	- Predicciones con alta fiabilidad $(98.90\%)$

3. Comparar la [[1716491727-medidas-de-dispersin-estadstica|dispersión]] relativa de ambas distribuciones

- [[1716491727-coeficiente-de-variacin-de-pearson|Coeficiente de variación de Pearson]]
	
	$C.V._x = \frac{s_x}{\overline{x}} = \frac{\sqrt{5.3488}}{6} = 0.3854$
	$C.V._y = 0.5$

Interpretación:

- Existe menor dispersión en las ventas $X$ que en las exportaciones $Y$
- Las ventas medias ofrecen una medida más representativa de su distribución