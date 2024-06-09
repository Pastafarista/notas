---
id: 1708330960-ecuacin-diferencial-homognea
aliases:
  - Ecuación diferencial homogénea
  - ecuación homogénea
  - Ecuación homogénea
tags:
  - ecuaciones-diferenciales
---

# Ecuación diferencial homogénea

- Una función $f(x_1,x_2,\cdots, x_n)$ es **homogénea** de [[1707050060-grado-ecuacin-diferencial|grado]] $k$ si
$${f(\lambda x_1, \lambda x_2, \cdots, \lambda x_n) = \lambda^k f(x_1,x_2,\cdots,x_n)}$$

- Una [[1708330318-ecuacin-diferencial-ordinaria-de-primer-orden|ecuación diferencial de primer orden]] escrita en forma diferencial, ${M(x,y)dx + N(x,y)dy = 0}$, es **homogénea** si ${M(x,y)}$ y ${N(x,y)}$ son funciones homogéneas de igual [[1707050060-grado-ecuacin-diferencial|grado]]

- Una ecuación diferencial de primer orden es **homogénea** si se puede escribir como $y' = f(x,y)$, donde $f(x,y)$ es una función homogénea de grado cero, es decir, $f(\lambda x, \lambda y) = f(x,y)$

## Resolución

La forma de resolver estas ecuaciones consiste en **realizar el cambio $y=xu$**, en cuyo caso la ecuación se transformará en una [[1708330652-eucacin-diferencial-de-variable-separada|ecuación de variable separada]], siendo esas variables $x$ y $u$

Una vez obtenida la [[1707058998-solucin-de-una-ecuacin-diferencial-ordinaria|solución general]], es necesario deshacer el cambio mediante la igualdad $u = \frac{x}{y}$

## Ejemplo

La función ${f(x,y) = (x^2 + y^2 - xy)}$ es **homogénea** de grado 2, ya que podemos escribir ${f(\lambda x, \lambda y) = (\lambda x)^2 + (\lambda y)^2 - (\lambda x)(\lambda y) = \lambda^2(x^2 + y^2 - xy)}$
