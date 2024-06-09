---
id: 1716491727-ejercicio-2-distribuciones-bidimensionales
aliases:
  - Ejercicio 2 Distribuciones bidimensionales
tags:
  - estadística
---

Examen Extraordinario MAIS 1A Ejercicio 1

## Queremos analizar si existe relación lineal entre la distancia y el tiempo de viaje transcurrido entre el domicilio y el lugar de trabajo. Se han analizado las distancias y tiempos de 5 empleados y los datos son lo siguientes

$X\equiv \text{distancia (km)}, \; X = \{3,7,11.1,17,12\}$
$Y \equiv \text{tiempo (min)} \; Y = \{8,18,26,40,33\}$

1. ¿Puedes decir que existe una [[1716491727-coeficiente-de-relacin-de-pearson|relación lineal]] entre las variables distancia y tiempo de viaje? Interpretar el valor de $r$

- [[1716491727-media-aritmtica|Medias]]
$$\begin{split}
	& \overline{x} = \frac{3+7+11.1+17+12}{5}= 10.02 \\
	& \overline{y} = \frac{8+18+26+40+33}{5}= 25
\end{split}$$

- [[1716491728-varianza|Varianzas]]
$$\begin{split}
	& s_x^2 = \frac{\sum_{i=1}^{n}x_i^2}{n} - \overline{x}^2 = \frac{3^2 + 7^2 +(11.1)^2 +17^2 + 12^2}{5} - (10.02)^2 = 22.4416\\
	& s_y^2 = \frac{\sum_{i=1}^n y_i ^2}{n} - \overline{y}^2 = \frac{8^2 + 18^2 + 26^2 + 40^2 + 33^2}{5} - 25^2 = 125.6
\end{split}$$
- [[1716491727-covarianza|Covarianza]]

$$s_{xy}=\frac{1}{n}\sum_{i=1}^{n}x_i y_i - \overline{x} \cdot \overline{y} = \frac{1}{5} (3 \cdot 8 + 7 \cdot 18 + 11.1 \cdot 26 + 17 \cdot 40 + 12 \cdot 33) - 10.02 \cdot 25 = 52.42$$

- [[1716491727-coeficiente-de-relacin-de-pearson|Coeficiente de relación de Pearson]]

$$r_{xy} = \frac{s_{xy}}{s_x \cdot s_y} = \frac{52.42}{\sqrt{22.4416} \cdot \sqrt{125.6}} = 0.9873$$
Tienen una relación lineal de dependencia directa muy fuerte 

2. Predecir el tiempo que tarda en llegar al trabajo un empleado que vive a $14 \; km$ de distancia y dar una medida de la fiabilidad de la predicción 

- [[1716491727-mtodo-de-mnimos-cuadrados|Recta de regresión]] de $Y$ sobre $X$
$$x - \overline{x} = \frac{s_{xy}}{s_{y}^2}(y - \overline{y}) \Longleftrightarrow x - 10.02 = \frac{52.42}{125.6}(y - 25)$$
Entonces si $x= 14$
$$\begin{split}
	& 14 - 10.02 = 0.4173 \cdot (y - 25) \Longleftrightarrow y = \frac{3.98}{0.4173} + 25\Longleftrightarrow\\ 
	& y = 34.5375
\end{split}$$
Nuestra predicción si la distancia es de $14 \; km$ es de $34.53 \; min$

- [[1716491727-coeficiente-de-determinacin-lineal|Coeficiente de determinación lineal]]

$$R^2 = r^2 = 0.9748$$
Nuestra predicción tiene una fiabilidad del $97.48\%$

3. Cual de las dos variables es más dispersa

- [[1716491727-coeficiente-de-variacin-de-pearson|Coeficiente de variación de Pearson]]

$$\begin{split}
	& C.V._x = \frac{s_x}{\overline{x}} = \frac{\sqrt{22.4416}}{10.02} = 0.4727\\
	& C.V._y = \frac{s_y}{\overline{y}} = \frac{\sqrt{125.6}}{25} = 0.4482
\end{split}$$
5. ¿Qué porcentaje de variabilidad en el tiempo de llegada queda explicada por la distancia?

- Casi toda la variabilidad de $Y$ queda explicada por $X$ mediante el ajuste
- Le doy un porcentaje del $98.73\%$

![[regresion.png]]


```python
X = [3, 7, 11.1, 17, 12]
Y = [8,18,26,40,33]

plt.scatter(X,Y)
  
# Recta de regresión
a = statistics.covariance(X,Y)/statistics.variance(X)
b = statistics.mean(Y) - a*statistics.mean(X)

plt.plot(X, [a*x + b for x in X], color='red')
plt.savefig("regresion.png")
```