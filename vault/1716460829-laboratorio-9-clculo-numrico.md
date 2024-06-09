---
id: 1716460829-laboratorio-9-clculo-numrico
aliases:
  - Laboratorio 9 cálculo numérico
  - Laboratorio 9
tags:
  - cálculo-numérico
---

# Laboratorio 9

## Problema 1: Iteración de punto fijo

Dada la función $f(x) = x - 0.5 \sin (x) - 0.7$, se propone utilizar el método de iteración de punto fijo con $x_{0}=0$ y 

$$
g(x) = x - \frac{x - 0.5 \sin (x) - 0.7}{1 - 0.5 \cos (x)}
$$

para encontrar una aproximación de la raíz de $f(x)$.

1. Demostrar que el cero buscado $\alpha$ es un [[1716491727-punto-fijo|punto fijo]] de $g(x)$.

Sabemos que $f(\alpha) = \alpha - 0.5 \sin(\alpha) - 0.7 = 0$, por lo tanto:

$$
g(\alpha) = \alpha - \frac{\alpha -0.5 \sin(\alpha) - 0.7}{1 - 0.5 \cos (\alpha)} = \alpha  - \frac{0}{1 - 0.5 \cos (\alpha)} = \alpha
$$

2. Demostrar la convergencia cuadrática del método de iteración de punto fijo para la función $g(x)$.

Para demostrar la convergencia cuadrática, necesitamos demostrar que $g'(\alpha) = 0$ y que existe $g''(\alpha)$:

$$
g'(x) = 1 - \frac{(1 - 0.5 \cos(x))(1 - 0.5 \cos(x)) - (x - 0.5 \sin(x) - 0.7)(0.5 \sin(x))}{(1 - 0.5 \cos(x))^2}
$$

Entonces $g'(\alpha)$:

$$
\begin{split}
    & g'(\alpha) = 1 - \frac{(1 - 0.5 \cos(\alpha))(1 - 0.5 \cos(\alpha)) - (\alpha - 0.5 \sin(\alpha) - 0.7)(0.5 \sin(\alpha))}{(1 - 0.5 \cos(\alpha))^2} = \\
    & = 1 - \frac{(1-0.5 \cos(\alpha))^2) - 0 \cdot (0.5 \sin(\alpha))}{(1 -0.5 \cos(\alpha))^2} = 1 - 1 = 0
\end{split}
$$
También sabemos que $g''(\alpha)$ estará definida ya que como el denominador de la función $g$ original existe, el denominador de $g''(x)$, $(1 - 0.5 \cos(x))^4$, también.

3. Calcular las primeras 3 iteraciones del método de iteración de punto fijo para la función $g(x)$ y sus errores. Comentar los resultados obtenidos. *Nota: utiliza la aproximación obtenida con `scipy.optimize.bisect` como verdadero valor de la raíz*

## Problema 2: Iteración de punto fijo II

Dada la ecuación $\frac{x^{5}}{10} + x - 1 = 0.$

1. Demuestre que tiene una única solución $\epsilon$ tal que $0 < \epsilon < 1$.

Por el [[1716715022-teorema-de-bolzano|teorema de Bolzano]], como $f$ es [[1716491727-funcin-continua|continua]] en $[0,1]$ y $f(0) = -1$ y $f(1)=1$, entonces existe $\epsilon \in (0,1)$ tal que $f(\epsilon)=0$.

Para demostrar la unicidad, supongamos por reducción al absurdo que existen dos soluciones $\epsilon_1, \; \epsilon_2 \in (0,1)$ tal que $f(\epsilon_1) = 0$ y $f(\epsilon_2) = 0$. Por el [[1716744725-teorema-de-rolle|teorema de Rolle]] como $f(\epsilon_1) = f(\epsilon_2)$ entonces existe $c \in (0,1)$ tal que $g'(c) = 0$. Pero no existe ningún valor $c \in \mathbb{R}$ para el que $f'(c) = 0$:

$$
f'(x) = \frac{x^4}{2} + 1 \ge 1 \quad\forall x \in \mathbb{R}
$$
2. Plantea una iteración de punto fijo (distinta de la de Newton) para obtener $\epsilon$ aproximadamente y demuestre que tal iteración converge cuando se parte de una estimación inicial suficientemente buena.

Construyamos nuestra función de [[1716491727-punto-fijo|punto fijo]]:

$$
\begin{split}
	& f(\epsilon) = \frac{\epsilon^5}{10} + \epsilon - 1 = 0\\
	& g(\epsilon) = 1 - \frac{\epsilon^5}{10} = \epsilon\\
	& g'(x) = -\frac{x^4}{2}
\end{split}
$$
Como $g$ está definida y tiene derivada [[1716491727-funcin-continua|continua]] en todo $[0,1]$ y además $g(\epsilon) = \epsilon$. Como $|g'(\epsilon)| < \frac{1}{2} < 1$ para todo $\epsilon \in (0,1)$, por el [[1715081050-atraccin-local-en-la-iteracin-de-punto-fijo|teorema de atracción local]], sabemos que la sucesión $x_{n+1}=g(x_n)$ convergerá si se parte de un $x_0$ suficientemente cercano a $\epsilon$.
