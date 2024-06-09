---
id: 1716491727-ejercicio-4-distribuciones-bidimensionales
aliases:
  - Ejercicio 4 Distribuciones bidimensionales
tags:
  - estadística
---

Examen Final MAIS 1ºA Parcial 1 

## En una empresa se analiza la posible existencia de una relación entre la edad $(X)$ de sus trabajadores y el número de días de baja $(Y)$ a lo largo de un año. Se han obtenido los siguientes datos correspondientes a 5 trabajadores

- $\overline{x} = 44.2$
- $\overline{y}=8.4$
- $\sum_{i=1}^{n}x_i^2=10439$
- $\sum_{i=1}^{n}y_i^2=368$
- $\sum_{i=1}^{n}x_i y_i = 1937$

1. Obtener una medida de la correlación entre ambas variables e interpretarla

- [[1716491728-varianza|Varianzas]]

$$s_x^2= \frac{\sum_{i=1}^{n}x_i^2}{n}-\overline{x}^2 = \frac{10439}{5} - 44.2^2 = 133.56$$
$$s_y^2 = \frac{\sum_{i=1}^{n}y_i^2}{n} - \overline{y}^2 = \frac{368}{5} - 8.4^2 = 3.04$$

- [[1716491727-covarianza|Covarianza]]

$$s_{xy} = \frac{1}{n}\sum_{i=1}^n x_i y_i - \overline{x} \cdot \overline{y} = \frac{1937}{5} - 44.2 \cdot 8.4 = 16.12$$
- [[1716491727-coeficiente-de-relacin-de-pearson|Coeficiente de relación de Pearson]]

$$r_{xy} = \frac{s_{xy}}{s_x \cdot s_y} = \frac{16.12}{\sqrt{133.56} \cdot \sqrt{3.04}} =0.8$$
- Es una dependencia directa notable
- La recta se ajusta mas o menos bien a la nube de puntos, con una fiabilidad de predicciones del $64\%$
- Las dos rectas forman un ángulo pequeño

2. Hallar una predicción del tiempo de baja de un trabajador de 32 años

- [[1716491727-mtodo-de-mnimos-cuadrados|Recta de regresión]] de $Y$ sobre $X$

$$\begin{split}
	& y - \overline{y} = \frac{s_{xy}}{s_x^2}(x-\overline{x})\\
	& y - 8.4 = \frac{16.12}{133.56}(x - 44.2)
\end{split}$$

- Si $x=32$ entonces:

$$y = 8.4 + \frac{16.12}{133.56}(32 - 44.2) = 7.9275$$

Si el trabajador tiene 32 años nuestro modelo predice que se tomará 8 días de baja en un año

3. ¿Cuál es la variabilidad del tiempo de baja que se explica por la edad de los trabajadores?¿Qué porcentaje representa esa variabilidad?

- [[1716491728-varianza-explicada|Varianza explicada]]

$$V_e = s_y^2 \cdot R^2 = 3.04 \cdot 0.64 = 1.9456$$
- $1.9456$ unidades de varianza que representan el $64 \%$ de la variabilidad total del producto

4. Calcular la pendiente de la [[1716491727-mtodo-de-mnimos-cuadrados|recta de regresión]] de $y$ sobre $x$ e interpretarla en el contexto del problema

- Ya la habíamos calculado, era de $b_{yx} = \frac{16.12}{133.56} = 0.1206$, lo que significa que por cada $100$ años de edad los días de baja aumentan en 12

5. Razonar si la edad media es más o menos representativa que el número medio de días de baja para los trabajadores de dicha empresa

- [[1716491727-coeficiente-de-variacin-de-pearson|Coeficiente de variación de Pearson]]

$$C.V._x = \frac{s_x}{\overline{x}} = \frac{\sqrt{133.56}}{44.2} = 0.2614$$
$$C.V._y = \frac{s_y}{\overline{y}} = \frac{\sqrt{3.04}}{8.4} = 0.2075$$

- El número de días de baja medio es más representativa que la edad media
- Presenta mayor dispersión la distribución de edades $X$

6. Si nos facilitan además las edades de los 5 trabajadores de la empresa que son $X = \{50,44,37,60,30\}$, dar una medida que permita analizar la simetría de la edad de esos trabajadores e interpretarla. Interpretar también los valores que uses en la fórmula correspondiente.

- [[1716491727-coeficiente-de-asimetra-de-fisher|Coeficiente de asimetría de Fisher]]

$$\begin{split}
	& A_F = \frac{\sum_{n}^{i=1}(x_i - \overline{x})^3}{n \cdot s^3}=\\
	& = \frac{(50-44.2)^3+(44-44.2)^3+(37-44.2)^3+(60-44.2)^3+(30-44.2)^3}{5 \cdot 11.5568^3}=\\
	& = 0, 0046
\end{split}$$

Es prácticamente simétrica, (ligerísimamente asimétrica a la izquierda)