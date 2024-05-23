---
id: 1716491728-topologa-de-sorgenfrey
aliases:
 - Topología de Sorgenfrey
---

#topología 

$X=\mathbb{R}$

[[1716491727-conjunto-abierto|abiertos]] y [[1716491727-conjunto-cerrado|cerrados]] en Sorgenfrey:

- $[a,b) \text{ son abiertos y cerrados}$
	Es cerrado ya que su complementario $(-\infty,a) \cup [b,+\infty)$ es abierto
- $(a,b) \text{ son abiertos}$
	$(a,b) = \cup[\frac{1}{n} + a,b)$
- $(a, \infty) \text{ son abiertos}$
	$(a, \infty) = \cup[\frac{1}{n} + a, n)$
- $(-\infty, a), [a,+\infty) \text{ son abiertos y cerrados}$
	$(-\infty,a) = \cup [-n,4) \implies (-\infty,a) \text{ es abierto}$
	$(-\infty,a)^{comp}=[a,+\infty) \implies [a, +\infty) \text{ es cerrado}$
	$[a,+\infty) = \cup[a,n]$ 
	$(-\infty,a)^{comp}=[a,+\infty) \text{ que es abierto} \implies (-\infty,a) \text{ es cerrado}$

- La topología de Sorgenfrey es más fina que la [[1716491728-topologa-cannica|canónica]]
- La topología de Sorgenfrey es la [[1716491728-topologa-inducida-por-la-base|topología inducida por la base]] de la base $B = \{[a,b) : a,b \in \mathbb{R}\}$