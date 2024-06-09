---
id: 1713105354-laboratorio-1-clculo-numrico
aliases:
  - Laboratorio 1 cálculo numérico
  - Laboratorio 1
tags:
  - cálculo-numérico
---

# Laboratorio 1

### Problema 1: Resolución de la ecuación de segundo grado

La ecuación de segundo grado $ax^2+bx+c=0$ se resuelve de la forma ordinaria utilizando las fórmulas de Bhaskara:

$$
\begin{split}
    & x_{1} = \frac{-b + \sqrt{b^2-4ac}}{2a}\\
    & x_{2} = \frac{-b - \sqrt{b^2-4ac}}{2a}
\end{split}
$$

1. Pruebe que si se define

$$
\begin{split}
    & y_{1} = \frac{2c}{-b - \sqrt{b^2-4ac}}\\    
    & y_{2} = \frac{2c}{-b + \sqrt{b^2-4ac}}
\end{split}
$$

entonces $y_{1} = x_{1}$ y $y_{2} = x_{2}$.

#### **Prueba:**

- Para $y_{1}$:
  
$$
\begin{split}
	y_{1} & = \frac{2c}{-b - \sqrt{b^2-4ac}} =\\
	& = \frac{2c}{-(b + \sqrt{b^2-4ac})} \cdot \frac{b - \sqrt{b^2-4ac}}{b - \sqrt{b^2-4ac}} = \\
	&  = \frac{2c(b - \sqrt{b^2-4ac})}{-(b^2 - (b^2-4ac))} = \\
	& = \frac{b - \sqrt{b^2-4ac}}{-2a} = \\
	& = \frac{-b + \sqrt{b^2-4ac}}{2a} = x_{1}
\end{split} 
$$

- Para $y_{2}$:
   
$$
\begin{split}
	y_{2} &= \frac{2c}{-b + \sqrt{b^2-4ac}} = \\
	& = \frac{2c}{-b + \sqrt{b^2-4ac}} \cdot \frac{b + \sqrt{b^2-4ac}}{b + \sqrt{b^2-4ac}} = \\
	& = \frac{2c(b + \sqrt{b^2-4ac})}{-b^2 + b^2 -4ac} = \\
	& = \frac{b + \sqrt{b^2-4ac}}{-2a} = \\
	& = \frac{-b - \sqrt{b^2-4ac}}{2a} = x_{2}
\end{split}
$$

2. Evalúe, utilizando Python, $x_{1},x_{2},y_{1},y_{2}$ cuando $a=1, b=9^{12} \text{ y } c = -3$.

- $x_{1}$ dará 0 ya que $b$ y $\sqrt{b^2-4ac}$ son números grandes muy cercanos que por el límite de la precisión de la máquina se cancelan.
- $x_{2}$ y ${y_{1}}$ darán resultados correctos.
- $y_{2}$ dará error de división entre cero ya que $b$ y $\sqrt{b^2-4ac}$ son números grandes muy cercanos que por el límite de la precisión de la máquina se cancelan.

```
a = 1, b = 282429536481, c = -3
x_1 = 0.0
x_2 = -282429536481.0
y_1 = 1.062211848441645e-11
Error y_2: float division by zero
```

3. Evalúe, utilizando python, $x_{1},x_{2},y_{1},y_{2}$ cuando $a=1, b=-9^{12} \text{ y } c = -3$.

- $x_{1}$ y $y_{2}$ darán resultados correctos.
- $x_{2}$ y $y_{1}$ darán los mismos errores que en el apartado anterior ya que hemos cambiado el signo de $b$.

```
a = 1, b = -282429536481, c = -3
x_1 = 282429536481.0
x_2 = 0.0
Error y_1: float division by zero
y_2 = -1.062211848441645e-11
```
4. Para cada uno de los apartados anteriores, indica cuáles son las soluciones de la ecuación de segundo grado y explique los resultados obtenidos en Python.

- Para el primer apartado, las soluciones de la ecuación de segundo grado son $x_{1} = 1.062211848441645e-11$ y $x_{2} = -282429536481.0$. Los resultados obtenidos en Python no son los esperados en $x_{1}$ y $y_{2}$ debido al límite de precisión de la mantisa.

- Para el segundo apartado, las soluciones de la ecuación de segundo grado son $x_{1} = 282429536481.0$ y $x_{2} = -1.062211848441645e-11$. Los resultados obtenidos en Python no son los esperados en $x_{2}$ y $y_{1}$ debido al límite de precisión de la mantisa.

### Problema 2: Algoritmo de Horner I

