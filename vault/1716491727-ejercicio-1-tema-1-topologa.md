---
id: 1716491727-ejercicio-1-tema-1-topologa
aliases:
 - Ejercicio 1 Tema 1 Topología
---

#topología 

## ¿Cuáles son [[1716491727-distancias|Distancias]] en $\mathbb{R}$?

- $d(x,y) = |x-y|$

1. $d(x,x) = |x-x| = 0$
2. $d(y,x) = |y-x| = |-(x-y)| = |x-y| = d(x,y)$
3. $d(z,x)=d(x,y)+d(y,z) \Longleftrightarrow |x-z| \leq |x-y| + |y-z|$ 
	$a=x-y, \; b = y-z \implies |a+b| \leq |a| + |b|$ 

- $d(x,y) = |x^2 -y^2|$

1. $d(x,x)=|x^2 - x^2| = 0$
	$d(x,-x) = | x^2 - (-x)^2| = 0$

- $d(x,y)=|x-2y|$

1. $d(x,x)=|x-2x|=x\neq0$

- $d(x,y)=(x-y)^2$

1. $d(x,x)=(x-x)^2=0$
2. $d(y,x)=(y-x)^2 = x^2 + y^2 -2xy = d(x,y)$
3. $d(x,z) \neq d(x,y) + d(y,z) \Longleftrightarrow (x-z)^2 = (x-y)^2 + (y-z)^2$
	$(1+1)^2 = 4 > (1-0)^2 + (0+1)^2 = 2$

- $d(x,y)=sin^2(x-y)$

1. d(0,\pi) = sin^2(\pi)=0$

- $d(x,y)=arctan|x-y|$

1. $d(x,x)=arctan|x-x|=arctan(0)=0$
2. $d(y,x)=arctan|y-x|=arctan|x-y|=d(x,y)$
3. $d(x,z)\leq d(y,x) + d(y,z) \Longleftrightarrow \arctan|a| + \arctan|b|$
	- Como la función $arctan|x|$ es una [[1716491727-funcin-continua|función continua]] estrictamente creciente, entonces la [[1716491727-desigualdad-triangular|desigualdad triangular]] se seguirá cumpliendo ya que si $\alpha > \beta$ se cumple que $\arctan(\alpha) > \arctan(\beta)$