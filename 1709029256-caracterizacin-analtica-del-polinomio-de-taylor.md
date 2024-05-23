---
id: 1709029256-caracterizacin-analtica-del-polinomio-de-taylor
aliases:
  - Caracterización analítica del polinomio de Taylor
tags:
  - cálculo-numérico
---

# Caracterización analítica del polinomio de Taylor

$$\begin{split}
    & b_0(x) = 1, \; b_1(x) = (x - x_0), \; b_2(x) = \frac{(x-x_0)^2}{2!}, \; \ldots, \; b_n(x) = \frac{(x-x_0)^n}{n!}\\
    & \lim_{x \rightarrow x_0} \frac{\frac{(x - x_0)^2}{2!}}{(x - x_0)} = 0 \;\;\;\;\; \frac{(x - x_0)^2}{2!} = o(x - x_0)\\
    & \lim_{x \rightarrow x_0} \frac{(x - x_0)^2}{1} = 0 \;\;\;\;\; \frac{(x - x_0)^2}{1} = o(1)\\
    & \lim_{x \rightarrow x_0} b_i(x) = 0 (b_j(x)) \;\; \forall j < i\\
\end{split}$$

## Teorema de Taylor o Fórmula infinitesimal del resto

Para $n \geq 1$, sea $f$ una función para la que el problema de Taylor se pueda proponer, es decir, que $f$ sea $n$ veces derivable en $x_0$, el polinomio de Taylor $P$ verifica:

$$ \lim_{x \rightarrow x_0} f-P= o((x- x_0))^n \;\;\;\;\; (a)$$

Además, $P$ es el único polinomio de grado menor o igual que $n$ con esta propiedad y por ello $(a)$ caracteriza al polinomio de Taylor entre todos los de grado menor o igual que $n$.

## Demostración


Recordatorios:
$$\begin{split}
    & P(x) = f'''(x_0) \frac{(x - x_0)^3}{3!} + f''(x_0) \frac{(x - x_0)^2}{2!} + f'(x_0) (x - x_0) + f(x_0)\\
    & P'(x) = \frac{f'''(x_0)}{3!}3 \cdot(x - x_0)^2 + \frac{f''(x_0)}{2!}2(x - x_0) + f'(x_0)\\
    & P''(x) =  \frac{f'''(x_0)}{3!} \cdot3\cdot2 \cdot(x-x_0)+\frac{f''(x_0)}{2!}2 = f'''(x_0)(x - x_0)+f''(x_0)
\end{split}$$
$$\begin{split}
	& f'(x_0) = \lim_{x \rightarrow 0} \frac{f(x) - f(x_0)}{x - x_0}\\
	& f^{(n)}(x_0) = \frac{f^{(n-1)}(x) - f^{(n-1)}(x_0)}{x - x_0}
\end{split}$$

$$\begin{split}
    & \lim_{x \rightarrow x_0} \frac{f(x) - P(x)}{(x-x_0)^n} = \left\{\frac{0}{0}\right\} =\\
    & = \lim_{x \rightarrow x_0} \frac{f'(x) - P'(x)}{n(x - x_0)^{n-1}} = \cdots = \lim_{x \rightarrow x_0}  \frac{f^{(n-1)}(x) - P^{n-1}(x)}{n!(x-x_0)} =\\
    & = \lim_{x \rightarrow x_0} \frac{f^{(n-1)}(x) - [f^{(n)}(x_0)(x-x_0) + f^{(N-1)}(x_0)]}{n!(x-x_0)} =\\
    & =  \frac{1}{n!} \left[\lim_{x \rightarrow x_0}\frac{f^{(n-1)}(x)-f^{(n-1)}(x_0)}{x-x_0} - \lim_{x \rightarrow x_0} \frac{f^{(n)}(x_0)(x-x_0)}{x - x_0} \right] = \\
    & = \frac{1}{n!} \left[ \lim_{x \rightarrow x_0} \cdots - f^{(n)}(x_0) \right] = \frac{1}{n!} \cdot 0 = 0
\end{split}$$

Ahora demostraremos la unicidad, para ello, queremos ver que si existen dos polinomios $Q_1$ y $Q_2$ de grado menor o igual que $n$ que satisfacen ${\lim_{x \rightarrow x_0}f - Q_1 = o((x-x_0)^n) \;\; i = 1,2}$ entonces $Q_2 = Q_1$, es decir $Q(x) = Q_2(x) - Q_1(x) = 0$

$${Q(x) = Q_2(x) - Q_1(x) = \sum_{i=0}^{n} a_i (x - x_0)^i}$$

debemos probar que $a_i=0 \;\; \forall i = 1, \ldots, n$

Suponiendo, por reducción al absurdo que $Q \neq 0$, existe un $m$ tal que $a_m \neq 0$ y $a_k = 0$ para todo $k < m$, ${m = min\{k \in \{1, \ldots, n\} : a_k \neq 0\}}$
"El coeficiente $a_m$ es el primer coeficiente no nulo de $Q$"

$$\begin{split}
	& lim_{x \rightarrow x_0} \frac{Q(x)}{(x - x_0)^m} = \lim_{x \rightarrow x_0} \frac{\sum_{i=0}^{n}a_i(x - x_0)^i}{(x - x_0)^m} =\\
	& = \lim_{x \rightarrow x_0} \frac{\sum_{i=m}^{n}a_i(x - x_0)^i}{(x-x_0)^m} = \lim_{x \rightarrow x_0} \sum_{i = m}^{n}a_i(x - x_0)^{i - m} = a_m
\end{split}$$

$$\begin{split}
	& \lim_{x \rightarrow x_0} \frac{Q(x)}{(x - x_0)^m} = a_m\\
	& \lim_{x \rightarrow x_0} \frac{Q(x)}{(x - x_0)^n} = \lim_{x \rightarrow x_0} \frac{Q_2(x) - Q_1(x)}{(x-x_0)^n} = \\
	& = \lim_{x \rightarrow x_0} \frac{f(x) - Q_1(x) - f(x) + Q_2(x)}{(x-x_0)^n} = \\
	& = \lim_{x \rightarrow x_0} \frac{f(x) - Q_1(x)}{(x - x_0)^m} - \lim_{x \rightarrow x_0} \frac{f(x) - Q_2(x)}{(x - x_0)^n} = \\
	& = 0 -0 = 0\\
\end{split}$$

Pero ${a_m = \lim_{x \rightarrow x_0} \frac{Q(x)}{(x - x_0)^m} = \lim_{x \rightarrow x_0} \frac{Q(x)}{(x - x_0)^n}(x - x_0)^{n-m} = 0}$ Absurdo!! Q.E.D.