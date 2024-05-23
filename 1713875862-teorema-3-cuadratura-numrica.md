---
id: 1713875862-teorema-3-cuadratura-numrica
aliases:
  - Teorema 3 cuadratura numérica
tags:
  - cálculo-numérico
---

# Teorema

Dados $N\ge 0$ y $N+1$ nodos $x_i$ distintos dos a dos, entonces hay una única elección de pesos $\alpha_i$ para los que $\mathcal{I}_{N+1}(f) = \alpha_{0}f(x_{0}) + \alpha_{1}f(x_{1}) + \ldots + \alpha_{N}f(x_{N})$ tenga grado $\ge N$

Nota: los pesos se obtienen resolviendo el [[1713875089-mtodo-de-coeficientes-indeterminados-reglas-cuadratura|sistema anterior]].

### Colorario

Entonces como el sistema anterior tenía solución única, la [[1713865555-reglas-de-cuadratura|regla de cuadratura]] [[1713873299-mtodo-interpolatorio|interpolatoria]] es la única con esos nodos que tiene grado de exactitud $\ge N$. Los pesos $\alpha_i$ pueden calcularse con el [[1713875089-mtodo-de-coeficientes-indeterminados-reglas-cuadratura|sistema anterior]] o con la fórmula $\alpha_i = \int_{a}^{b}l_i(x)dx \quad i=0,\ldots,N$
