#topología #topología

**No en todas las [[Topología|topologías]]** las [[Sucesión convergente|sucesiones]] convergen a un solo punto

Contraejemplos: Cualquier topología que no sea [[Espacio Hausdorff|Hausdorff]] como la [[Topología Cofinita|cofinita]] o [[Topología de Sorgenfrey|Sorgenfrey]]

## Demostración:

Utilizaré una [[Topología Discreta|topología discreta]] que no sea [[Espacio Hausdorff|Hausdorff]] como por ejemplo:

$T = \{\{\},\{A\}, \{A,B\}, \{A,C\}, \{A,B,C\}\}$

- como vemos no es T2 ya que $A \in \{ A\} \; \; B \in \{A,B\} \;\; \{A\} \cap \{A,B\} = A \neq \emptyset$
- Tomemos la [[Sucesión convergente|sucesión]] $x_n = A$
- Como no hay [[Métrica|distancia]] obviaremos la parte de las [[Bola Abierta|bolas abiertas]] de la definición de [[Sucesión convergente|sucesión convergente]]
- Como vemos, para cualquier $n>0$ , existen 3 [[Conjunto abierto|entornos abiertos]] que contienen a $A$ :$(\{A\}, \{A,B\}, \{A,C\}, \{A,B,C\})$ por lo que la sucesión converge a más de un punto