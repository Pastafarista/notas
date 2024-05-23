---
id: 1715679859-teorema-de-puntos-fijos-repulsores
aliases:
  - Teorema de puntos fijos repulsores
tags:
  - cálculo-numérico
---

# Teorema de puntos fijos repulsores

La condición $|g'(\alpha)|<1$ que garantica la [[1715081050-atraccin-local-en-la-iteracin-de-punto-fijo|atracción local]] al [[1716491727-punto-fijo|punto fijo]] es (casi) necesaria.

## Enunciado

Sea $g$ una función definida y con derivada [[1716491727-funcin-continua|continua]] en un conjunto que contenga un intervalo de la forma $(\alpha - r_{0}, \alpha + r_{0}), \quad r > 0$, con $g(\alpha)=\alpha$.

Si $|g'(\alpha)| > 1$, las únicas sucesiones de la forma $x_{n+1} = g(x_{n}) \quad n=0,1,\ldots$ que convergen a $\alpha$ son aquellas cuyos términos son, de uno en adelante, iguales a $\alpha$. 

## Demostración

Como $|g'(\alpha)| > 1$, existe $M$ tal que $|g'(\alpha)| > M > 1$.

Por la [[1716491727-funcin-continua|continuidad]] de $g'$, existe $r < r_{0}$, tal que para $x\in [\alpha -r,\alpha +r]$ se tiene $|g'(x)| \ge  M$.

Supongamos que tenemos una sucesión $x_{n+1} = g(x_{n}) \quad n=0,1,\ldots$ que converge a $\alpha$. Entonces existe $n_{1}$ tal que para todo $n\ge n_{1}$, $x_{n}\in [\alpha - r, \alpha +r]$.

Suponemos por reducción al absurdo que existe $n_{2}$ tal que para todo $n\ge n_{2}, \; x_n \neq \alpha$.

Sea $n_{0}=\max(n_{1},n_{2})$, para todo $n\ge n_{0}$ se tiene que $x_{n} \in [\alpha - r, \alpha + r]$ y $x_{n} \neq \alpha$.

Como $x_{n}-\alpha = g(x_{n}) - g(\alpha)$ por el [[1715082816-teorema-del-valor-medio-de-lagrange|teorema del valor medio de Lagrange]], existe $\beta_{n} \in (x_{n}, \alpha)$ tal que $x_{n+1}-\alpha = g'(\beta_{n})(x_{n}-\alpha)$

Por tanto para $n\ge n_{0}$, $\beta_n \in (x_n,\alpha) \subset [x-r,x+r]$ y
$$
|x_{n+1}-\alpha| = |g'(\beta_{n})||x_{n}-\alpha| = |g'(\beta)| |x_{n}-\alpha | \ge  M |x_{n} - \alpha |
$$

luego
$$|x_n-\alpha | \ge M|x_{n-1}-\alpha | \ge M^2|x_{n-2}-\alpha | \ge \ldots \ge M^{n-n_{0}}|x_{n_0} - \alpha|$$

pero
$$
M^{n-n_{0}}|x_{n_0} - \alpha| \to \infty \text{ cuando } n\to \infty 
$$
Lo que contradice la convergencia a $\alpha$ de la sucesión $x_{n}$. Por tanto, no existe $n_{2}$ tal que $\forall n\ge n_{2} \;\; x_{n}\neq \alpha$. Es decir, de un término en adelante $x_{n} = \alpha$.

