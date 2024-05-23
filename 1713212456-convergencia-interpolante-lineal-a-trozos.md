---
id: 1713212456-convergencia-interpolante-lineal-a-trozos
aliases:
  - Convergencia interpolante lineal a trozos
tags:
  - cálculo-numérico
---

# Convergencia interpolante lineal a trozos

Consideramos en $[a,b]$ una sucesión $\Delta_{0}, \Delta_{1}, \Delta_{2},\ldots$ de particiones con diámetros $h_{0},h_{1},h_{2},\ldots$ que tienden a cero.

Dada una función $f_i$ podemos considerar la sucesión de funciones interpolantes a trozos $s_{0},s_{1},s_{2},\ldots$ Si $f$ tiene segunda derivada y existe la cota $K_{2}$ tal que $|f''(x)|\leq K_{2}$ para todo $x\in [a,b]$, entonces se tiene que

$$
|f(x)-s_{n}(x)|\leq \frac{K_{2}}{8}h_{N}^{2}
$$

Luego si $N \to \infty$ entonces $s_N(x) \to f(x)$ uniformemente en $[a,b]$. Esto ocurre ya que cuanto mayor sea $N$, menor será el diámetro de la partición y por lo tanto menor será el error de interpolación.

La convergencia es cuadrática: Si reducimos el diámetro de la partición a la mitad, la cota del error de interpolación se divide por cuatro.

