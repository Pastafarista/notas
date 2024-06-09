---
id: 1716491727-ejercicio-6-tema-2-topologa
aliases:
 - Ejercicio 6 Tema 2 Topología
---

#topología 

## ¿Existe una función discontinua en $\mathbb{Q}$ y continua en $\mathbb{R} \setminus \mathbb{Q}$?

La [[1716491727-funcin-de-thomae|Función de Thomae]] es una [[1716491727-funcin-continua|Función continua]] en los irracionales y discontinua en los racionales

### Demostración

1. Es continua en los irracionales:

![[Ejercicio 6 Tema 2 Topología 2023-10-31 16.46.32.excalidraw]]

Utilizando el [[1716491727-teorema-de-continuidad-y-convergencia|Teorema de continuidad y convergencia]] tenemos que $\forall x \in \mathbb{R} \setminus X :\forall x_n \text{ convergente a } x \text{ se cumple que } f(x_n)=0$, Como vemos los $x_n$ convergen a 0 que es también $f(x)$, por lo que la función efectivamente es continua (ESTA-MAL)


2. Es discontinua en los racionales:

- $x = \frac{p}{q} \in \mathbb{Q}$
- Consideremos la sucesión de irracionales $a_n = x + \frac{\pi}{n} \; \forall n \in \mathbb{N}$ que converge a $x$
- La imagen de todos los términos de esta sucesión son igual a 0, ya que son números irracionales $f(a_n)=0$, por lo que $f(a_n)$ converge a 0 
- Como $f(a_n)$ converge a $0 \neq \frac{1}{q}$, entonces por el [[1716491727-teorema-de-continuidad-y-convergencia|Teorema de continuidad y convergencia]] queda demostrado que en los racionales no es continua
