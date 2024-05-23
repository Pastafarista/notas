---
id: 1716491727-ejercicio-1-parcial-1c
aliases:
 - Ejercicio 1 Parcial 1ºC
---

#lógica 
## Dada la identidad $[(X \cap Z) - (Z \cap Y)] \cup [Y - (X \cup Z)] = [(X - Y) \cup (Y - X)] - [(Y \cap Z) \cup (X - (Y \cup Z))]$
1. Demostrarla utilizando diagramas de Venn.
2. Demostrarla formalmente.

## Resolución apartado 1:

![[1716491727-diagramas-venn|diagramas venn]]

## Resolución apartado 2:

#### **Vamos a demostrar la identidad formalmente mediante demostración directa:**

>$[(X \cap Z) - (Z \cap Y)] \cup [Y - (X \cup Z)] \Longleftrightarrow [(X - Y) - (X - (Y \cup Z))] \cup [(Y - X) - (Y \cap Z)]$

Reordenando:

>$[(X - Y) - (X - (Y \cup Z))] \cup [(Y - X) - (Y \cap Z)] \Longleftrightarrow [(X-Y) \cup (Y - X)] - [(Y \cap Z) \cup (X - (Y \cup Z))]$

**Como vemos si que son lo mismo, por lo tanto queda demostrada la identidad.**