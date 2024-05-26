---
id: 1713873299-mtodo-interpolatorio
aliases:
  - Método interpolatorio
tags:
  - cálculo-numérico
---

# Método interpolatorio

La idea será sustituir el integrando $f$ por el [[1709641715-polinomio-interpolador-de-lagrange|polinomio interpolador de Lagrange]] de grado $\le N$ que coincide con $f$ en los $N+1$ nodos de cuadratura $x_i$.

$$
\begin{split}
    & \mathcal{I}_{N+1}(f) = \mathcal{I}(P) = \int_{a}^{b} P(x) dx =\\
    & = \int_{a}^{b} \left(\sum_{i=0}^{N} f(x_i) \cdot l_i(x)\right) dx = \sum_{i=0}^{N} f(x_i) \cdot \int_{a}^{b} l_i(x) dx
\end{split}
$$

Entonces los pesos $\alpha_i$ serán:

$$
\alpha_i = \int_{a}^{b} l_i(x) dx
$$

Decimos que el método interpolatorio da como resultado la regla interpolatoria ([[1713865555-reglas-de-cuadratura|regla de cuadratura]]) correspondiente a los nodos $x_i$.

La regla interpolatoria de $N+1$ nodos tendrá [[1713866424-grado-de-exactitud|grado de exactitud]] mayor o igual a $N$