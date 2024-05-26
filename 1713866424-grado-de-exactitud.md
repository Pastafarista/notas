---
id: 1713866424-grado-de-exactitud
aliases:
  - Grado de exactitud
tags:
  - cálculo-numérico
---

# Grado de exactitud

Una [[1713865555-reglas-de-cuadratura|regla de cuadratura]] tiene un grado de exactitud $M \ge 0$ si calcula de forma exacta la integral de todo polinomio de grado $\le M$ y exista un polinomio $f$ de grado $M + 1$ tal que $\mathcal{I}(f) \neq \mathcal{I}(f)$

$$
\begin{split}
    & \mathcal{I}_{N+1}(f) = \mathcal{I}(f) \quad \forall f \text{ polinomio de grado } \le M\\
    & \exists f \text{ de grado } M + 1 \text{ dal que } \mathcal{I}_{N+1}(f) \neq \mathcal{I}(f)
\end{split}
$$

### Ejemplos

- [[1713866465-grado-de-exactitud-para-la-regla-de-los-rectngulos|Grado de exactitud para la regla de los rectángulos]] 
- [[1713866869-grado-de-exactitud-para-la-regla-del-punto-medio#grado-de-exactitud-para-la-regla-del-punto-medio|Grado de exactitud para la regla del punto medio]]
- [[1716660069-grado-de-exactitud-para-la-regla-del-trapecio|Grado de exactitud para la regla del trapecio]]
- La [[1713865832-regla-de-simpson|regla de Simpson]] tiene grado de exactitud $M=3$