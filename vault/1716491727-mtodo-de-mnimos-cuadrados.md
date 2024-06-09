---
id: 1716491727-mtodo-de-mnimos-cuadrados
aliases:
  - Método de mínimos cuadrados
tags:
  - estadística
---


- Se trata de encontrar la [[1716491727-regresin-lineal|recta]] tal que $\forall i \in \mathbb{N}:e_i = 0$
- Como no siempre es posible, se trata de resolver el siguiente problema de optimización $$min \sum_{i=1}^{n} e_i^2$$
- Por tanto hay que encontrar los $\beta_0 \beta_1 \in \mathbb{R}$ tales que minimicen la suma de los residuos

$$\beta_0 = \overline{y} - \beta_1 \overline{x}$$
$$
\beta_1 = \frac{s_{xy}}{s^2_x}
$$

Recta de regresión de $Y$ sobre $X$ (Para hacer predicciones de $y_i$)
$$y - \overline{y} = \frac{s_{xy}}{s_x^2}(x-\overline{x})$$
Recta de regresión de $X$ sobre $Y$ (Para hacer predicciones de $x_i$)
$$x - \overline{x} = \frac{s_{xy}}{s_{y}^2}(y - \overline{y})$$

![[1716491727-coeficiente-de-regresin|Coeficiente de regresión]]