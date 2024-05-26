---
id: 1713865555-reglas-de-cuadratura
aliases:
  - Reglas de cuadratura
  - Regla de cuadratura
tags:
  - cálculo-numérico
---

# Reglas de cuadratura

Combinación lineal de valores de la función $f$ en $N+1$ puntos $x_{0}, x_{1}, \ldots, x_{N}$.

$$
\begin{split}
    & \mathcal{I}_{N+1}(f) = \alpha_{0}f(x_{0}) + \alpha_{1}f(x_{1}) + \ldots + \alpha_{N}f(x_{N})\\
    & \text{Fijados } x_i, \alpha_i \; \forall i=0,\ldots,N \quad I_{N+1}(f) \in \mathbb{R}\\
\end{split}
$$

- Los puntos $x_{0}, x_{1}, \ldots, x_{N}$ son los nodos de cuadratura.
- $\alpha_i$ se llaman pesos o coeficientes.
- En general si $x_i \in [a,b]$, entonces $x_i \neq x_j$ si $i\neq j$

### Reglas:

- [[1713865627-regla-de-los-rectngulos|Regla de los rectángulos]]
- [[1713865721-regla-del-punto-medio|Regla del punto medio]]
- [[1713865822-regla-del-trapecio|Regla del trapecio]]
- [[1713865832-regla-de-simpson|Regla de Simpson]]
- [[1713873299-mtodo-interpolatorio|Regla interpolatoria]]
- [[1713875089-mtodo-de-coeficientes-indeterminados-reglas-cuadratura|Regla coeficientes indeterminados]]
- [[1716663320-mtodo-del-desarrollo-de-taylor|Regla de desarrollo de Taylor]]
