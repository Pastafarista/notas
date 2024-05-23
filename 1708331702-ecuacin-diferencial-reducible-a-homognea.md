---
id: 1708331702-ecuacin-diferencial-reducible-a-homognea
aliases:
  - Ecuación diferencial reducible a homogénea
  - Ecuación reducible a homogénea
tags:
  - ecuaciones-diferenciales
---

# Ecuación diferencial reducible a homogénea

Mientras que las [[1708330960-ecuacin-diferencial-homognea|ecuaciones homogéneas]] se podían escribir como $y' = f(y/x)$, las **ecuaciones reducibles a homogéneas** son aquellas que se pueden escribir como $y' = f\left( \frac{ax + by + c}{dx + ey + f}  \right)$

## Resolución

En estas ecuaciones, la función $f(x,y)$ no es homogénea de [[1707050060-grado-ecuacin-diferencial|grado]] cero debido a la presencia de los valores $c$ y $f$.

Para conseguir resolverlas, es necesario realizar un cambio de variable que depende de la naturaleza de las rectas $r: ax + by + c = 0$ y $s:dx + ey + f = 0$

- Si las rectas $r$ y $s$ se cortan en un punto ${(x_0,y_0)}$, para trasladar dicho punto al origen se utiliza el siguiente cambio, que genera una ecuación homogénea en $X$ e $Y$:

$${x = X + x_0 \;\;\;\;\; y = Y + y_0}$$

- Si las rectas $r$ y $s$ son paralelas, para resolver la ecuación diferencial como una variable de [[1708330652-eucacin-diferencial-de-variable-separada|variable separada]] es necesario realizar el siguiente cambio de variable:

$${u = ax + by}$$

## Ejemplo

Las ecuaciones ${y' = \frac{5x - 7y + 1}{3x + y - 2}}$ e ${y' = e^{\frac{5x-7y+1}{3x+y-2}}}$ son reducibles a homogéneas