El algoritmo de Horner se define formalmente así. $\text{Dados un natural no nulo } N \text{ y } a_{0},\ldots a_{N}, x_{0}, \text{ hacer:}$

$$
\begin{split}
    & q_{N-1} \coloneqq a_{N}\\
    & q_{N -i - 1} \coloneqq q_{N - i} \cdot x_{0} + a_{N - i}, \text{ para } i = 1, \ldots, N.
\end{split}
$$

1. Demuestre con el mayor rigor de que sea capaz, que $Q(x) = q_{N - 1}x^{N-1} + \dots + q_{0}$ y $q_{-1}$ son respectivamente el cociente y resto de la división euclidea de $P$ entre $x - x_{0}$.

#### Prueba:

Para demostrar que $Q(x) = q_{N - 1}x^{N-1} + \dots + q_{0}$ y $q_{-1}$ son respectivamente el cociente y resto de la división euclidea de $P$ entre $x - x_{0}$, se debe demostrar que $P(x) = Q(x)(x - x_{0}) + q_{-1}$.

Para ello, con el algoritmo de Horner definimos:

$$
\begin{split}
    & a_{N} = q_{N-1}\\
    & a_{N-1} = q_{N-2} - q_{N-1}x_{0}\\
    & \ldots\\
    & a_{1} = q_{0} - q_{1}x_{0}\\
    & a_{0} = q_{-1} - q_{0}x_{0}
\end{split}
$$

Ahora, desarrollamos $Q(x)(x - x_{0}) + q_{-1}$:

$$
\begin{split}
    & (x - x_{0})(q_{N - 1}x^{N-1} + \dots + q_{0}) + q_{-1} =\\
    & (q_{N - 1}x^{N} + q_{N - 2}x^{N-1} + \dots + q_{1}x^2 + q_{0}x) -\\
    & (q_{N - 1}x^{N-1}x_{0} + \dots + q_{1}x x_{0} + q_{0}x_{0}) + q_{-1} =\\
    & x^{N}(q_{N - 1}) + x^{N-1}(q_{N - 2} - q_{N - 1}x_{0}) + \dots + x(q_{0} - q_{1}x_{0}) + (q_{-1} - q_{0}x_{0}) =\\
    & x^{N}a_{N} + x^{N-1}a_{N-1} + \dots + x^{2}a_{2} + x a_{1} + a_{0} = P(x)
\end{split}
$$

2. Demuestre como consecuencia, que $q_{-1} = P(x_{0})$

#### Prueba:

$$
\begin{split}
	& P(x_0) = (x_0 - x_0)(q_{N - 1}x_{0}^{N-1} + \dots + q_{0}) + q_1 =\\
	& = 0 \cdot (q_{N - 1}x_{0}^{N-1} + \dots + q_{0}) + q_{-1} = q_{-1}
\end{split}
$$

### Problema 3: Algoritmo de Horner II

Utilize reiteradamente el algoritmo de Horner para escribir $x^3 + x^2 - x - 1$ en potencias de $(x - 2)$.

- Empezamos con el polinomio $P(x) = x^3 + x^2 - x - 1$ y $x_0 = 2$.

$$
\begin{split}
   q_{3} & = 1\\ 
   q_{2} & = q_{3} \cdot 2 + 1 = 3\\
   q_{1} & = q_{2} \cdot 2 - 1 = 5\\
   q_{0} & = q_{1} \cdot 2 - 1 = 9
\end{split}
$$

- Ahora volvemos a aplicar el algoritmo de Horner con el polinomio $Q_{1}(x) = x^2 + 3x + 5$ y $x_0 = 2$.

$$
\begin{split}
   q_{2} & = 1\\ 
   q_{1} & = q_{2} \cdot 2 + 3 = 5\\
   q_{0} & = q_{1} \cdot 2 + 5 = 15
\end{split}
$$

- Finalmente, aplicamos el algoritmo de Horner con el polinomio $Q_{2}(x) = x + 5$ y $x_0 = 2$.

$$
\begin{split}
   q_{1} & = 1\\ 
   q_{0} & = q_{1} \cdot 2 + 5 = 7
\end{split}
$$

Utilizando los restos y el polinomio $Q_{3}(x) = 1$, podemos escribir $x^3 + x^2 - x - 1$ en potencias de $(x - 2)$:

$$
\begin{split}
    & 9 + (x - 2)(15 + (x - 2)(7 + (x - 2)(1))) =\\
    & 9 + 15(x - 2) + 7(x - 2)^2 + (x - 2)^3 =\\
    & (x - 2)^3 + 7(x - 2)^2 + 15(x - 2) + 9
\end{split}
$$

