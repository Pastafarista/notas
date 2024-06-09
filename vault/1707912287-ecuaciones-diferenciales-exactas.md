---
id: 1707912287-ecuaciones-diferenciales-exactas
aliases:
  - Ecuaciones diferenciales exactas
  - Ecuación diferencial exacta
tags:
  - ecuaciones-diferenciales
---

# Ecuaciones diferenciales exactas

Dada una función $F(x,y)$ que posee derivadas parciales [[1716491727-funcin-continua|continuas]] en un dominio $D \subset \mathbb{R}^2$, se define su diferencial total de la siguiente manera:

$${dF(x,y) = \frac{\partial F(x,y)}{\partial x} dx + \frac{\partial F(x,y)}{\partial y}dy}$$

Dada la [[1708330318-ecuacin-diferencial-ordinaria-de-primer-orden|ecuación]] ${M(x,y)dx + N(x,y)dy = 0}$, se dice que es una **ecuación diferencial exacta** si existe una función $F(x,y)$ tal que ${dF=M(x,y)dx + N(x,y)dy = 0}$, con lo que la [[1707058998-solucin-de-una-ecuacin-diferencial-ordinaria|solución de la ecuación]] viene dada por la expresión $F(x,y)=C$

## Condiciones de exactitud

Para poder saber si una [[1706869334-ecuacin-diferencial|ecuación diferencial]] es exacta podemos utilizar el siguiente teorema:


La ecuación diferencial ${M(x,y)dx + N(x,y)dy = 0}$ es exacta si y solo si ${M(x,y)}$ y ${N(x,y)}$ admiten derivadas parciales continuas en un dominio $D$ y además ${\frac{\partial M(x,y)}{\partial y} = \frac{\partial N(x,y)}{\partial x}}$

## Resolución

Para resolver la ecuación diferencial exacta, debemos comenzar por una de las dos derivadas parciales de $F$, por ejemplo ${\frac{\partial F(x,y)}{\partial x} = M(x,y)}$.

A continuación se integra dicha expresión, con lo que se obtiene ${F(x,y) = \int M(x,y)dx + C(y)}$

Por ultimo, debemos derivar respecto de la variable $y$, igualando dicha expresión a $N(x,y)$, con lo que será posible determinar el término ${C(y)}$ y, con ello, la expresión de la [[1707058998-solucin-de-una-ecuacin-diferencial-ordinaria|solución a la ecuación]]

## Ejemplo

La diferencial total de ${F(x,y) = xy + 2x^3y^2 \text{ es } dF=(y + 6x^2y^2)dx + (x + 4x^3y)dy}$
