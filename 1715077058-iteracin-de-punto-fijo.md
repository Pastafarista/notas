---
id: 1715077058-iteracin-de-punto-fijo
aliases:
  - Iteración de punto fijo
  - Método para las aproximaciones sucesivas
tags:
  - cálculo-numérico
---

# Iteración de [[1716491727-punto-fijo|punto fijo]]

$x^{*}$ es raíz de $f$
$g(x) = x + f(x)$
$g(x^{*}) = x^{*} + f(x^{*}) = x^{*} + 0 = x^{*}$
$x^{*}$ es un [[1716491727-punto-fijo|punto fijo]] de $g$

$$
\begin{split}
    & f(x) = x - 0.007 \sin(x) - 0.7 = 0\\
    & x_{0} & = 0.7 \text{ (aproximación)}\\
    & x^{*} \approx 0.7 \\
    & 0.007 \sin (0.7) = 0.004510\\
    & x_{1} = 0.7 + 0.004510 = 0.704510\\
    & x^{*} \approx 0.704510\\
    & 0.007 \sin (0.704510) = 0.004534\\
    & x_{2} = 0.7 + 0.004534 = 0.704534
\end{split}
$$

Si $x^{*}$ es raíz de $f(x)$, entonces $x^{*}$ es punto fijo de $g(x) = 0.7 + 0.007\sin(x)$

La filosofía de la iteración de punto dijo es generar aproximaciones sucesivas $x_{1},x_{2},\ldots ,x_{n}$ a la raíz buscada $\alpha$ esperando acercarnos cada vez más a ella. 

$$
\begin{split}
    & \text{Buscamos que:}\\
    & n \to \infty \implies x_{n} \to \alpha
\end{split}
$$

Si ocurre, entonces dada una tolerancia existe un valor $N$ tal que $x_N,x_{N+1}\ldots$ distan de $\alpha$ menos que la tolerancia.

. Cada aproximación $x_{n+1} \quad n=0,\ldots$ se obtiene como una función de $x_{n}, x_{n+1}=g(x_n)$. $g$ se denomina función de iteración. ¡Ojo! $f\neq g$ (en general)

¿Como seleccionamos $g$?

- Si $x_n \implies \infty$ cuando $n \to \infty$ y $g$ [[1716491727-funcin-continua|continua]], tomando límites en $x_{n+1}=g(x_n)$

$$
\alpha = \lim_{n \to \infty} x^{n+1} = \lim_{n \to \infty} g(x_n) = g(\lim_{n \to \infty} x_n) = g(\alpha)
$$

Es condición necesaria para que la iteración de punto fijo tenga éxito que $\alpha$ sea un punto fijo de $g$.
