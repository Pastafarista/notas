#topología 


![[Conjunto Peine 2023-11-24 11.11.41.excalidraw]]

$$Peine (con \;\; vertices) = 
\begin{split}
	\{(x,y), \; x = \frac{1}{n}, \; n \in \mathbb{N}: y \in [0,1]\} \cup \{(0,y): y \in \{0,1\}\} \cup \{(x,0): x \in [0,1]\}
\end{split}
$$

- El conjunto Peine es un conjunto [[Espacios conexos|conexo]]
	- El conjunto peine completo es un conjunto conexo ya que es [[Espacio conexo por caminos|conexo por caminos]] ([[conexo por caminos implica conexo]])
	- Usando [[Si A es un subconjunto conexo cualquier subconjunto B con A sub B sub cl(A), es también conexo|este teorema]]:
$$Peine(\text{sin la primera pua}) \subset Peine(\text{con vertices})\subset \overline{Peine(\text{sin la primera pua})}$$
- El conjunto Peine no es [[Espacio conexo por caminos||conexo por caminos]] ya que no existe ningún camino para llegar al punto $(1,1)$ o al $(0,1)$