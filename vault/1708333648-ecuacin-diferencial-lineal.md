---
id: 1708333648-ecuacin-diferencial-lineal
aliases:
  - Ecuación diferencial lineal
tags:
  - ecuaciones-diferenciales
---

# Ecuación diferencial lineal

Las [[1706869334-ecuacin-diferencial|ecuación diferencial]] **lineales** de [[1708330318-ecuacin-diferencial-ordinaria-de-primer-orden|primer orden]] son las que tienen el siguiente formato:

$${y' + p(x)y = r(x)}$$

## Resolución

### 1. Solución conocida una solución particular de la ecuación completa

La solución de estas ecuaciones se puede obtener como la suma de la [[1707058998-solucin-de-una-ecuacin-diferencial-ordinaria|solución general]] de la ecuación lineal [[1708330960-ecuacin-diferencial-homognea|Ecuación diferencial homogénea|homogénea]] asociada más una solución particular de la ecuación completa

$${y = y_{\text{SGEH}} + y_{SPEC}}$$

La [[1708330960-ecuacin-diferencial-homognea|ecuación homogénea asociada]] es una ecuación con la forma ${y' = p(x)y = 0}$, por lo que se podrá resolver como una [[1708330652-eucacin-diferencial-de-variable-separada|ecuación diferencial de variable separada]] 

La dificultad consistirá, entonces, en determinar una solución particular de la ecuación completa

### 2. Solución conocida dos soluciones particulares de la ecuación completa

Si se conocen dos [[1707058998-solucin-de-una-ecuacin-diferencial-ordinaria|soluciones]] de la ecuación completa, ${y_{SPEC1}}$ y ${y_{SPEC2}}$, tal que una no sea proporcional a la otra, entonces la solución general de la ecuación completa viene dada por la expresión:
$${y=C(y_{SPEC1} - y_{SPEC2}) + y_{SPEC1}}$$

En realidad, es posible demostrar que la solución de la [[1708330960-ecuacin-diferencial-homognea|ecuación homogénea]] es precisamente ${Y_{SGEH} = C(y_{SPEC1} - y_{SPEC2})}$, por lo que se trataría de un caso particular del caso anterior

### 3. Método de variación de constantes

Puesto que la [[1707058998-solucin-de-una-ecuacin-diferencial-ordinaria|solución]] de la [[1708330960-ecuacin-diferencial-homognea|ecuación homogénea]] asociada se puede escribir ${y = Ke^{-\int p(x) dx}}$, suponemos que el elemento $K$ en realidad depende de $x$, con lo que tendríamos un solución de la ecuación completa que sería ${y = K(x)e^{-\int p(x) dx}}$

A continuación se debe introducir esa solución en la ecuación completa a fin de poder determinar la expresión de $K(x)$

### 4. Método del factor integrante

Se puede tratar la ecuación completa $y' = p(x)y = r(x)$ como una ecuación que admite un factor integrante de la forma ${\mu(x) = e^{\int p(x)dx}}$
