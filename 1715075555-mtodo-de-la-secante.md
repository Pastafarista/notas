---
id: 1715075555-mtodo-de-la-secante
aliases:
  - Método de la secante
tags:
  - cálculo-numérico
---

# Método de la secante

Partimos de dos aproximaciones $x_0$ y $x_{1}$ a la raíz $\alpha$ $(f(\alpha )=0)$

Sea $P_{1}(x)$ la [[1709641715-polinomio-interpolador-de-lagrange|recta interpolante]] a $f$ en $x_{0}$ y $x_{1}$, resuelvo $P_{1}(x)=0$ y denoto por $x_{2}$ a la raíz.

$$
\begin{split}
    & \begin{cases}
        \text{Si } P_{1} \equiv f \text{ entonces } x_{2}=\alpha \\
        \text{Si el error de interpolación es pequeño, esperamos que } x_2 \text{ sea una mejor aproximación a } x_{0} \text{ y } x_{1}
    \end{cases}\\
    & x_{n+2} \text{ es la raíz de la recta que interpola a } x_n \text{ y } x_{n+1} \text{, tenemos que } \\
    & f(x_{n+1}) + f[x_{n+1},x_{n}](x_{n+2}-x_{n+1}) = 0\\
    & x_{n+2} = x_{n+1} - \frac{f(x_{n+1})}{f[x_{n+1},x_{n}]} \quad n=0,1,2,\ldots
\end{split}
$$
 
El cálculo no siempre es posible:

- Cuando $f[x_{n+1},x_{n}] = 0$, pero cuando eso ocurre significa que se trata de una recta horizontal. Por lo tanto, si es constante cero $x_{n+1}$ era una raíz, o si no, no corta el eje de abscisas.
- Cuando $f(x_{n+1})$ no está definido.

## Comparación con el [[1715073673-mtodo-de-la-biseccin|método de la bisección]]

| Bisección   | Secante    |
|--------------- | --------------- |
| Funciona siempre   | No siempre genera aproximaciones   |
| Da cotas superiores e inferiores para la raíz buscada   | No siempre da cotas   |
| Lento   | Más rápido que bisección (si converge)   |
| `scipy.optimize.bisect`   | `scipy.optimize.newton` con `fprime=None`   |

