
## Origen de la idea

$T = \{\{\},\{A\}, \{A,B\}, \{A,C\}, \{A,B,C\}\}$

¿A donde converge la [[Sucesión convergente]] $x_n = A$?
 
- Converge a $\{A\}, \{A,B\}, \{A,C\}, \{A,B,C\}$

Queremos evitar estos casos, ¿Cuál era el problema?
	Que no habían entornos que separaban $A$ y $B$
### [[Espacio Hausdorff|Propiedad de Hausdorff]] o $T_2$

- Un espacio tiene la propiedad de Hausdorff si para cada parejas de puntos $x_1, x_2 \in X$ existen entornos disjuntos $x_1 \in U_1, x_2 \in U_2: U_1 \cap U_2 = \emptyset$
- Ejemplo: [[La topología canónica es T2]]

### [[Espacio T1|Propiedad T1]] o Propiedad de Fletcher

- Un espacio es $T_1$ si para cada pareja de puntos $x_1, x_2 \in X$ existen $x_1 \in U_1,x_2 \in U_2: x_1 \notin U_2$ y $x_2 \notin U_1$
- 
## ¿Cuál es más restrictiva?

- Claramente Hausdorff es más restrictiva ya que $Hausdorff \implies T_1$
- Para las topologías discretas es al revés, pero no siempre

**Si un espacio es Hausdorff entonces**

- Cada sucesión convergente converge a único punto #TODO -> demostración fácil
- Los puntos son conjuntos [[Conjunto cerrado|cerrados]]
- Además, si los puntos son cerrados, el espacio es $T_1$

$\text{Hausdorff} \Longleftrightarrow \text{Sucesiones convergen a un punto}$
$\text{Hausdorff} \implies \text{Puntos cerrados}$

**La topología [[Topología Cofinita]] satisface $T_1$ pero no $T_2$** #TODO

$\mathbb{R} \setminus \{x_1\}$
$\mathbb{R} \setminus \{x_2\}$

Si los puntos son cerrados sus complementarios son abiertos y entonces sus complementarios tienen puntos en común y por lo tanto son Hausdorff

## Teoremas:

- [[Un espacio es T1 si y solo si los puntos son cerrados]]
- [[Si un espacio es Hausdorff y es un espacio finito, entonces es topología discreta]]

## Ejercicios

[[Ejercicio 1 Hausdorff]]


