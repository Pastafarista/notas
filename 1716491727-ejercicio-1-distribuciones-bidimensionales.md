---
id: 1716491727-ejercicio-1-distribuciones-bidimensionales
aliases:
  - Ejercicio 1 Distribuciones bidimensionales
tags:
  - estadística
---

## Dados los siguientes datos sobre ingresos de un grupo de familias al cabo de un mes, se pide construir las rectas de regresión

![[Pasted image 20231120114724.png]]

|     | 6   | 7   | 8   | 12  | 13  | 15  | 20  | 25  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
|   5  |     |     |     |     |  1   |     |     |   1  |
|   8  |  1   |     |  1   |     |     |     |     |     |
|   10  |     |     | 1    |     |     |     |     |   1  |
|  12   |     | 1    |     |     |     |     |     |     |
|   13  |     |     |     |     |     |     |  1   |     |
|  14   |     |     |     |     |     |  2   |     |     |
|  20 |     |     |     |     |     |     |     |   1  |

$X \equiv \text{Ingresos de un grupo de familias al cabo de un mes}$
$Y \equiv \text{Consumo de un grupo de familias al cabo de un mes}$

1. [[1716491727-media-aritmtica|Medias]]

$\overline{x} = \frac{8+15+20+25+25+25+8+13+7+6+12+15}{12} = 14.9166$
$\overline{y} = \frac{10+14+13+5+10+20+8+5+12+8+10+14}{12}=10.75$

2. [[1716491728-varianza|Varianzas]]

$s_x^2= \frac{\sum_{i=1}^{n}x_i^2}{n}-\overline{x}^2 = \frac{8^2 + 15^2 +20^2 +25^2 + 25^2 +25^2 + 8^2 + 13^2 +7^2 +6^2 +12^2 +15^2}{12} - (14.9166)^2 = 48.4117$
$s_y^2 = \frac{\sum_{i=1}^{}y^2_i}{n} - \overline{y}^2 = \frac{10^2 + 14^2 + 13^2 + 5^2 +10^2 + 20^2 + 8^2 + 5^2 + 12^2 + 8^2 + 10^2 + 14^2}{12} - (10.75)^2 = 16.3541$

3. [[1716491727-covarianza|Covarianza]]

$$
s_{xy} = \frac{1}{n} \sum_{i=1}^{n}x_i y_i - \overline{x} \cdot \overline{y} = \frac{8 \cdot 10 + 15 \cdot 14 + 20 \cdot 13 + 25 \cdot 5 + 25 \cdot 10 + 25 \cdot 20 + 8 \cdot 8 + 13 \cdot 5 + 7 \cdot 12 + 6 \cdot 8 + 12 \cdot  10 + 15 \cdot 14}{12} - (14.9166) \cdot (10.75) = 7.6465
$$

4. [[1716491727-mtodo-de-mnimos-cuadrados|rectas de regresión]]

- Recta de $X$ sobre $Y$

$$x - \overline{x} = \frac{s_{xy}}{s_{y}^2}(y - \overline{y}) \Longleftrightarrow x - (14.9166) = \frac{7.6465}{48.4117}(y - 10.75)$$

- Recta de $Y$ sobre $X$

$$y - \overline{y} = \frac{s_{xy}}{s_x^2}(x-\overline{x}) \Longleftrightarrow y - 10.75 = \frac{7.6465}{16.3541}(x - 14.9166)$$

![[geogebra-export.png]]

5. [[1716491727-coeficiente-de-relacin-de-pearson|Coeficiente de relación de Pearson]]

$$r_{xy}=\frac{s_{xy}}{s_x \cdot s_y} = \frac{7.6465}{\sqrt{48.4117} \cdot \sqrt{16.3541}}=0.27175$$
- La correlación entre las dos variables no es muy alta (interdependencia directa débil)
- Como $R^2 = (0.27175)^2 = 0.07384$, las predicciones tendrán una fiabilidad del $7.38 \%$
- Los valores teóricos están muy alejados de los observados y la recta de regresión pasa muy alejada de los puntos de la nube