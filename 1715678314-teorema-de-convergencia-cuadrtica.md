---
id: 1715678314-teorema-de-convergencia-cuadrtica
aliases:
  - Teorema de convergencia cuadrática
tags:
  - cálculo-numérico
---

# Teorema de convergencia cuadrática

Sea $g$ una función definida 

Sea $g$ una función definida y con derivada [[1716491727-funcin-continua|continua]] en un intervalo de la forma $(\alpha - r_{0}, \alpha + r_{0}), \quad r > 0$, con $g(\alpha)=\alpha$

Si $g'(\alpha) = 0$ y existe $g''(\alpha)$ entonces existe $0 < r < r_{0}$ tal que para $x_{0} \in  [\alpha - r, \alpha + r]$, se puede construir la sucesión $x_{n+1}=g(x_{n}), \quad n=0,1,\ldots ,$ con elementos en $[\alpha -r,\alpha +r]$ y es convergente hacia $\alpha$. Además si los errores $e_{n}=x_{n}-\alpha$ son no nulos, entonces los cocientes $\frac{e_{n+1}}{e_{n}^2}\to \frac{1}{2}g''(\alpha), \quad n \to \infty$

## Demostración

La construcción de los iterantes y la convergencia son consecuencia del [[1715081050-atraccin-local-en-la-iteracin-de-punto-fijo|teorema de atracción local]] que se puede aplicar pues las hipótesis se cumplen ya que si $g'(\alpha) = 0$ entonces $|g'(\alpha)|<1$

Falta probar que $\frac{e_{n+1}}{e_{n}^2} \to \frac{1}{2}g'(\alpha )$ si $n\to \infty$.

Usando el polinomio de Taylor de segundo grado de $g$ en torno a $\alpha$ para aproximar $g(x_{n})$

$$
\begin{split}
    & e_{n+1} = x_{n+1} - \alpha = g(x_{n}) - g(\alpha ) =\\
    & = [g(\alpha ) + g'(\alpha )(x_{n} - \alpha ) + \frac{g''(\alpha}{2})(x_{n} - \alpha )^2 + o(x_{n}-\alpha)^2] - g(\alpha) =\\
    & = g'(\alpha)(x_{n} - \alpha) + \frac{1}{2}g''(\alpha)(x_{n} - \alpha)^2 + o(x_{n}-\alpha)^2
\end{split}
$$

donde utilizamos la [[1709029256-caracterizacin-analtica-del-polinomio-de-taylor|caracterización analítica del polinomio de Taylor]] para escribir como $o((x_{n}-\alpha )^2)$ la diferencia entre $g(x_{n})$ y el polinomio de Taylor de segundo grado.

Pero, por hipótesis, $g'(\alpha ) = 0$ luego $e_{n+1} = \frac{1}{2}g''(\alpha )(x_{n}-\alpha )^2 + o((x_{n}- \alpha )^2)$

Dividiendo entre $e_{n}^2 = (x_{n} - \alpha )^2$ (recordemos que estamos suponiendo errores no nulos)

$$
\begin{split}
    & \frac{e_{n} + 1}{e_{n}^2} = \frac{1}{2}g''(\alpha) + \frac{0((x_{n} - \alpha )^2)}{e_{n}^2} \implies\\
    & \lim_{n\to \infty} \frac{e_{n+1}}{e_{n}^2} = \frac{1}{2}g''(\alpha) + 0 = \frac{1}{2}g''(\alpha)
\end{split}
$$

Pues $\frac{o(e_{n}^2)}{e_n^2}$ tiende a $0$ cuando $n\to \infty$ por definición de [[1713169805-notaciones-de-landau|o pequeña]].

La convergencia que tenemos en este caso se llama cuadrática (error asintóticamente proporcional al cuadrado del precedente).
Por lo tanto, está convergencia es mucho más rápido que la convergencia lineal del [[1715081050-atraccin-local-en-la-iteracin-de-punto-fijo#notas|teorema de atracción local]] (cuando la derivada de nuestra raíz es cero y exista su segunda derivada, la convergencia va a ser más rápida)



