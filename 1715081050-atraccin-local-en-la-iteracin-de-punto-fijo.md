---
id: 1715081050-atraccin-local-en-la-iteracin-de-punto-fijo
aliases:
  - Atracción local en la iteración de punto fijo
  - Atracción local
  - Teorema de atracción local
tags:
  - cálculo-numérico
---

# Atracción local en la [[1715077058-iteracin-de-punto-fijo|iteración de punto fijo]]

Supongamos que tenemos una función $g$ que tiene como [[1716491727-punto-fijo|punto fijo]] la raíz (cero) de $f$ que buscamos

$$
\begin{split}
	& f(\alpha) = 0\\
	& g(\alpha) = \alpha
\end{split}
$$

El siguiente teorema proporciona una condición suficiente para que la sucesión de iterantes converja hacia $\alpha$

## Teorema

Sea $g$ una función definida y con derivada [[1716491727-funcin-continua|continua]] en un intervalo de la forma $(\alpha - r_{0}, \alpha + r_{0}), \quad r > 0$, con $g(\alpha)=\alpha$

Si $|g'(\alpha)|<1$ entonces existe $0 < r < r_{0}$ tal que para $x_{0} \in  [\alpha - r, \alpha + r]$, se puede construir la sucesión $x_{n+1}=g(x_{n}), \quad n=0,1,\ldots ,$ con elementos en $[\alpha -r,\alpha +r]$ y es convergente hacia $\alpha$. Además si los errores $e_{n}=x_{n}-\alpha$ son no nulos, entonces los cocientes $\frac{e_{n+1}}{e_{n}}\to g'(\alpha), \quad n \to \infty$

#### Notas

- Si un error $e_{n}$ es $0$, entonces $x_{n}=\alpha$ y $x_{k}=\alpha \forall k\ge n$
- El teorema garantiza la construcción de la sucesión de iterantes.
- El teorema es local: garantiza que para $x_{0}$ suficientemente próximos a $\alpha$ la iteración de [[1716491727-punto-fijo|punto fijo]] tiene éxito.

## Demostración

Como $|g'(\alpha )|<1$, podemos tomar un $M$ con $|g'(\alpha )|<M<1$
Por la continuidad de $g'$, existe $r < r_{0}$ tal que para $x\in [\alpha -r,\alpha +r]$ se tiene $|g'(x)|<M$

Sea $x_{0}\in [\alpha -r, \alpha +r]$ y supongamos que ya hemos calculado $x_{1},\ldots ,x_{n}$ y que están en $[\alpha -r,\alpha +r]$ y que están en $[alpha-r,alpha+r]$. Entonces $x_{n+1}=g(x_n)$ y puesto que $g(\alpha )=\alpha$ entonces $x_{n+1}-\alpha = g(x_{n})- \alpha  = g(x_{n})-g(\alpha )$ (usando el [[1715082816-teorema-del-valor-medio-de-lagrange|teorema del valor medio de Lagrange]])

$$
\begin{split}
    & x_{n+1} - \alpha = g(x_{n}) - g(\alpha ) ) g'(\beta_{n})(x_{n}-\alpha ), \quad \beta_{n} \text{ entre } x_{n} \text{ y } \alpha\\
\end{split}
$$

Luego $\beta_{n} \in [\alpha -r,\alpha +r]$.

Tomando valores absolutos tenemos que $|x_{n+1} - \alpha| = |g'(\beta_{n})| |x_{n}-\alpha| \le M |x_{n}-\alpha| < |x_{n} - \alpha| \le r$.
Por tanto $x_{n+1}\in [\alpha -r,\alpha +r]$. Por inducción concluimos que todos los $x_{i} \in [\alpha -r,\alpha +r], \quad \forall i=0,1,\ldots$

Acabamos que ver que $|e_{n+1}| = |x_{n+1}|\le M|e_{n}|$ para cada $n$, luego $|e_{n}|\le M|e_{n-1}| \le M(M|e_{n-1}|) \le \ldots \le M^{n}|e_{0} \to 0$ cuando $n \to \infty$ y $x_{n} \to  \alpha$ cuando $n \to \infty$.

Si $e_{n}\neq 0$ y $e_{n+1}\neq 0$ entonces $\frac{e_{n+1}}{e_{n}} = \frac{x_{n+1}-\alpha}{x_{n}-\alpha} = \frac{g(x_n)-g(\alpha)}{x_{n}-\alpha} \to  g'(\alpha)$ cuando $n\to \infty$ y $x_{n} \to \alpha$ (demostrado anteriormente).

## Conclusiones

- El teorema de atracción local nos dice que $g'(\alpha )$ gobierna la rapidez de iteración de punto fijo
- El caso más favorable será $g'(\alpha ) = 0$, pues entonces $\frac{e_n + 1}{e_n} \to 0$ cuando $n\to \infty$, es decir, $e_{n+1} = o(e_{n})$ ($e_{n+1}$ es una [[1713169805-notaciones-de-landau|o pequeña]] de $e_{n}$)

