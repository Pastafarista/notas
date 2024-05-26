---
id: 1713875089-mtodo-de-coeficientes-indeterminados-reglas-cuadratura
aliases:
  - Método de coeficientes indeterminados reglas cuadratura
  - Método de coeficientes indeterminados
tags:
  - cálculo-numérico
---

# Método de coeficientes indeterminados

La idea es que $\mathcal{I}_{N+1}(f)$ tiene [[1713866424-grado-de-exactitud|grado de exactitud]] $\ge k \iff \mathcal{I}_{N+1}(f) = \mathcal{I}(f)$ para $f(x) = 1, x, x^2, \ldots , x^{k}$

Con el siguiente sistema podemos calcular los pesos $\alpha_i$ de la [[1713865555-reglas-de-cuadratura|regla de cuadratura]]:

$$
\begin{split}
    & \mathcal{I}_{N+1}(1) = \mathcal{I}(1) \coloneqq \alpha_{0} + \alpha_{1} + \ldots + \alpha_{N} = \int_{a}^{b} 1 dx = b - a\\
    & \mathcal{I}_{N+1}(x) = \mathcal{I}(x) \coloneqq \alpha_{0}x_{0} + \alpha_{1}x_{1} + \ldots + \alpha_{N}x_{N} = \int_{a}^{b} x dx = \frac{b^2 - a^2}{2}\\
    & \mathcal{I}_{N+1}(x^2) = \mathcal{I}(x^2) \coloneqq \alpha_{0}x_{0}^2 + \alpha_{1}x_{1}^2 + \ldots + \alpha_{N}x_{N}^2 = \int_{a}^{b} x^2 dx = \frac{b^3 - a^3}{3}\\
    & \vdots\\
    & \mathcal{I}_{N+1}(x^{k}) = \mathcal{I}(x^{k}) \coloneqq \alpha_{0}x_{0}^{k} + \alpha_{1}x_{1}^{k} + \ldots + \alpha_{N}x_{N}^{k} = \int_{a}^{b} x^{k} dx = \frac{b^{k+1} - a^{k+1}}{k+1}
\end{split}
$$

Tenemos un sistema de $K+1$ ecuaciones con $N+1$ incógnitas (pesos $\alpha_i$). Si $k=N$ entonces tenemos tantas ecuaciones como incógnitas.

La matriz del sistema es la matriz de Vandermonde, por lo tanto si $k=N$ entonces el sistema tiene solución única.
