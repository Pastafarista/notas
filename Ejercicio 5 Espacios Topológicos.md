#topología 


## En la [[Topología de semirrectas derechas]] ¿son [[Función continua]]'s?

1. $f(x)=2x$
	
	$f^{-1}(x) = \frac{x}{2}$
	Si tomamos el abierto $U = (a, +\infty)$ tenemos que $f^{-1}(U)=(\frac{a}{2},+\infty)$ que es abierto, por lo que se cumple que [[Una función es continua si y sólo si la preimagen de un conjunto abierto es abierta]]

2. $f(x) = -x$
	
	$f^{-1}(x) = -x \implies f^{-1}(U)=(-\infty, -a)$ que es cerrado, por lo que la función no es continua   

3. $f(x)=x^2$
	
	$f^-1(x)= \pm \sqrt{x} \implies f^{-1}(U)=(-\infty, -\sqrt{a})\cup(\sqrt{a}.\infty)$, como el primero no es abierto la función no es continua

4. $f(x)=x^3$
	
	$f^{-1}(x)=\sqrt[3]{x} \implies f^{-1}(U)=(\sqrt[3]{x},+\infty)$ que es abierto, por lo que la función es abierta 

## ¿Y en la [[Topología de Sorgenfrey]]?

1. $f(x) = 2x$
	
	$U = [a,b)$
	$f^{-1}(x) = \frac{x}{2} \implies f(U) = [\frac{a}{2}, \frac{b}{2})$ que es abierto, por lo que la función en continua

2. $f(x)=-x$
	
	$f^{-1}(x)=-x \implies f(U) = (-b, -a]$ que no es abierto

3. $f(x)=x^2$
	
	$f^{-1}(x) = \pm \sqrt{x} \implies f^{-1}(x) = (-\sqrt{b}, \sqrt{a} \; ] \cup [\sqrt{a}, \sqrt{b})$ como el primero no es abierto, la función no es continua

4. $f(x)=x^3$
	
	$f^{-1}(x)=\sqrt[3]{x} \implies f^{-1}(U)=[\sqrt[3]{a}, \sqrt[3]{b})$ que es abierto, por lo que la función es continua

## ¿Y en la [[Topología Cofinita]]?

1. $f(x)=x^2$
	
	$f^{-1}(\mathbb{R} \setminus \{0,2\})=\mathbb{R} \setminus \{0,\sqrt{2},-\sqrt{2}\}$ Como vemos la imagen de un abierto es un abierto, por lo que la función es continua

2. $f(x)=-x$
	
	$f^{-1}(\mathbb{R} \setminus \{0,2\}) = \mathbb{R} \setminus \{0,-2\}$ Si es continua

3. [[Función de Dirichlet]]
	
	No es continua