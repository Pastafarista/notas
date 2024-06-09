---
id: 1716491727-ejercicio-4-examen-lymd-2122-covid
aliases:
 - Ejercicio 4 Examen LyMD 21-22 Covid
---

#lógica 
## Analizar la consistencia del siguiente razonamiento:

- Cuando me levanto perezoso me cuesta estudiar.
- Es suficiente con que me tome un café para que no me cueste estudiar.
- Cuando me levanto perezoso me tomo un café.
- Me cuesta estudiar.

## Resolución:

**Primero definimos nuestras variables:**

>Cuando me levanto perezoso $\equiv A$
>Me cuesta estudiar $\equiv B$
>Tomar un café $\equiv C$

**Luego pasamos nuestros enunciados a lógica proposicional:**

>$A \implies B$
>$C \implies \lnot B$
>$A \implies C$
>$B$

**Ahora construimos nuestra expresión $f$ y vemos que pasa para $A = V$, $B = V$ y $C = V$:**

>$f(A,B,C) = (A \implies B) \land (C \implies \lnot B) \land (A \implies C) \implies B$
>$f(V,V,V) = (V \implies V) \land (V \implies F) \land (V \implies V) \implies V = V \land F \land V \implies V = F \implies V = V$

**Cuando todos son verdaderos $f$ es verdadero, por lo que nuestro razonamiento inicial si tiene consistencia.**
