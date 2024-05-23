---
id: 1716491727-ejercicio-18-ejercicios-lgica
aliases:
 - Ejercicio 18 Ejercicios Lógica
---

#lógica
## Ejercicio 18. Si $n$ es un entero y $n^2$ es par (respectivamente, múltiplo de 3), probar que $n$ es par (respectivamente, múltiplo de 3).

## Resolución:

**Primero deberemos pasar nuestro enunciado a [[1716491727-lgica-de-primer-orden|Lógica de Primer Orden]]:**


>$P_1(x)= \exists k \in \mathbb{Z} \; | \; x = 2k$

>$P_2(x)= \exists k \in \mathbb{Z} \; | \; x = 3k$

>$\forall n \in \mathbb{Z} \; tq \; P_1(n^2) \land P_2(n^2) \implies P_1(n) \land P_2(n)$

Podemos simplificar las condiciones de que sea par y múltiplo de 3 en:

>$P_1(x) \land P_2(x) = \exists k \in \mathbb{R} \; | \; 6k$

Teniendo esto en cuenta, vamos a demostrarlo mediante reducción al absurdo.

>Supongamos que n no es par ni múltiplo de 3, es decir que $n \neq 6k \; | \; k \in \mathbb{Z}$
>Entonces tenemos que $n^2 = (6k)^2 = 6(6k^2) = 6k'$

Como vemos hay una contradicción ya que $n^2$ si es par y múltiplo de 3, por lo que queda demostrado que si se cumple.

>$A \equiv n^2 \text{ es par y múltiplo de 3}$
>$B \equiv n \text{ es par y múltiplo de 3}$
>$(A \land \lnot B) \implies F$
 