---
id: 1716491727-ejercicio-1-parcial-1b
aliases:
 - Ejercicio 1 Parcial 1ºB
---


## Ejercicio 1. (2.5 puntos) Demostrar que $10^n + 1$ es múltiplo de 11 para cualquier $n \in \mathbb{N}$ impar.

## Resolución:

**Primero deberemos pasar nuestro enunciado a [[1716491727-lgica-de-primer-orden|Lógica de Primer Orden]], para ello usaremos los siguientes predicados:

>$P_{1}(x) = \exists n \in \mathbb{N} \;\; tq \;\; x = 2n+1$         $\equiv$      $P_{1}(x)=$ "x es impar" 
>$P_{2}(x) = x \;\; mod \;\; 11 = 0$                     $\equiv$       $P_{2}(x) =$ "x es múltiplo de 11"


Una vez ya tenemos el predicado, nuestro enunciado quedaría:

>$\forall n \in \mathbb{N} \;\; tq \;\; P_{1}(n) \;\; | \; P_{2}(10^n + 1)$

**Ahora que ya hemos pasado el enunciado a lógica de primer orden, lo demostraremos mediante demostración directa:**

1. Primero podemos reescribir la demostración de la siguiente forma:
	>$\forall k \in \mathbb{N} \;\; \exists m \in \mathbb{N} \;\; | \; 10^{2k + 1} + 1 = 11m$
2. Desarrollando tenemos:
	>$10^{2k+1} + 1 = 10^{2k} \cdot 10 +1 = (10^k)^2 \cdot 10 + 1$
	