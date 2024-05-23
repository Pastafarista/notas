---
id: 1716491727-ejercicio-4-parcial-1b
aliases:
 - Ejercicio 4 Parcial 1ºB
---

#lógica 
## Analizar la consistencia del siguiente razonamiento.

-  Es necesario abrir el menú para iniciar la partida.
-  Si pulsas X, abrirás el menú.
- Es necesario no pulsar X para no iniciar la partida.
- No abro el menú.

## Resolución

**Primero definimos nuestras variables:**

>Abrir el menú $\equiv A$
>Iniciar la partida $\equiv B$
>Pulsar X $\equiv C$

**Luego pasamos nuestros enunciados a lógica proposicional:**

>$B\implies A$
>$C \implies A$
> $\lnot B \implies \lnot C$
> $\lnot A$

**Ahora construimos nuestra expresión $f$ y vemos que pasa para $A = V$, $B = V$ y $C = V$:**

>$f(A,B,C) = (B \implies A) \land (C \implies A) \land ( \lnot B \implies \lnot C)  \implies \lnot A$
>$f(V,V,V) = (V \implies V) \land (V \implies V) \land ( \lnot V \implies \lnot V)  \implies \lnot V = V \land V \land V \implies F = V \implies F = F$

**Como vemos cuando todos son verdaderos $f$ es falso, por lo que el razonamiento no tiene consistencia.**