---
id: 1714468484-laboratorio-7-clculo-numrico
aliases:
  - Laboratorio 7 cálculo numérico
tags:
  - cálculo-numérico
---

# Laboratorio 7 cálculo numérico

1. Utilizando el [[1713873299-mtodo-interpolatorio|método interpolatorio]]. Escriba la recta interpolatoria de lagrande en forma de newton e intégrela ¿Cuál es el grado de exactitud de la regla?

Sabemos que la forma de Newton del polinomio interpolatorio de Lagrange en los nodos $x_0, x_1, \ldots, x_n$ es:

$$
P(x) = f[x_{0}] + f[x_{0}, x_{1}](x - x_{0}) + f[x_{0}, x_{1}, x_{2}](x - x_{0})(x - x_{1}) + \ldots + f[x_{0}, x_{1}, \ldots, x_{n}](x - x_{0})(x - x_{1})\ldots(x - x_{n-1})
$$

Entonces, si integramos el polinomio:

$$
\begin{split}
    & \int_{a}^{b} P(x) =\\
    & =\int_{a}^{b} f[x_{0}] + f[x_{0}, x_{1}](x - x_{0}) + \ldots + f[x_{0}, \ldots, x_{n}](x - x_{0})\ldots(x - x_{n-1}) =\\
    & = \int_{a}^{b} f[x_{0}] + \int_{a}^{b} f[x_{0}, x_{1}](x - x_{0}) + \ldots + \int_{a}^{b} f[x_{0}, x_{1}, \ldots, x_{n}](x - x_{0})\ldots(x - x_{n-1}) =\\
    
\end{split}
$$

2. Utilizando el [[1713873299-mtodo-interpolatorio|método interpolatorio]]. Calcule los pesos $\lambda_{i}$ utilizando los polinomios de la base de Lagrange. ¿Cuál es el grado de exactitud de la [[1713865555-reglas-de-cuadratura|regla]]?

$$
\begin{split}
    & [a,b] \quad N=1 \quad x_{0}=a, x_{1}=b; \quad x_{0}\neq x_{1}\\
    & I_{N+1}(f) = \lambda_{0}f(x_{0}) + \ldots + \lambda_{n}f(x_{n})
\end{split}
$$
