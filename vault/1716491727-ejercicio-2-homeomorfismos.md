---
id: 1716491727-ejercicio-2-homeomorfismos
aliases:
 - Ejercicio 2 Homeomorfismos
---


## Inventa un [[1716491727-homeomorfismo|Homeomorfismo]]

1. $\mathbb{R}^+ \rightarrow \mathbb{R}$
	Si $f(x) = e^x$ va de $f:\mathbb{R} \rightarrow \mathbb{R}$ entonces $f^{-1}(x)=ln(x)$ va de $f: \mathbb{R}^+ \rightarrow \mathbb{R}$

2. $(2,5) \rightarrow (-9,0)$
	- $(2,5)$ mide $3$ y $(-9,0)$ mide 9 entonces para pasar de $3$ a $9$ hay que estirarlo en un factor de $3 \rightarrow f(x)=3x$
	- Ahora nuestro homeomorfismo convierte $(2,5)$ en $(6,15)$ falta desplazarlo $15$ unidades
	- Entonces $f(x)=3x-15$ 
	
	[[1716491727-para-cada-pareja-de-intervalos-en-r-existe-un-homeomorfismo-que-transforma-uno-en-otro|Para cada pareja de intervalos en R existe un homeomorfismo que transforma uno en otro]]

3. $(0,1)\rightarrow \mathbb{R}$

	- $f(x)=\tan(x) \;\; f:(-\frac{\pi}{2},\frac{\pi}{2})\rightarrow \mathbb{R}$  Entonces tenemos que hacer otro homeomorfismo tal que $f_1:(-\frac{\pi}{2},\frac{\pi}{2}) \rightarrow (0,1)$ 
	- $f_1(x)=x \cdot \pi - \frac{\pi}{2}$ 
	- $f(x)=\tan(x \cdot \pi - \frac{\pi}{2})$
	
	- Otro ejemplo: $f_1(x)= \frac{1}{1-x}$ $f_1:(0,1) \rightarrow (0,\infty)$

4. $\{ x \in \mathbb{R}^n:0 < |x| \leq 1\} \rightarrow \{x \in \mathbb{R}^n:|x| \geq 1\}$

	Pasa todos los puntos de dentro del círculo a uno del plano fuera del círculo
	![[Ejercicio 2 Homeomorfismos 2023-11-03 11.27.21.excalidraw]]
	$d_1 \cdot d_2 = 1$
	$d_2 = \frac{1}{d_1}$
	$f(z) = \frac{z}{||z||}$ es una inversión