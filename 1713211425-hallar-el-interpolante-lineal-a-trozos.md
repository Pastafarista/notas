---
id: 1713211425-hallar-el-interpolante-lineal-a-trozos
aliases:
  - Hallar el interpolante lineal a trozos
tags:
  - cálculo-numérico
---

# Hallar el interpolante lineal a trozos

Para hallar el [[1713210516-interpolante-lineal-a-trozos|interpolante lineal a trozos]] de $f$ en $\Delta$, hemos de encontrar para cada $i = 1,\ldots, N$ los dos coeficientes reales $\alpha_{i}$ y $\beta_{i}$ tales que:

$$
S(x) = \alpha_{i} + \beta_{i}(x - x_{i-1}) \quad \text{para } x \in [x_{i-1}, x_{i}]
$$

Para calcular $\alpha$ nos fijaos en que $S(x_{i-1}) = f(x_{i-1})$ y $S(x_{i}) = f(x_{i - 1})$. Sustituyendo en la ecuación anterior, obtenemos:

$$
\begin{split}
    & s(x_{i-1}) = \alpha_{i} + \beta_{i}(x_{i-1} - x_{i-1}) = \alpha_{i} = f(x_{i-1})\\
\end{split}
$$

Para calcular $\beta_{i}$ nos fijamos en $s(x_i)$:

$$
\begin{split}
    & s(x_{i}) = \alpha_{i} + \beta_{i}(x_{i} - x_{i-1}) = f(x_{i})\\
    & \beta_{i} = \frac{f(x_{i}) - f(x_{i-1})}{x_{i} - x_{i-1}}\\
    & \beta_{i} = f[x_{i-1}, x_{i}]
\end{split}
$$
