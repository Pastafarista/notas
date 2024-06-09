---
id: 1716491727-ejercicio-4-examen-lymd-2122
aliases:
 - Ejercicio 4 Examen LyMD 21-22
---

#lógica 
## Analizar la consistencia del siguiente razonamiento:

- Si un triángulo tiene tres ángulos, un cuadrado tiene cuatro ángulos rectos.
- Un triángulo tiene tres ángulos y la suma de los mismos es igual a dos ángulos rectos.
- Si un rombo tiene cuatro ángulos rectos, entonces un cuadrado no tiene cuatro ángulos rectos.
- Por tanto, un rombo no tiene cuatro ángulos rectos.

## Resolución:

**Primero definimos nuestras variables:**

>Un triángulo tiene tres ángulos $\equiv A$
>Un cuadrado tiene cuatro ángulos rectos $\equiv B$
>La suma de los ángulos de un triángulo es igual a dos ángulos rectos $\equiv C$
>Un rombo tiene cuatro ángulos rectos $\equiv D$

**Luego pasamos nuestras enunciados a lógica proposicional:**

>$A \implies B$
>$A \land C$
>$D \implies \lnot B$
>$\lnot D$

**Ahora construimos nuestra expresión $f$ y vemos que pasa para $A = V$, $B = V$ y $C = V$:**

>$f(A, B, C, D) = (A \implies B) \land (A \land C) \land (D \implies \lnot B) \implies \lnot D$
>$f(V, V, V, V) = (V \implies V) \land (V \land V) \land (V \implies F) \implies F = V \land V \land V \land F \implies F = F \implies F = V$ 

**Cuando todos son verdaderos $f$ es verdadero, por lo que nuestro razonamiento inicial si tiene consistencia.**