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
2. Demostrar la convergencia cuadrática del método de iteración de punto fijo para la función $g(x)$.
3. Calcular las primeras 3 iteraciones del método de iteración de punto fijo para la función $g(x)$ y sus errores. Comentar los resultados obtenidos. *Nota: utiliza la aproximación obtenida con `scipy.optimize.bisect` como verdadero valor de la raíz*

## Problema 2: Iteración de punto fijo II

Dada la ecuación $\frac{x^{5}}{10} + x - 1 = 0.$

1. demuestre que tiene una única solución $\epsilon$ tal que $0 < \epsilon < 1$.
2. Plantea una iteración de punto fijo (distinta de la de Newton) para obtener $\epsilon$ aproximadamente y demuestre que tal iteración converge cuando se parte de una estimación inicial suficientemente buena.
