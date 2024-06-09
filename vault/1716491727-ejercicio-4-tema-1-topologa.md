---
id: 1716491727-ejercicio-4-tema-1-topologa
aliases:
 - Ejercicio 4 Tema 1 Topología
---

#topología 
## ¿Es [[1716491727-mtrica|distancia]] $d(x,y)=min(|x-y|, 1-|x-y|)$ en $[0,1)$?

1. $d(x,x)=min(|x-x|,1 - |x-x|)=min(0,1)=0$
2. $d(y,x)=min(|y - x|, 1 - |y - x|) = min(|x-y|, 1 - |x - y|) = d(x,y)$
3. $d(x,z) \leq d(x,y) + d(y,z)$

	Hay 8 casos posibles:
	
	Si $d(x,z) = 1 - |x-z|$ $d(x,y)=|x-y|$ $d(y,z)=|y-z|$
	
