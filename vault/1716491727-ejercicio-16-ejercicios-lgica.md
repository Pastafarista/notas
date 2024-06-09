---
id: 1716491727-ejercicio-16-ejercicios-lgica
aliases:
 - Ejercicio 16 Ejercicios Lógica
---

#lógica 
## Demostrar que si $m,n \in \mathbb{Z}$ son múltiplos de $p \in \mathbb{Z}$, entonces m + n y m − n también son múltiplos de p.

## Resolución:

**Primero deberemos pasar nuestro enunciado a [[1716491727-lgica-de-primer-orden|Lógica de Primer Orden]]:**

>$\forall m,n \in \mathbb{Z} \;\; tq \;\; \exists p \in \mathbb{Z} \;\; tq \;\; (m \;\; mod \;\; p = 0) \land (n \;\; mod \;\; p = 0) \implies [(m + n) \;\; mod \;\; p = 0] \land [(m - n) \;\; mod \;\; p = 0]$

Podemos escribir que m sea múltiplo de p como $m \;\; mod \;\; p = 0$, pero también lo podemos expresar como $\exists c \in \mathbb{Z} \;\; tq \;\; m = p \cdot c$ 

Teniendo esto en cuenta, vamos a empezar demostrando que $(m + n)$ también es múltiplo de $p$:

>$(m = p \cdot c_{1}) \land (n = p \cdot c_{2}) \implies (m+n) = p \cdot c_{1} + p \cdot c_{2} = p \cdot (c_{1} + c_{2})$
>$c=(c_{1}+c_{2})\in \mathbb{Z}$
>$(m + n) = p \cdot c$ 

Para $(m-n)$ sería lo mismo:

>$(m = p \cdot c_{1}) \land (n = p \cdot c_{2}) \implies (m-n) = p \cdot c_{1} - p \cdot c_{2} = p \cdot (c_{1} - c_{2})$
>$c=(c_{1}-c_{2})\in \mathbb{Z}$
>$(m + n) = p \cdot c$ 

Como vemos hemos demostrado por demostración directa que si $m$ y $n$ son múltiplos de $p$, entonces $(m+n)$ y $(m-n)$ también lo son. 