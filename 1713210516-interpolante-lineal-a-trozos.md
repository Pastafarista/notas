---
id: 1713210516-interpolante-lineal-a-trozos
aliases:
  - Interpolante lineal a trozos
tags:
  - cálculo-numérico
---

# Interpolante lineal a trozos

Dada un intervalo $[a,b]$ y una partición $\Delta$ del mismo:

$$
\Delta : a = x_{0} < x_{1} < \ldots < x_{N} = b
$$

y dados los valores de una función $f$ en los nodos de la partición ${f(x_{0}), \ldots, f(x_{N})}$, existe una única función lineal a trozos $S \in M^{1}_{0}(\Delta)$ tal que:

$$
S(x_{0}) = f(x_{0}), \ldots, S(x_{N}) = f(x_{N})
$$

Esta función $S(x)$ se llama *interpolante lineal a trozos* de $f$ en $\Delta$

- $M^{1}_{0}(\Delta)$ es el conjunto de todas las funciones $s$ [[1716491727-funcin-continua|continuas]] en $[a,b]$ que restringidas a cada intervalo $[x_{i-1}, x_{i}]$ coinciden con un polinomio de grado $\le 1$ (es decir, es lineal).