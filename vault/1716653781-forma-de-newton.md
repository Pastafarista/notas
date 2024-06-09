---
id: 1716653781-forma-de-newton
aliases:
  - Forma de Newton
tags:
  - cálculo-numérico
---

# Forma de Newton

En la forma de Newton, el [polinomio interpolador](1709641715-polinomio-interpolador-de-lagrange) tiene la siguiente forma:

$$
P(x) = f[x_{0}] + f[fx_{0},x_{1}](x-x_{0}) + \ldots + f[x_{0},x_{1},\ldots,x_N](x-x_{0})(x-x_{1})\dots(x-x_{N-1})
$$

Los términos $f[x_{0},x_{1},\ldots,x_i]$ son las [[1716653895-diferencia-dividida|diferencias divididas]]

