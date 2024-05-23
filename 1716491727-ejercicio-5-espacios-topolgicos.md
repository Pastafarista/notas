---
id: 1716491727-ejercicio-5-espacios-topolgicos
aliases:
 - Ejercicio 5 Espacios Topológicos
---

#topología 


## En la [[1716491728-topologa-de-semirrectas-derechas|Topología de semirrectas derechas]] ¿son [[1716491727-funcin-continua|Función continua]]'s?

1. $f(x)=2x$
	
	$f^{-1}(x) = \frac{x}{2}$
	Si tomamos el abierto $U = (a, +\infty)$ tenemos que $f^{-1}(U)=(\frac{a}{2},+\infty)$ que es abierto, por lo que se cumple que [[1716491728-una-funcin-es-continua-si-y-slo-si-la-preimagen-de-un-conjunto-abierto-es-abierta|Una función es continua si y sólo si la preimagen de un conjunto abierto es abierta]]

2. $f(x) = -x$
	
	$f^{-1}(x) = -x \implies f^{-1}(U)=(-\infty, -a)$ que es cerrado, por lo que la función no es continua   

3. $f(x)=x^2$
	
	$f^-1(x)= \pm \sqrt{x} \implies f^{-1}(U)=(-\infty, -\sqrt{a})\cup(\sqrt{a}.\infty)$, como el primero no es abierto la función no es continua

4. $f(x)=x^3$
	
	$f^{-1}(x)=\sqrt[3]{x} \implies f^{-1}(U)=(\sqrt[3]{x},+\infty)$ que es abierto, por lo que la función es abierta 

## ¿Y en la [[1716491728-topologa-de-sorgenfrey|Topología de Sorgenfrey]]?

1. $f(x) = 2x$
	
	$U = [a,b)$
	$f^{-1}(x) = \frac{x}{2} \implies f(U) = [\frac{a}{2}, \frac{b}{2})$ que es abierto, por lo que la función en continua

2. $f(x)=-x$
	
	$f^{-1}(x)=-x \implies f(U) = (-b, -a]$ que no es abierto

3. $f(x)=x^2$
	
	$f^{-1}(x) = \pm \sqrt{x} \implies f^{-1}(x) = (-\sqrt{b}, \sqrt{a} \; ] \cup [\sqrt{a}, \sqrt{b})$ como el primero no es abierto, la función no es continua

4. $f(x)=x^3$
	
	$f^{-1}(x)=\sqrt[3]{x} \implies f^{-1}(U)=[\sqrt[3]{a}, \sqrt[3]{b})$ que es abierto, por lo que la función es continua

## ¿Y en la [[1716491728-topologa-cofinita|Topología Cofinita]]?

1. $f(x)=x^2$
	
	$f^{-1}(\mathbb{R} \setminus \{0,2\})=\mathbb{R} \setminus \{0,\sqrt{2},-\sqrt{2}\}$ Como vemos la imagen de un abierto es un abierto, por lo que la función es continua

2. $f(x)=-x$
	
	$f^{-1}(\mathbb{R} \setminus \{0,2\}) = \mathbb{R} \setminus \{0,-2\}$ Si es continua

3. [[1716491727-funcin-de-dirichlet|Función de Dirichlet]]
	
	No es continua