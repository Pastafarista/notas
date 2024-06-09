---
id: 1716491727-para-cada-pareja-de-intervalos-en-r-existe-un-homeomorfismo-que-transforma-uno-en-otro
aliases:
 - Para cada pareja de intervalos en R existe un homeomorfismo que transforma uno en otro
---

#topología 

**Para cada pareja de intervalos en $\mathbb{R}$ existe un [[1716491727-homeomorfismo|Homeomorfismo]] que transforma uno en otro**

$\forall(a,b),(c,d) \subseteq \mathbb{R}$ 

1. Primero estiramos

	$b-a$ y $d - c$ son cuanto miden cada intervalo, $\frac{d-c}{b-a}$ es lo que tenemos que estirar $(a,b)$

	$f(x)=\frac{d-c}{b-a}x$

2. Luego desplazamos hasta que $f(a) = c$ por lo que restaremos $\frac{d-c}{b-a}a-c$

	$f(x) = \frac{d-c}{b-a}x - \frac{d-c}{b-a}a + c = \frac{d-c}{b-a}(x-a)+c$

## Ejemplo:

2. $(2,5) \rightarrow (-9,0)$
	- $(2,5)$ mide $3$ y $(-9,0)$ mide 9 entonces para pasar de $3$ a $9$ hay que estirarlo en un factor de $3 \rightarrow f(x)=3x$
	- Ahora nuestro homeomorfismo convierte $(2,5)$ en $(6,15)$ falta desplazarlo $15$ unidades
	- Entonces $f(x)=3x-15$ 
