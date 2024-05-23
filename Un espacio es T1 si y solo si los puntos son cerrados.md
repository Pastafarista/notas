#topología

$\implies$ Si es [[Espacio T1]] los puntos son cerrados
- Si es $T_1$, queremos comprobar que el conjunto {$x$} es cerrado, es decir, que su complementario $X \setminus \{ x\}$ es abierto.
- Sabemos que cualquier punto $y$ tiene un abierto $A_y$ que no incluya el punto $x$. Consideremos la unión de todos los $U_{y\in X, y \neq x} \; A_y = X \setminus \{x\}$. Es abierto, por lo que $\{x\}$ es cerrado

$\impliedby$ Si los puntos son cerrados, es $T_1$

- Si el punto es cerrado, su complementario es abierto. Cogiendo cualquier $y$ buscamos un [[Conjunto abierto|entorno abierto]] suyo que no contenga $x$
- Pues resulta un entorno suyo que no contenga a $x$ siempre va a ser $X \setminus \{x\}$
- Por lo tanto, cada pareja de puntos $x,y$ tienen entornos abiertos en los que no está el otro ($X \setminus \{x\}$ y $X\setminus\{y\}$) y esto implica que el espacio es $T_1$
$$\forall x,y \in X: \;\; y \in X \setminus \{x\} \;\;x \in X \setminus \{y\} \;\; y \notin X \setminus \{y\} \;\;x \notin X \setminus \{x\}$$